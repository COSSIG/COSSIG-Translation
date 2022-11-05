[#]: subject: "How updates work in CentOS"
[#]: via: "https://blog.centos.org/2022/09/how-updates-work-in-centos/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: "fosinoprilsodium"
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

How updates work in CentOS
======

This document is an attempt to explain the relationship between Fedora Linux, CentOS Stream and RHEL, with a specific focus around how package updates flow between them.

## From Fedora to CentOS Stream

Fedora is where day-to-day development and innovation happens. Fedora Linux releases every 6 months and each release is maintained for about 13 months. Major changes should be (and almost always are) deployed in Fedora first, following the [Change process][1]. Fedora packages sources are maintained in [dist-git][2] and built in [Fedora Koji][3].

At the beginning of the development cycle of a new CentOS major release (meaning, `9`, `10`, etc.), Fedora is branched into the new distribution. Historically, this is done from the current stable Fedora release at the branching time (e.g. Fedora 34 for CentOS Stream 9). After the distribution is branched, the development cycle for the new CentOS Stream release begins.

Nowadays, [Fedora ELN][4]helps prepare for the branching process by continuously rebuilding Rawhide (the development version of Fedora). This provides a view into what a new CentOS Stream could look like if it were branched from Fedora today, and ensures that the spec file logic stays compatible with the future set of EL macros and build flags at any given point in time.

## From CentOS Stream to RHEL

CentOS Stream package sources are maintained in [GitLab][5], and that is where most of the distribution [development work][6] happens after branching. Packages are built on the [CentOS Stream Koji][7] and are delivered as part of regularly-produced [distribution composes][8]. Composes for Stream are generated 2-3 times a week, and they usually include updates that have been released during that time window, but there is no actual SLA around updates flowing into Stream.

RHEL point releases are essentially, but not actually, a snapshot in time of a given Stream compose, with actual development work happening on the Stream side and showing up there first. In general, a given package will go through QA, then land into Stream, then down the road be incorporated into the next RHEL minor release. In this sense, Stream acts as a continuously-delivered preview of the next RHEL minor release. Aleksandra Fedorova also talks about this process in detail in her [OpenInfra Summit talk][9].

Once a given RHEL release is out, the corresponding sources are delivered on [git.centos.org][10], where they can be consumed by RHEL rebuild projects such as Alma Linux and Rocky Linux.

## Deep dive: critical security erratas

As explained above, the general assumption is that packages will land in CentOS Stream first. There is one exception to this, which is embargoes security fixes and security erratas rated critical or important. These are developed by Red Hat and held until the embargo expires. They are then released to RHEL first, and then flow into Stream.

There’s two practical scenarios at hand here.

### RHEL and CentOS Stream have a package with the same NVR

When an errata comes out for RHEL, the package is updated there. In this case, you will see thesame NVR that came out for RHEL come out for Stream as well.

The [polkit CVE][11] from last December is a good example of this: both RHEL 8 and CentOS Stream 8 were at [polkit-0.115-11.el8_4.1][12] before the CVE, and [polkit-0.115-13.el8_5.1][13] fixes the CVE in both.

### CentOS Stream has a package with a greater NVR than RHEL

In this scenario, CentOS Stream is ahead of RHEL for a given package. When an errata comes out for RHEL the package is updated there, but its version remains behind the Stream one. In this case, assuming the update still applies to the CentOS Stream version, a new update will be made for Stream, either by backporting the changes onto the latest Stream package version or by rebasing the package.

AnotherCVE, this time in libxml2, provides a good example of this. RHEL was at [libxml2-2.9.7-9.el8][14] before the CVE, and issued a fixed package as [libxml2-2.9.7-9.el8_4.2][15]. Within Stream, the fix was instead included in [libxml2-2.9.7-11.el8][16].

## Deep dive: CentOS Stream 8

CentOS Stream 8 was the first version of CentOS where the Stream development process was introduced, and has some significant differences. Notably:

- CentOS Stream 8 package sources are hosted on [git.centos.org][10] (under the `c8s` branch) instead of GitLab
- because of technical limitations, the contribution process for CentOS Stream 8 is different; the standard PR workflow isn’t supported, and the best way to contribute patches is by attaching them to a Bugzilla ticket against the relevant component
- CentOS Stream 8 packages are build on the [Koji mbox instance][17]

There is ongoing work to migrate CentOS Stream 8 onto the current development process and tooling, and the hope is to eventually minimize and hopefully eliminate these differences.

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/09/how-updates-work-in-centos/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[译者ID](https://github.com/译者ID)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://docs.fedoraproject.org/en-US/program_management/changes_policy/
[2]: https://src.fedoraproject.org
[3]: https://koji.fedoraproject.org
[4]: https://docs.fedoraproject.org/en-US/eln/
[5]: https://gitlab.com/redhat/centos-stream/rpms
[6]: https://gitlab.com/groups/redhat/centos-stream/rpms/-/merge_requests
[7]: https://kojihub.stream.centos.org
[8]: https://composes.stream.centos.org/
[9]: https://www.youtube.com/watch?v=yf1wO5Iu8uY
[10]: http://git.centos.org
[11]: https://koji.mbox.centos.org/koji/buildinfo?buildID=17891
[12]: https://koji.mbox.centos.org/koji/buildinfo?buildID=20924
[13]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-3541
[14]: https://koji.mbox.centos.org/koji/buildinfo?buildID=14132
[15]: https://koji.mbox.centos.org/koji/buildinfo?buildID=18244
[16]: https://koji.mbox.centos.org/koji/buildinfo?buildID=17568
[17]: https://koji.mbox.centos.org
