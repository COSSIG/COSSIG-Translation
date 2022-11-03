[#]: subject: "CentOS Community Newsletter, October 2022"
[#]: via: "https://blog.centos.org/2022/10/centos-community-newsletter-october-2022/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: " "
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CentOS Community Newsletter, October 2022
======

## Project News

### Modularity in EPEL 8

The EPEL team is [retiring package modularity][1] in EPEL 8. Modules were introduced in RHEL 8, but have since been phased out. They were never supported in EPEL 9.

### Keylime Changes

The Keylime team has announced th new versions of `keylime` and `keylime-agent-rust` will [include major changes in their configuration files][2]. These changes are intended to ease future upgrades and to make the TLS setup more consistent.

## SIG Reports

Each month, we publish a rotating selection of quarterly reports from our [Special Interest Groups][3]. This month includes reports from the Automotive, Hyperscale, and Kmods SIGs.

### Automotive SIG

The AutomotivE SIG has posted their quarterly report [on the mailing list][4].

### Hyperscale SIG

The Hyperscale SIG has posted their quarterly report [on the CentOS blog][5].

### Kmods SIG

This report covers work that happened since last report. The previous report can be found [here][6].

#### Purpose

Packaging and maintaining kernel modules for CentOS Stream and Enterprise Linux.

#### Membership Update

No SIG members have been added since last report. We welcome anybody that’s interested and willing to do work within the scope of the SIG to join and contribute.

#### Support for CentOS Stream 9 / EL9

The Kmods SIG provides packages for CentOS Stream 9 and EL9.

#### Support for CentOS Stream 8 / EL8

The Kmods SIG continues to provide packages for CentOS Stream 8 and EL8.

#### New Packages

See [Kmods SIG’s documentation][7] for lists of available packages. This documentation also provides further information, e.g. how to enable the Kmods SIG’s repositories.

Note that the kernel modules provided by the Kmods SIG are currently not signed with a private key. Hence it is required to disable Secure Boot to be able to use any of these kernel modules.

Please report any issues with these packages in the corresponding project on [gitlab.com/CentOS/kmods][8] or [here][9] in case the issue is not related to a particular package.

#### Recent Activities

The Kmods SIG has moved all of its resources to [gitlab.com/CentOS/kmods][8]. This includes all tooling to automatically detect required kernel module rebuilds due to kABI changes. We rely on GitLab CI for these kind of tasks.

Thanks to work done by the CentOS Infrastructure team there is now automatically created a Driver Disk for any kernel module released by the Kmods, or any other, SIG.

#### Health and Activity

The Kmods SIG maintains a healthy development pace.

#### Communication

Regular meetings are scheduled monthly, in the first week, on Monday at 1600 UTC in #centos-meeting. Everyone is welcome to join!

You can also get in touch with SIG members at any time in #centos-kmods.

#### Open Issues

- Signing kernel modules: This requires collaboration and further discussion with Infra SIG. Especially about how to securely store a SIG specific key that can be used in CBS, but is not accessible by any unauthorized person.
- Release packages for EL: The SIG would like to provide release packages to allow users running RHEL, or one of its clones, to easily access packages provided by the SIG. The current state can be tracked [here][10].

#### Issues for the Board

We have no new issues to bring to the board’s attention at this time.

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/10/centos-community-newsletter-october-2022/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[译者ID](https://github.com/译者ID)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://lists.centos.org/pipermail/centos-devel/2022-September/120610.html
[2]: https://lists.centos.org/pipermail/centos-devel/2022-September/120609.html
[3]: https://blog.centos.org/2022/07/centos-hyperscale-sig-quarterly-report-for-2022q2/
[4]: https://lists.centos.org/pipermail/centos-devel/2022-September/120617.html
[5]: https://blog.centos.org/2022/10/centos-hyperscale-sig-quarterly-report-for-2022q3/
[6]: https://blog.centos.org/2022/07/centos-community-newsletter-july-2022/
[7]: https://sigs.centos.org/kmods/
[8]: https://gitlab.com/CentOS/kmods
[9]: https://gitlab.com/CentOS/kmods/sig
[10]: https://pagure.io/centos-infra/issue/643
