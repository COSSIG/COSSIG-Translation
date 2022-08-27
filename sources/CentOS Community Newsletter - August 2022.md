[#]: subject: "August 2022 Newsletter"
[#]: via: "https://blog.centos.org/2022/08/centos-community-newsletter-august-2022/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: " "
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

August 2022 Newsletter
======

# Project News

## Dojo at DevConf

CentOS hosted a [Dojo at DevConf.US][1] in Boston. This was our first return to hosting in-person events, and we tried to include remote participants with a YouTube live stream. Thanks to everybody who joined us in Boston or online. We appreciate feedback on how we can improve hybrid events. The recordings will be published soon.

## SIG Reports

Each month, we publish a rotating selection of quarterly reports from our [Special Interest Groups][2]. This month includes reports from the Cloud and Storage SIGs.

## [Cloud SIG][3]

### Purpose

Packaging and maintaining different FOSS based Private cloud infrastructure applications that one can install and run natively on CentOS.

[https://wiki.centos.org/SpecialInterestGroup/Cloud][3]

### Membership update

The OKD (OpenShift community edition) team contacted the Cloud SIG in order to know whether they could join our effort. Their contributors are looking for the best way to provide OKD along with SCOS (CentOS Stream CoreOS) images. As OKD and SCOS onboard into the community, it was suggested one of the contributors fill the vacant CloudSIG co-chair position.

### Releases in the most recent quarter

#### RDO

Yoga is still the [latest release][4]. RDO community is about to package the next release named “Zed” in a couple of weeks, which will be supported on CentOS Stream 9 only. As a reminder Yoga is used as a transitive Openstack release with CentOS Stream 8 and 9 support, in order to be able to migrate the OS from one to another.

### Health and activity

The Cloud SIG remains fairly healthy. However, it is still, for the most part, a monoculture containing only OpenStack.

## [Storage SIG][5]

Package updates since the last report:

- Glusterfs 10 updated to glusterfs-10.2, packages are available for Stream 9 and Stream 8.
- Glusterfs 9, no update to glusterfs-9.
- Ceph Quincy (17) updated to ceph-17.2.2, packages are available for Stream 9, Stream 8, and RHEL8.
- Ceph Pacific (16) updated to ceph-16.2.10, packages are available for Stream 9, Stream 8, and RHEL8.
- Ceph Octopus (15), no update to ceph-15.
- NFS-ganesha 4 and libntirpc 4, no updates.
- Apache Arrow updated to libarrow-8.0.1, packages are available for Stream 9, Stream 8.
- Apache ORC updated to liborc-1.7.5, packages are available for Stream 9, Stream 8.

Note: Dependencies for Ceph Quincy (17) and earlier that are not in CoreOS, CBR/PowerTools, or AppStream are provided by the Storage SIG. Starting with Ceph Reef (18) those dependencies will be provided by EPEL instead. This includes Apache Arrow (libarrow), Apache ORC (liborc), and a rather lengthy list of other packages. This will simplify building dependencies by only requiring that they be built in one place. Many developers and end users also tend to prefer EPEL, and enable EPEL by default, and this will reduce or outright eliminate conflicts between packages in EPEL and packages in the Storage SIG. And no, Ceph itself will not be in EPEL; it will remain solely in the Storage SIG.

Following are the updates for Samba:

- Samba 4.16, updated to latest version 4.16.3 on Stream 9 and Stream 8.
- Samba 4.15, updated till the latest version 4.15.8 on Stream 9 and Stream 8. RHEL8 builds are also available.
- Samba 4.14, in CVE fixes only mode.

Issues reported:

In the light of [user report][6] for a crash during Samba daemon start up efforts are underway to ensure that system installed versions of dependent libraries like libtalloc, litdb, libtevent and libldb does not interfere with corresponding copies internally within builds.

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/08/centos-community-newsletter-august-2022/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[译者ID](https://github.com/译者ID)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org/
[b]: https://github.com/lkxed
[1]: https://wiki.centos.org/Events/Dojo/DevConfUS2022
[2]: https://blog.centos.org/2022/07/centos-hyperscale-sig-quarterly-report-for-2022q2/
[3]: https://wiki.centos.org/SpecialInterestGroup/Cloud
[4]: https://blogs.rdoproject.org/2022/04/rdo-yoga-released/
[5]: https://wiki.centos.org/SpecialInterestGroup/Storage
[6]: https://lists.centos.org/pipermail/centos-devel/2022-June/120415.html
