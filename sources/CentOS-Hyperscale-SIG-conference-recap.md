[#]: subject: "CentOS Hyperscale SIG conference recap"
[#]: via: "https://blog.centos.org/2022/09/centos-hyperscale-sig-conference-recap/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: "turbokernel"
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CentOS Hyperscale SIG conference recap
======

In the past couple of months members of the CentOS Hyperscale SIG attended several conferences where they were able to share the work the SIG is doing and meet up in person, in some cases for the first time.

We have a page tracking [conference presentations][1] around Hyperscale-related topics. You can find references there to all talks mentioned below, including video recordings where available.

Conferences aren’t just about presentations though. The “hallway track” provides a great opportunity for serendipidous connection, and the various social events are often a great venue for folks to mingle and get to know each other in an informal setting.

If you’d like to meet us in person at a future event please [reach out][2]. We also generally cover conferences we plan to attend in our [quarterly reports][3].

## SCaLE 19x

Anita Zhang, Davide Cavalca, and Neal Gompa attended [SCaLE 19x][4] in Los Angeles at the end of July.

Anita presented two systemd-related talks: [The Curious Case of Memory Growth][5] which walks through debugging a regression in the Journal and – together with Alvaro Leiva Geisse – [Journey into the heart of systemd][6], providing a practical introduction to systemd and its abilities.

Davide presented [Building the future with CentOS Stream][7], covering the evolution of CentOS throughout the years and Meta’s learned experience engaging with the community.

Conferences videos for SCaLE have not been published yet, but recordings of the livestream feeds are available on [YouTube][8], and linked from our [tracking page][9] as well.

## CentOS Dojo and DevConf.US 2022

In August, Anita, Davide, David Duncan, Jack Aboutboul, Neal, and Quentin Deslandes attended [DevConf.US 2022][10] and the co-located [CentOS Dojo][11] event.

Joined remotely by Daan De Meyer, Anita talked at Dojo about managing and automating systemd releases within the Hyperscale SIG in [Adventures with systemd in Hyperscale][12]. At the same event, Davide presented another [Hyperscale SIG update][13] covering the latest developments.

Also at Dojo, Neal talked about [Making custom CentOS images with KIWI][14], which featured a live demo and [a repository of example KIWI image build data files][15]. Later in the week, Neal expanded on the subject of image building at his [Golden Images for Scaling Up with the Best of Them][16] talk during DevConf.US.

Shaun McChance also posted a [report][17] of this event on behalf of the [Promo SIG][18].

## Hyperscale face-to-face meetup

The day before Dojo, we also hosted the first face-to-face [Hyperscale SIG meetup][19]. Anita, Davide, David, Neal, and Quentin participated in person, joined by Shaun, who had helped organize the event. While this was primarily meant as an in-person event, we had a conference bridge setup to allow remote folks to join, which allowed people to follow the conversation and drop in and out as their scheduled allowed. Among others, Daan and Manu Bretelle participated in the event remotely this way.

We had a lot of great conversation at the meetup, covering specific work items, general brainstorming for future work and potential process improvements. Everybody agreed that the event was really useful and we will definitely try to organize more of these in the future.

The meetup wasn’t recorded, but there are [notes][20] of the discussion, and the various work items that were brought up will soon be reflected in tickets on our [SIG tracker][21].

## Linux Plumbers Conference 2022

Anita, Davide, Daan, Manu, and Quentin attended [Linux Plumbers Conference 2022][22] in Dublin in September. This was a hybrid event, also allowing Michel Salim and Neal to attend remotely.

Anita organized the [Service Management and systemd][23] micro-conference, featuring day-long presentations and discussions around systemd. Daan presented there his latest work on Journal optimization in [Slimming down the journal][24].

The conference also featured several Birds-of-a-Feather sessions to facilitate topic-specific discussion. Among others, SIG members participated in the [systemd BoF][25] and the [Btrfs BoF][26].

Conferences videos for LPC have not been published yet, but recordings of the livestream feeds are available on [YouTube][27], and linked from our [tracking page][28] as well.

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/09/centos-hyperscale-sig-conference-recap/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[turbokernel](https://github.com/turbokernel)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://sigs.centos.org/hyperscale/communication/talks/
[2]: https://sigs.centos.org/hyperscale/communication/channels/
[3]: https://sigs.centos.org/hyperscale/communication/reports/
[4]: https://www.socallinuxexpo.org/scale/19x
[5]: https://www.socallinuxexpo.org/scale/19x/presentations/curious-case-memory-growth
[6]: https://www.socallinuxexpo.org/scale/19x/presentations/journey-heart-systemd
[7]: https://www.socallinuxexpo.org/scale/19x/presentations/building-future-centos-stream
[8]: https://www.youtube.com/user/socallinuxexpo/videos
[9]: https://www.devconf.info/us/
[10]: https://wiki.centos.org/Events/Dojo/DevConfUS2022
[11]: https://www.youtube.com/watch?v=PdbyYqrvlnY
[12]: https://www.youtube.com/watch?v=aXO0eLMkCDI
[13]: https://www.youtube.com/watch?v=RKeFR4R2IeA
[14]: https://pagure.io/centos-kiwi-examples
[15]: https://devconfus2022.sched.com/event/14TEW/golden-images-for-scaling-up-with-the-best-of-them
[16]: https://lists.centos.org/pipermail/centos-promo/2022-September/007298.html
[17]: https://wiki.centos.org/SpecialInterestGroup/Promo
[18]: https://lists.centos.org/pipermail/centos-devel/2022-July/120462.html
[19]: https://pagure.io/centos-sig-hyperscale/sig/blob/main/f/meetups/20220816-boston-meetup.md
[20]: https://pagure.io/centos-sig-hyperscale/sig/issues
[21]: https://lpc.events/event/16/
[22]: https://lpc.events/event/16/sessions/146/
[23]: https://lpc.events/event/16/contributions/1185/
[24]: https://lpc.events/event/16/contributions/1399/
[25]: https://lpc.events/event/16/contributions/1300/
[26]: https://www.youtube.com/c/LinuxPlumbersConference/videos
