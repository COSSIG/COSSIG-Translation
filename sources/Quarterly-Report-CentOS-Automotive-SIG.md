[#]: subject: "Quarterly Report – CentOS Automotive SIG"
[#]: via: "https://blog.centos.org/2023/01/quarterly-report-centos-automotive-sig/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: " "
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

Quarterly Report – CentOS Automotive SIG
======

## Membership update

The [CentOS Automotive SIG][1] does not have a formal membership process. The mailing list currently has 106 subscribers representing at least 32 organizations, though not all subscribers use corporate emails and some are participating as individuals.

Releases in the most recent quarter (or most recent release, if none in that quarter).

The Automotive SIG produces three types of artifacts:

- [AutoSD][2], a streaming distribution of CentOS designed for in-vehicle automotive use cases.
- An Automotive SIG RPM repository that allows the community to expand the content of AutoSD or experiment with some of its parts.
- Sample images, built using OSBuild, which provide examples of how to assemble production images based on AutoSD, customized for some hardware, including container images, based on CoreOS/ostree technologies.

**AutoSD**, or Automotive Stream Distribution, is a streaming distribution for automotive in-vehicle software development based on CentOS Stream. It is transparently the upstream project for [Red Hat's eventual in-vehicle OS product][3]. AutoSD has been downloaded and used by many organizations who have commented or asked for help, so we know it is getting some traction though of course we don't have exact metrics on usage.

In Q4 2022, we released a version of AutoSD compatible with the emerging SOAFEE specification. SOAFEE ([https://soafee.io][4]) is an initiative driven by Arm for the purpose of developing a reference specification for Arm-based software-defined vehicles (SDVs) consisting of an operating system, container orchestration strategy, and application layer. In addition, we introduced a very [lightweight container runtime][5] based on podman and systemd that does not include Kubernetes, as the latter represented a significant performance hit on all relevant hardware. We presented at the [Arm Developer Summit][6] in November on these topics.

In the coming quarter, we plan to tighten up documentation, begin a process for accepting  and supporting hardware enablement contributions, and continue to develop AutoSD toward the SOAFEE specification while also contributing to that specification within the SOAFEE community.

## Health report and general activity narrative

The SIG typically has [1 public meeting per month][7] with 25-40 attendees, with visible participation from 7-10 separate organizations. We have largely given up on a separate office hours meeting due to attendance.

This SIG is intended to be a community effort with contributions and shared benefits from all participants. All formal meetings are recorded and posted on this page: [https://wiki.centos.org/SpecialInterestGroup/Automotive/Meetings][7]

Several Red Hat employees made the initial contributions to the project as well as the infrastructure required to build and test it. We occupy a gitlab repository in the CentOS namespace building software regularly using CI, with build instructions provided on the documentation page at [https://sigs.centos.org/automotive/][2]. Sample images are present and downloadable along with customization and build instructions.

--------------------------------------------------------------------------------

via: https://blog.centos.org/2023/01/quarterly-report-centos-automotive-sig/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[译者ID](https://github.com/译者ID)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://wiki.centos.org/SpecialInterestGroup/Automotive
[2]: https://sigs.centos.org/automotive/
[3]: https://www.redhat.com/en/blog/new-standard-red-hat-vehicle-operating-system-modern-and-future-vehicles
[4]: https://soafee.io/
[5]: https://www.redhat.com/en/blog/running-containers-cars
[6]: https://devsummit.arm.com/
[7]: https://wiki.centos.org/SpecialInterestGroup/Automotive/Meetings

