[#]: subject: "CentOS Community Newsletter, September 2022"
[#]: via: "https://blog.centos.org/2022/09/centos-community-newsletter-september-2022/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: " "
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CentOS Community Newsletter, September 2022
======

## Project News

### Tru Stepping Down

Tru Huynh has decided to step down from the Board of Directors. We thank him for his many years of hard work on the Board and across the entire CentOS project.

### Jefro Stepping Up

The CentOS Board has appointed Jeffrey “Jefro” Osier-Mixon to fill the vacancy. Jefro has been instrumental in developing the [Automotive SIG][1].

### Dojo @ DevConf

CentOS hosted a [Dojo][2] in Boston at [DevConf.US][3]. This free mini-conference featured nine talks on a variety of subjects from the Enterprise Linux ecosystem. We also live streamed and took questions from remote participants, which is something we plan to continue for future in-person events. The [recordings are available][4] on YouTube.

## SIG Reports

Each month, we publish a rotating selection of quarterly reports from our [Special Interest Groups][5]. This month includes reports from the Artwork and Virtualization SIGs.

### [Artwork SIG][5a]

#### Purpose

The CentOS Artwork SIG exists to produce the CentOS Project visual identity. See https://wiki.centos.org/SpecialInterestGroup/Artwork

#### Membership Update

There is not membership changes. We are always looking for new members.

#### Releases

##### CentOS Brand v2

![The CentOS Logo][6]

The CentOS Brand v2 is the new visual identity of the CentOS Project. We encorage you to use it abundantly. It was [recently approved][7], and is where we will be transitioning to.

The source files related to CentOS Brand v2 are publicly available at [centos-brand][8] repository, which purpose is to:

1. Consolidate devlopment of CentOS Brand design, usage, and presentation.
2. Consolidate automation jobs for rendering the CentOS Brand consistently (e.g., through GitLab pipelines, that you could include on your own projects).

The CentOS Brand is released under the terms of _[Creative Commons Attribution-ShareAlike 4.0 International Public License][9]_, and usage limited by _[CentOS Trademark Guidelines][10]_.

The previous brand, CentOS Brand v1, is still ative and will stand so under the term “CentOS Classic” instead of just “CentOS”.

#### Healthy and Activity

##### Health

We are here; doing what we can, when we can.

##### Recent activities related to website redesign

![][11]

The design of CentOS websites happens at [jekyll-theme-centos][12] repository, a [gem-based theme][13] for [Jekyll][14]. When a design change enters the theme, it can be [reviewed][15] immediatly to make corrections. The theme is available as open source under the terms of the [MIT License][16]. This section describes changes we are introducing into [jekyll-theme-centos][12]. Keep in mind these changes are not final.

###### Toolkit

We are moving jekyll-theme-centos development from Bootstrap 4 to Bootstrap 5. The number of custom CSS classes added on top of Bootstrap’s default ones is being reduced to make transition from one version to another easier in the future. As consequence, the HTML is also being rewritten to support Bootstrap-only classes and retire all those which aren’t. Though, there may be few exceptions still.

###### Typography

Montserrat and Overpass continue being the two typographies used in the website.

###### CentOS Brand Scalability

Presenting the CentOS Brand consistenly in different visual manifestations is high priority for the Artwork SIG. We are changing the file format from PNG to SVG to address rastered image quality degradation when the CentOS Brand is presented on very high resolution monitors. The [SVG support][17] seems to be pretty good in modern browsers.

###### Legibility on headers and footers

We are retiring the artistic motif background from website header and footers in favor of a plain color instead. The plain color at the moment is the same color used in CentOS Brand, to establish the visual connection with it. Footers and navbars backgrounds use a darker color to provide enough contrast with headers.

Before:

![][18]

After:

![][19]

The artistic motif is still relevant to reinforce the visual connection between different visual manifestations. So, it is still present in the home page, using CentOS Distribution screenshots.

###### CentOS Distribution

We are adding a carousel of screenshots related to CentOS Distributions. This has two purposes. One, connecting the CentOS Brand with the artistic motif used by default in the CentOS Stream distribution. Second, showing the world what CentOS Stream looks like with images, not just text.

![][20]

###### News, events and blog posts

We are replacing a home page title, from “Around CentOS” to “Blog posts”. The position of these sections is being aligned horizontally instead of vertically.

![][21]

###### CentOS Sponsors

The sponsors presentation occurs one-image-at-a-time, every few seconds. We are exploring a two rolling rows of 6 images each at the end of the home page, where the sponsors logo is randomly loaded from the entire list of active sponsors. In this layout, 12 sponsors will be always visible at once, in a reasonable amount of space, attractively. Hopefully, another set of 12 sponsors will be visible, the next time the home page is reladed, and so on.

![][22]

The images used in the screenshot are marely for testing purpose, they **don’t represent real sponsors in any way**. Once the gem-based theme is installed, the sponsor images stored in the theme are ignored and the images stored in `assets/img/sponsors/` directory are used instead.

The “becoming a sponsor” link is more visible now.

![][23]

We are retireing the sponsor section from the website footers in favor of the sponsor section in the website home page. Sites like mailling lists that need a sponsor image on footer, will continue using it.

##### Issues for the Board

None.

### Virtualization SIG

In the last quarter upstream had a few releases with binaries now mostly shipped via CentOS Virt SIG:

- [oVirt 4.5.2][24]
- [oVirt 4.5.1][25]
- [oVirt 4.5.0][26]

We are now building kata-containers for c9s as well, with the latest release (2.5.0) already available.

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/09/centos-community-newsletter-september-2022/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[译者ID](https://github.com/译者ID)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://wiki.centos.org/SpecialInterestGroup/Automotive
[2]: https://wiki.centos.org/Events/Dojo/DevConfUS2022
[3]: https://www.devconf.info/us/
[4]: https://www.youtube.com/watch?v=5usWZhLnJyA&list=PLuRtbOXpVDjDP1RLkzZmLbp699cCBnn47
[5]: https://blog.centos.org/2022/07/centos-hyperscale-sig-quarterly-report-for-2022q2/
[5a]: https://wiki.centos.org/SpecialInterestGroup/Artwork
[6]: https://gitlab.com/areguera/centos-brand/-/raw/v2/Sources/centos-logo.svg
[7]: https://git.centos.org/centos/board/issue/4#comment-612
[8]: https://gitlab.com/areguera/centos-brand/
[9]: https://creativecommons.org/licenses/by-sa/4.0/legalcode
[10]: https://www.centos.org/legal/trademarks/
[11]: https://i.imgur.com/RRPGRK4.png
[12]: https://gitlab.com/areguera/jekyll-theme-centos/-/tree/migration-to-bootstrap-v5
[13]: https://rubygems.org/gems/jekyll-theme-centos
[14]: https://jekyllrb.com/
[15]: https://areguera.gitlab.io/jekyll-theme-centos/
[16]: https://opensource.org/licenses/MIT
[17]: https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types#svg_scalable_vector_graphics
[18]: https://i.imgur.com/jrK4dk1.jpg
[19]: https://i.imgur.com/bQz4828.png
[20]: https://i.imgur.com/J7CWrPo.jpg
[21]: https://i.imgur.com/ydK4Eb2.jpg
[22]: https://i.imgur.com/ScXzGVw.png
[23]: https://i.imgur.com/RqPVH9o.jpg
[24]: https://blogs.ovirt.org/2022/08/ovirt-4-5-2-is-now-generally-available/
[25]: https://blogs.ovirt.org/2022/06/ovirt-4-5-1-is-now-generally-available/
[26]: https://blogs.ovirt.org/2022/04/ovirt-4-5-0-is-now-generally-available/