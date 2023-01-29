[#]: subject: "CentOS Hyperscale SIG Quarterly Report for 2022Q4"
[#]: via: "https://blog.centos.org/2023/01/centos-hyperscale-sig-quarterly-report-for-2022q4"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: " "
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CentOS Hyperscale SIG Quarterly Report for 2022Q4
======

This report covers work that happened between October 1st 2022 and January 8th 2023. For previous work, see the[2022Q3 report][1].

## Purpose

The[Hyperscale SIG][2]focuses on enabling CentOS Stream deployment on large-scale infrastructures and facilitating collaboration on packages and tooling.

## Membership update

Since the last update, the SIG gained one new member (Jun Wang).

We welcome anybody that’s interested and willing to do work within the scope of the SIG to join and contribute. See the[membership][3]section on the wiki for the current members list and how to join.

## Releases and Packages

Unless otherwise specified, packages are available in our main repository, which can be enabled with`dnf install centos-hyperscale-release`. Please report any issues with these packages on our[package-bugs][4]tracker.

### Documentation

We have continued streamlining our[user documentation][5]website and keeping its content up to date.

As previously mentioned, we would very much welcome any feedback and[contributions][6]you might have for this documentation.

### systemd

The latest version in the Hyperscale SIG is systemd 251.4 for both CentOS Stream 8 and CentOS Stream 9. We are still working on updating the SELinux policy for the Hyperscale build and would not recommend updating to systemd 251.4 if you need to enable SELinux.

We’re currently working on releasing systemd 252.4.

### Kernel

The latest version in the Hyperscale SIG is 5.14.0-76.hs1.hsx for both CentOS Stream 8 and CentOS Stream 9. We are working on a rebase to the latest CentOS Stream 9 kernel and incorporate support for building it for CentOS Stream 8 too.

### Container images

Our container build pipeline is fully automated, and[container images][7]are built on the CentOS OpenShift CI/CD infrastructure and published weekly on[Quay][8].

We provide both CentOS Stream 8 and CentOS Stream 9 variants at`quay.io/centoshyperscale/centos`.

### Spin images

We have worked with[CPE][9]to enable the ability to use[KIWI][10]to build operating system images through CBS. This is now enabled in CBS for Hyperscale. During efforts to produce images through CBS, we discovered[Koji doesn’t import environment groups][11]. We’re working on working around this issue in our image descriptions while we wait for this to be fixed.

The remaining task is to figure out how the release pipeline is supposed to work from CBS to the mirrors.

### Package updates

We have published new backports of`zsh`5.9,`fish`3.5.1,`iperf3`3.11 and`dmidecode`3.4 for CentOS Stream 8 and CentOS Stream 9 based on the packaging in Fedora. Our existing`fio`backport has been updated to 3.32, and on CentOS Stream 8 we have also updated`dwarves`to 1.24, bringing it in line with the version present in CentOS Stream 9 upstream.

The`kpatch`build in Hyperscale has been updated to 0.9.7, integrating a number of upstream improvements and improved support for clang PGO optimizations.

We also now provide a backport of`linuxptp`based off a recent git snapshot. This build also includes a number of patches developed at Meta for hardware support that are in the process of being upstreamed.

In the experimental repo, we now provide a backport of`snapper`0.10 based on the Fedora packaging.

On the development front, our CI pipeline to[detect package updates][12]in upstream CentOS that would supersede our versions and alert us has received a number of reliability improvements and bug fixes, and is now tracking CentOS Stream 9 as well in parallel with CentOS Stream 8.

### DNF/RPM stack with CoW support

The[Copy-on-Write][13]stack was rebuilt on top of the latest packaging changes in upstream CentOS, and we added support for disabling select RPMs from using RPM CoW. The compatiblity issue we had reported with some external packages has been root caused and reported, and we have implemented a workaround on our end to prevent conversion issues with non-compliant signature headers.

We’re in the process of reworking the CoW patchset to address the latest[upstream feedback][14]; once the discussion has settled we will publish an updated version.

## Health and Activity

The SIG continues to maintain a healthy development pace.

### Meetings

The SIG holds regular[bi-weekly meetings][15]on Wednesdays at 16:00 UTC. Meetings are logged and the minutes for past meetings are[available][16].

The SIG uses the[`#centos-hyperscale`][17]IRC channel for ad-hoc communication and work coordination; this channel is also bridged on Matrix in the[`#centos-hyperscale:fedoraproject.org`][18]room. For async discussions and announcements we generally use the[centos-devel][19]mailing list. The SIG also holds open[monthly video conference sessions][20]to promote collaboration and social interaction.

The SIG will hold an[in-person meetup][21]in Brussels, Belgium on February 2nd, the day before[CentOS Connect at FOSDEM][22]. A number of SIG members will be present in person, and we will have a conference bridge setup for remote participants as well. Everyone is welcome to attend, see the[event page][23]for details and to RSVP.

### Conference talks

Davide Cavalca will be presenting an update on the SIG activities at[CentOS Connect at FOSDEM][22]in February 2023. Several SIG members plan to attend Connect and[FOSDEM][24]in person. We also plan to have a presence at[SCALE 20x][25]in March 2023.

As a reminder, we have a page keeping track of our[conference presentations][26]with links to recordings and slides where available.

### Live streams

The SIG periodically does work live on Twitch from[its official Twitch channel][27]. Interested parties who want to watch and interact with us as we do work should follow us on Twitch to get notified for when we stream.

### Planned work

The SIG tracks pending work as issues on our[Pagure repository][28]. Notable projects currently in flight include:

- migrate to the new OpenShift instance
- using CBS to build our spin images
- shipping an updated QEMU package in EPEL
- integrate btrfs transactional updates as an optional feature

## Issues for the Board

We have no issues to bring to the board’s attention at this time.

--------------------------------------------------------------------------------

via: https://blog.centos.org/2023/01/centos-hyperscale-sig-quarterly-report-for-2022q4

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[译者ID](https://github.com/译者ID)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://blog.centos.org/2022/10/centos-hyperscale-sig-quarterly-report-for-2022q3/
[2]: https://wiki.centos.org/SpecialInterestGroup/Hyperscale
[3]: https://wiki.centos.org/SpecialInterestGroup/Hyperscale#Membership
[4]: https://pagure.io/centos-sig-hyperscale/package-bugs
[5]: https://sigs.centos.org/hyperscale/
[6]: https://sigs.centos.org/hyperscale/internal/documentation/
[7]: https://sigs.centos.org/hyperscale/content/containers/
[8]: https://quay.io/centoshyperscale/centos
[9]: https://docs.fedoraproject.org/en-US/cpe/
[10]: https://osinside.github.io/kiwi/
[11]: https://pagure.io/koji/issue/3626
[12]: https://pagure.io/centos-sig-hyperscale/package-updates
[13]: https://fedoraproject.org/wiki/Changes/RPMCoW
[14]: https://github.com/rpm-software-management/rpm/discussions/2057
[15]: https://www.centos.org/community/calendar/#hyperscale-sig
[16]: https://sigs.centos.org/hyperscale/internal/meetings/
[17]: https://wiki.centos.org/irc#A.23centos-hyperscale
[18]: https://matrix.to/#/#centos-hyperscale:fedoraproject.org
[19]: https://lists.centos.org/mailman/listinfo/centos-devel
[20]: https://www.centos.org/community/calendar/#hyperscale-sig-monthly-hangout
[21]: https://discussion.fedoraproject.org/t/centos-hyperscale-sig-meetup-connect-fosdem-2023/45558
[22]: https://connect.centos.org/
[23]: https://www.eventbrite.com/e/centos-hyperscale-sig-meetup-connectfosdem-2023-tickets-505677965407
[24]: https://fosdem.org/2023/
[25]: https://www.socallinuxexpo.org/scale/20x
[26]: https://sigs.centos.org/hyperscale/communication/talks/
[27]: https://www.twitch.tv/centoshyperscale
[28]: https://pagure.io/centos-sig-hyperscale/sig/issues
