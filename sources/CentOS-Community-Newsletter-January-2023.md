[#]: subject: "CentOS Community Newsletter, January 2023"
[#]: via: "https://blog.centos.org/2023/01/centos-community-newsletter-january-2023/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: " "
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CentOS Community Newsletter, January 2023
======

## CentOS Connect

![CentOS Connect][1]

[CentOS Connect][2] has been announced as a FOSDEM Fringe event. This free event takes place in Brussels on February 3, 2023, the day before FOSDEM. If you’re attending FOSDEM, join us at CentOS Connect to learn about CentOS and connect with the people who work on it.

## CentOS Hyperscale SIG Meeting

The CentOS Hyperscale SIG will be holding an in-person meetup on February 2nd, 2023 at the [DoubleTree Brussels City Center Hotel][3]. This is the same venue hosting CentOS Connect on February 3rd, and only a short walk from where FOSDEM will be held over the weekend. The meetup is open to everybody interested – you don’t have to be a member of the SIG to attend, and we’d welcome participation from anyone interested in this space.

The event will be held from 9am to 5pm in the Birch room at the DoubleTree hotel. While this is an in-person event, we will do our best to setup a conference bridge so that remote participants can attend and interact as well.

Please register at [https://www.eventbrite.com/e/centos-hyperscale-sig-meetup-connectfosdem-2023-tickets-505677965407][4] to help with the event planning.

## CentOS Web+Docs Working Day

CentOS will be hosting a web+docs working day on Monday, February 6th, 2023 at the [DoubleTree Brussels City Center Hotel][3]. It will be held in the Birch room from 9am to 5pm. Everybody is welcome to attend and help us work on a content plan for our web sites and documentation. We can set up a video call for remote participation if there is interest.

Please see the [web+docs day planning page][5] if you’re interested. If you plan to attend in-person, let us know on the planning page.

## SIG Reports

Each month, we publish a rotating selection of quarterly reports from our [Special Interest Groups][6]. This month includes reports from the Automotive, Hyperscale, Kmods, Alternate Images, and Virtualization SIGs.

### Automotive

The Automotive SIG has published their [report on the blog][7].

### Hyperscale

The Hyperscale SIG has published their [report on the blog][8].

### Kmods

This report covers work that happened since last report. The previous report can be found [here][9].

#### Purpose

Packaging and maintaining kernel modules for CentOS Stream and Enterprise Linux.

#### Membership Update

No SIG members have been added since last report. We welcome anybody that’s interested and willing to do work within the scope of the SIG to join and contribute.

#### Support for CentOS Stream 9 / EL9

The Kmods SIG provides packages for CentOS Stream 9 and EL9.

#### Support for CentOS Stream 8 / EL8

The Kmods SIG continues to provide packages for CentOS Stream 8 and EL8.

#### New Packages

See [Kmods SIG’s documentation][10] for lists of available packages. This documentation also provides further information, e.g. how to enable the Kmods SIG’s repositories.

Note that the kernel modules provided by the Kmods SIG are currently not signed with a private key. Hence it is required to disable Secure Boot to be able to use any of these kernel modules.

Please report any issues with these packages in the corresponding project on [gitlab.com/CentOS/kmods][11] or [here][12] in case the issue is not related to a particular package.

#### Recent Activities

There have been no notable recent activities. With all of the infrastructure (except the functionality to sign kernel modules) and automation set up, the decline in recent activities is expected.

#### Conference talks

A talk about the current status of the Kmods SIG and its used automation is scheduled for the [CentOS Connect][2] on February 3rd 2022 in Brussels, Belgium.

#### Health and Activity

The Kmods SIG maintains a healthy development pace.

#### Communication

Regular meetings are scheduled monthly, in the first week, on Monday at 1600 UTC in #centos-meeting. Everyone is welcome to join!

You can also get in touch with SIG members at any time in #centos-kmods.

#### Open Issues

- **Signing kernel modules:** This requires collaboration and further discussion with Infra SIG. Especially about how to securely store a SIG specific key that can be used in CBS, but is not accessible by any unauthorized person.
- **Release packages for EL:** The SIG would like to provide release packages to allow users running RHEL, or one of its clones, to easily access packages provided by the SIG. The current state can be tracked [here][13] and is discussed on the centos-devel mailing list ([Link to archive][14]).

#### Issues for the Board

We have no issues to bring to the board’s attention at this time.

### Alternative Images

#### Purpose

To build and provide alternate iso images for CentOS Stream.

### Membership Update

No new SIG members have been added this quarter.

#### Images

No images have been created this quarter.

#### Health and Activity

The Alternative Images SIG is fairly healthy. We are still setting everything up and finding out what everyone wants.

- https://wiki.centos.org/SpecialInterestGroup/AltImages
- https://sigs.centos.org/altimages/
- https://pagure.io/centos-sig-alt-images/sig

- Livecd
- Kiwi
- Image Builder

- We have finalized the meeting date and time, which is currently weekly.
- We have setup the wiki, CentOS Documentation, and pagure git repos
- We have established that we want to use the following image buildering services in cbs
- We have tickets open with CentOS Infrastructure for the setup of those services and are working with them in getting them setup.
- We are working on getting configurations setup in anticipation of those services coming online.

#### Issues for the Board

We have no issues to bring to the board’s attention at this time.

### Virtualization

- On the oVirt side, CentOS Virt SIG now ships also oVirt Engine for CentOS Stream 9. Upstream released version 4.5.3 which is the one currently built within the SIG.
- Upstream community has been [updated about Red Hat involvement in the project][15]. This also applies to the Red Hat involvement for oVirt within the CentOS Virt SIG.

--------------------------------------------------------------------------------

via: https://blog.centos.org/2023/01/centos-community-newsletter-january-2023/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[译者ID](https://github.com/译者ID)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://connect.centos.org/connect-card-c10.png
[2]: https://connect.centos.org/
[3]: https://www.hilton.com/en/hotels/brudtdi-doubletree-brussels-city/
[4]: https://www.eventbrite.com/e/centos-hyperscale-sig-meetup-connectfosdem-2023-tickets-505677965407
[5]: https://gitlab.com/CentOS/promo/centos-events/-/issues/2
[6]: https://blog.centos.org/2022/07/centos-hyperscale-sig-quarterly-report-for-2022q2/
[7]: https://blog.centos.org/2023/01/quarterly-report-centos-automotive-sig/
[8]: https://blog.centos.org/2023/01/centos-hyperscale-sig-quarterly-report-for-2022q4/
[9]: https://blog.centos.org/2022/10/centos-community-newsletter-october-2022/
[10]: https://sigs.centos.org/kmods/
[11]: https://gitlab.com/CentOS/kmods
[12]: https://gitlab.com/CentOS/kmods/sig
[13]: https://pagure.io/centos-infra/issue/643
[14]: https://lists.centos.org/pipermail/centos-devel/2022-December/120755.html
[15]: https://lists.ovirt.org/archives/list/users@ovirt.org/thread/HEKKBM6MZEKBEAXTJT45N5BZT72VI67T/
