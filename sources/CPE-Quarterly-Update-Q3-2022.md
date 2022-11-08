[#]: subject: "CPE Quarterly Update Q3 2022"
[#]: via: "https://blog.centos.org/2022/10/cpe-quarterly-update-q3-2022/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: " "
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CPE Quarterly Update Q3 2022
======

This is a summary of the work done on initiatives by the [CPE][1] Team. Each quarter CPE Team together with CentOS and Fedora community representatives chooses initiatives that will be worked on in this quarter. The CPE Team is then split into multiple smaller sub-teams that will work on chosen initiatives + day to day work that needs to be done.

This update is made from infographics and detailed updates. If you want to just see what’s new, check the infographics. If you want more details, continue reading. ![][2]

## About

The purpose of this sub-team is to take care of day-to-day business regarding CentOS and Fedora Infrastructure and Fedora release engineering work. It’s responsible for services running in Fedora and CentOS infrastructure and preparing things for the new Fedora release (mirrors, mass branching, new namespaces, etc.). This sub-team is also investigating possible initiatives. This is done by ARC (The Advance Reconnaissance Crew), which is formed from the Infra & Releng sub-team members based on the initiative that is being investigated.

**Issue trackers**

- [Fedora Infrastructure][3]
- [CentOS Infrastructure][4]
- [Fedora Release Engineering][5]

**Documentation**

- [Fedora Infrastructure][6]
- [CentOS Infrastructure][7]
- [Fedora Release Engineering][8]

## Members of sub-team

- Mark O’Brien (Team Lead) (mobrien)
- Kevin Fenzi (nirik)
- Fabian Arrotin (arrfab)
- Pedro Moura (pshmoura)
- Tomáš Hrčka (humaton)
- Anton Medvedev (amedvede)
- Michal Konečný (zlopez)
- Akashdeep Dhar (t0xic0der)
- Vipul Siddharth (siddhartvipul)

## Closed tickets

- CentOS Infrastructure - 112
- Fedora Infrastructure - 150
- Fedora RelEng - 185

## Mini-initiatives finished

- [Deploy/Configure new Duffy CI instance][9]
- [new mock and systemd-nspawn][10]
- [DNS Mini-initiative][11]

## Other tasks finished

- Mass update/reboots
- Mass rebuild for F37

## ARC Investigations completed

- [Update of kernel test app][12]

## About

This initiative is working on CentOS Stream/Emerging RHEL to make this new distribution a reality. The goal of this initiative is to maintain CentOS Stream and develop new features for it.

**Status:** In Progress

**Issue trackers**

- [Bugzilla][13]

**Documentation**

- [CentOS documentation][14]

**Application URLs**

- [https://centos.org/centos-stream/][15]

## Members of sub-team

- Brian Stinson (Team Lead) (bstinson)
- Adam Samalik (asamalik)
- James Antill (jantill)
- Johnny Hughes
- David Fan (dfan)
- Stephen Gallagher (sgallagher)
- Troy Dawson (tdawson)
- Adam Saleh (asaleh)

## About

FMN (FedMsg Notifications) is a project that allows people in our community to get notified when messages that interest them fire on the message bus, making the message bus more useful to people that are not directly developing or troubleshooting applications running in our infra.

The current solution has plenty of tech debt and this initiative will rewrite it from scratch addressing all the issues.

**Status:** In Progress

**Issue trackers**

- [Github project][16]

**Documentation**

- [Initiative proposal][17]
- [ARC investigation][18]
- [Documentation link][19]

**Application URLs**

- [FMN Service][20]

## Members of sub-team

- Aurelien Bompard (Team Lead) (abompard)
- Ryan Lerch (rlerch)
- Nils Philippsen (nils)
- James Richardson (jrichardson)

## About

CPE UX team is working on Graphic Design, User Experience, and User Interface for Fedora.

**Status:** In Progress

**Issue trackers**

- [Gitlab][21]

## Members of sub-team

- Jess Chitas
- Emma Kidney
- Gbenga Oti

## About

Extra Packages for Enterprise Linux (or EPEL) is a Fedora Special Interest Group that creates, maintains, and manages a high-quality set of additional packages for Enterprise Linux, including, but not limited to, Red Hat Enterprise Linux (RHEL), CentOS, and Scientific Linux (SL), Oracle Linux (OL).

EPEL packages are usually based on their Fedora counterparts and will never conflict with or replace packages in the base Enterprise Linux distributions. EPEL uses much of the same infrastructure as Fedora, including a build system, Bugzilla instance, updates manager, mirror manager, and more.

**Status:** In Progress

**Issue trackers**

- [Pagure][22]

**Documentation**

- [EPEL documentation][23]

## Members of sub-team

- Carl George (Team Lead) (carlwgeorge)
- Diego Herrera

## About

CPE has a dedicated sub-team working on the documentation in Fedora.

**Status:** In Progress

**Issue trackers**

- [Gitlab project][24]

**Application URLs**

- [Fedora documentation][25]

## Members of sub-team

- Petr Bokoc (pbokoc)

If you get here, thank you for reading this. If you want to contact us, feel free to do it in the #redhat-cpe channel on [libera.chat][26] or [matrix.org][27].

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/10/cpe-quarterly-update-q3-2022/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[RakerZh](https://github.com/RakerZh)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://docs.fedoraproject.org/en-US/cpe/
[2]: https://blog.centos.org/wp-content/uploads/2022/10/Q3_2022_infographics-scaled.jpg
[3]: https://pagure.io/fedora-infrastructure/issues
[4]: https://pagure.io/centos-infra/issues
[5]: https://pagure.io/releng/issues/
[6]: https://docs.fedoraproject.org/en-US/infra/
[7]: https://docs.infra.centos.org/
[8]: https://docs.pagure.org/releng/
[9]: https://pagure.io/centos-infra/issue/821
[10]: https://pagure.io/releng/issue/6967
[11]: https://pagure.io/fedora-infrastructure/issue/9852
[12]: https://pagure.io/cpe/initiatives-proposal/issue/22
[13]: https://bugzilla.redhat.com/buglist.cgi?version=CentOS%20Stream
[14]: https://docs.centos.org/en-US/docs/
[15]: https://centos.org/centos-stream/
[16]: https://github.com/orgs/fedora-infra/projects/13
[17]: https://pagure.io/cpe/initiatives-proposal/issue/10
[18]: https://fedora-arc.readthedocs.io/en/latest/fmn/index.html
[19]: https://fmn.readthedocs.io/en/latest/
[20]: https://apps.fedoraproject.org/notifications/
[21]: https://gitlab.com/groups/fedora/design/team/-/issues
[22]: https://pagure.io/epel/issues
[23]: https://docs.fedoraproject.org/en-US/epel/
[24]: https://gitlab.com/fedora/docs/docs-website/pages/-/issues
[25]: https://docs.fedoraproject.org/
[26]: https://libera.chat/
[27]: https://matrix.org/
