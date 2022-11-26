[#]: subject: "November 2022 Newsletter"
[#]: via: "https://blog.centos.org/2022/11/centos-community-newsletter-november-2022/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "Northurland"
[#]: translator: ""
[#]: reviewer: ""
[#]: publisher: ""
[#]: url: ""

November 2022 Newsletter
======

## Project News

![CentOS Connect][13]

[CentOS Connect][1] has been announced as a FOSDEM Fringe event. This free event takes place in Brussels on February 3, 2023, the day before FOSDEM. If you’re attending FOSDEM, join us at CentOS Connect to learn about CentOS and connect with the people who work on it.

### Alternate Images SIG

The [Alternate Images SIG][2] has officially been launched to provide additional operating system images, such as live media and alternate installations. Their [meetings][3] happen weekly on Thursdays at 1900 UTC in the #centos-meeting IRC channel.

### OKD Streams

The [OKD][4] project has [announced OKD Streams][5], stable OKD builds on the newly introduced CentOS Stream CoreOS. OKD is the community distribution of Kubernetes that powers Red Hat OpenShift.

## SIG Reports

Each month, we publish a rotating selection of quarterly reports from our [Special Interest Groups][6]. This month includes reports from the Cloud, Promo, and Storage SIGs.

### [Cloud][7]

### Purpose

Packaging and maintaining different FOSS based Private cloud infrastructure applications that one can install and run natively on CentOS.

https://wiki.centos.org/SpecialInterestGroup/Cloud

### Membership update

Continue to aid OKD and SCOS in onboarding into the community. OKD maintainer Christian Glombek will fill the vacant CloudSIG co-chair position.

Releases in the most recent quarter (or most recent release, if none in that quarter)

CloudSIG has published the RDO Zed release based on upstream OpenStack Zed. [8]

The OKD Working Group has published the first OKD/SCOS (OKD on CentOS Stream CoreOS) MVP release in collaboration with the CloudSIG. [9]

### Health and activity

The Cloud SIG remains fairly healthy. And is still looking for other projects to join to expand it’s audience.

### [Promo](https://wiki.centos.org/SpecialInterestGroup/Promo)

In August, we put on a [Dojo at DevConf.US][10]. This was our first return to in-person events. We also allowed virtual participation. The event went well overall, and has potential for future growth. Read the [full event report][11].

We have been working on planning [CentOS Connect at FOSDEM][1]. CentOS Connect is a rebranding of CentOS Dojos. In the past, our FOSDEM Dojos have been our largest by far. We are planning for 100 people for a single-day event. This is smaller and shorter than pre-pandemic events.

Finally, a [group from China][12] has formally joined the Promo SIG to work on regional and localized outreach and promotion. We’re excited about the work they’re already doing, and we hope this paves the way for more regional promotion activities down the line.

### [Storage](https://wiki.centos.org/SpecialInterestGroup/Storage)

Package updates since the last report:

 - Glusterfs 10 updated to glusterfs-10.3, packages are available for Stream 9 and Stream 8.
 - Glusterfs 9, updated to glusterfs-9.6, packages are available for Stream 9, Stream 8, and CentOS 7.
 - Ceph Quincy (17) updated to ceph-17.2.5, packages are available for Stream 9 and Stream 8.
 - Ceph Pacific (16) no update, however ceph-16.2.11 is likely coming soon.
 - Ceph Octopus (15), updated to ceph-15.2.17, packages are available for Stream 9, Stream 8, and CentOS 8. This is the final update to ceph-15, which has reached EOL upstream.
 - NFS-ganesha 4 and libntirpc 4, no updates, however nfs-ganesha-4.1 and libntirpc-4.1 updates are coming shortly.
 - Apache Arrow updated to libarrow-9.0.0 in Stream 9, No update to Stream 8.
 - Apache ORC no update to liborc.

--------------------------------------------------------------------------------
via: https://blog.centos.org/2022/11/centos-community-newsletter-november-2022/

作者：[CentOS Blog][a]
选题：[Northurland][b]
译者：[翻译者ID](https://github.com/翻译者ID)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org/
[b]: https://github.com/Northurland
[1]: https://connect.centos.org/
[2]: https://wiki.centos.org/SpecialInterestGroup/AltImages
[3]: https://www.centos.org/community/calendar/
[4]: https://www.okd.io/
[5]: https://www.okd.io/blog/2022-10-25-OKD-Streams-Building-the-Next-Generation-of-OKD-together/
[6]: https://blog.centos.org/2022/07/centos-hyperscale-sig-quarterly-report-for-2022q2/
[7]: https://wiki.centos.org/SpecialInterestGroup/Cloud
[8]: https://lists.centos.org/pipermail/centos-devel/2022-November/120679.html
[9]: https://cloud.redhat.com/blog/okd-streams-building-the-next-generation-of-okd-together
[10]: https://wiki.centos.org/Events/Dojo/DevConfUS2022
[11]: https://lists.centos.org/pipermail/centos-promo/2022-September/007298.html
[12]: https://www.cossig.org/
[13]: https://connect.centos.org/connect-card-c10.png