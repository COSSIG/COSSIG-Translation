[#]: subject: "CentOS Hyperscale SIG Quarterly Report for 2022Q3"
[#]: via: "https://blog.centos.org/2022/10/centos-hyperscale-sig-quarterly-report-for-2022q3/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: " "
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CentOS Hyperscale SIG Quarterly Report for 2022Q3
======

This report covers work that happened between July 5th and September 30th. For previous work, see the [2022Q2 report][1].

## Purpose

The [Hyperscale SIG][2] focuses on enabling CentOS Stream deployment on large-scale infrastructures and facilitating collaboration on packages and tooling.

## Membership update

Since the last update, the SIG gained two new members (Quentin Deslandes and Richard Phibel).

We welcome anybody that’s interested and willing to do work within the scope of the SIG to join and contribute. See the [membership][3] section on the wiki for the current members list and how to join.

## Releases and Packages

Unless otherwise specified, packages are available in our main repository, which can be enabled with `dnf install centos-hyperscale-release`. Please report any issues with these packages on our [package-bugs][4] tracker.

### Documentation

We have continued fleshing out our [user documentation][5] website, and recently completed a major restructuring that will hopefully make content easier to find and consume. Recent additions also include expanded and revamped documentation for SIG contributions around [packaging][6] and [kernel][7], a rewrite of our [branches policy][8] and a new section on communications, with details around our [channels][9] where the SIG can be reached and our [live streams][10].

As previously mentioned, we would very much welcome any feedback and [contributions][11] you might have for this documentation.

### systemd

The latest version in the Hyperscale SIG is systemd 251.4 for both CentOS Stream 8 and CentOS Stream 9. While the “hs+fb” version has been tagged and rolled out within Meta, we are still working on resolving issues with SELinux policies in the “hs” version before tagging and releasing it. In the meantime, the “hs” version is available on CBS for testing.

If you’re interested in learning more about how we roll out systemd in the Hyperscale SIG, we did a [talk][12] about it at the CentOS Dojo this past August. You can find out more about this and our other systemd-related conference activities this quarter in the conference recap linked below.

### Kernel

We have published a new build of the el8 kernel, which includes a [bugfix][13] for the perf package, which had previously been uninstallable.

### Container images

Our container build pipeline is now fully automated, and container images are built on the CentOS Open Shift CI/CD infrastructure and published weekly on Quay.

### Spin images

Neal has been working on image build descriptions for the Hyperscale Workstation, Cloud, and Vagrant images for CentOS Stream 9 using [KIWI][14]. In order to support that work, [we worked with the CentOS infrastructure to get support for using KIWI for building images deployed to CBS][15] and we’re now testing it. This is now live, though currently we cannot build release images through it due to issues with CBS assuming everything going out being RPM content.

### Package updates

We’ve published updated backports of `wireshark` (for CentOS Stream 8) and `fio` (for both CentOS Stream 8 and 9), based on the existing Fedora packaging. We’ve also updated the `ethtool` backport for CentOS Stream 9 to 5.16.

As part of the [ongoing work][16] to package QEMU in EPEL, we’ve started working on a Hyperscale backport to make it easier to iterate on this work. As a prerequisite, we’ve published updated backports of `meson`, `edk2` and `SLOF` in the Experimental repository. We’ve also requested to add `edk2` and `SLOF` to CRB and upstreamed a couple of build fixes to the Fedora QEMU packaging.

### DNF/RPM stack with CoW support

The [Copy-on-Write][17] stack was rebuilt on top of the latest upstream changes. We’ve also identified an incompatibility between CoW and some external packages from Microsoft that slightly deviate from the RPM specifications. As a result, we have improved our tooling robustness, and are engaging with Microsoft to get their packages fixed.

## Health and Activity

The SIG continues to maintain a healthy development pace.

### Meetings

The SIG holds regular [bi-weekly meetings][18] on Wednesdays at 16:00 UTC. Meetings are logged and the minutes for past meetings are [available][19].

The SIG uses the [`#centos-hyperscale`][20] IRC channel for ad-hoc communication and work coordination; this channel is also bridged on Matrix in the [`#centos-hyperscale:fedoraproject.org`][21] room. For async discussions and announcements we generally use the [centos-devel][22] mailing list. The SIG also holds open [monthly video conference sessions][23] to promote collaboration and social interaction.

### Conference talks

We’ve published a recap of our [conference activities][24] from the past few months on the [CentOS Blog][25]. As a reminder, we also have a page keeping track of our [conference presentations][26] with links to recordings and slides where available.

A number of SIG members are tentatively planning to attend [FOSDEM][27] in February 2023.

### Live streams

The SIG periodically does work live on Twitch from [its official Twitch channel][28]. Interested parties who want to watch and interact with us as we do work should follow us on Twitch to get notified for when we stream.

### Planned work

The SIG tracks pending work as issues on our [Pagure repository][29]. Notable projects currently in flight include:

- using CBS to build our spin images
- shipping an updated QEMU package in EPEL
- integrate btrfs transactional updates as an optional feature

## Issues for the Board

We have no issues to bring to the board’s attention at this time.

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/10/centos-hyperscale-sig-quarterly-report-for-2022q3/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[译者ID](https://github.com/译者ID)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://blog.centos.org/2022/07/centos-hyperscale-sig-quarterly-report-for-2022q2/
[2]: https://wiki.centos.org/SpecialInterestGroup/Hyperscale
[3]: https://wiki.centos.org/SpecialInterestGroup/Hyperscale#Membership
[4]: https://pagure.io/centos-sig-hyperscale/package-bugs
[5]: https://sigs.centos.org/hyperscale/
[6]: https://sigs.centos.org/hyperscale/contributing/packaging/
[7]: https://sigs.centos.org/hyperscale/contributing/kernel/
[8]: https://sigs.centos.org/hyperscale/policies/branches/
[9]: https://sigs.centos.org/hyperscale/communication/channels/
[10]: https://sigs.centos.org/hyperscale/communication/streams/
[11]: https://sigs.centos.org/hyperscale/internal/documentation/
[12]: https://www.youtube.com/watch?v=PdbyYqrvlnY
[13]: https://pagure.io/centos-sig-hyperscale/package-bugs/issue/18
[14]: https://osinside.github.io/kiwi/
[15]: https://pagure.io/centos-infra/issue/696
[16]: https://pagure.io/centos-sig-hyperscale/sig/issue/67
[17]: https://fedoraproject.org/wiki/Changes/RPMCoW
[18]: https://www.centos.org/community/calendar/#hyperscale-sig
[19]: https://sigs.centos.org/hyperscale/internal/meetings/
[20]: https://wiki.centos.org/irc#A.23centos-hyperscale
[21]: https://matrix.to/#/#centos-hyperscale:fedoraproject.org
[22]: https://lists.centos.org/mailman/listinfo/centos-devel
[23]: https://www.centos.org/community/calendar/#hyperscale-sig-monthly-hangout
[24]: https://blog.centos.org/2022/09/centos-hyperscale-sig-conference-recap/
[25]: https://blog.centos.org
[26]: https://sigs.centos.org/hyperscale/communication/talks/
[27]: https://fosdem.org/2023/
[28]: https://www.twitch.tv/centoshyperscale
[29]: https://pagure.io/centos-sig-hyperscale/sig/issues
