---
name: cc-course-case_study
tags: cc, course-cc
---

:::info
**legal information**

(c) Holger Kienle

![](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/by-sa.svg =x40)  
Except where otherwise noted, this document's content is licensed under the [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) license.
Please attribute this document to Holger Kienle and link it with [https://hackmd.io/@hkienle/course-cc-final/](https://hackmd.io/@hkienle/course-cc-final/)

For **screenshots** made by the author:
- Making a screenshot is believed to be [fair use](https://psu.libanswers.com/faq/333836) (thus not violating any copyright that may exist in the depicted GUI).
- To remove doubt, if the screenshot depicts content by the author, this content is licensed under CC BY-SA 4.0 and the entire screenshot is licensed CC BA-SA 4.0.

**No endorsement by Creative Commons:** This case study has been performed in the *CC Certificate for Educators* course, but this does not mean in any sense that it is endorsement by or association with Creative Commons. This especially holds for the (ab)use of the CC heart logo.
:::

::: danger
**caveat**

I cannot give legal advice and I am not a lawyer anyways. What I can do is to make you aware of certain considerations about the intersection of intellectual property (IP), licenses, and technical artifacts. This case study is intended as a starting point to form your own opinions and conclusions.

Whenever you read a sentence discussing legal issues, you should prepend it with: As you know, the author is not a lawyer and only gives his opinion as a lay person **for entertainment purposes only**. Also, the specifics of the law will vary depending on the country, even on the [regional circuit](https://system.uslegal.com/us-courts-of-appeals/circuits/) in the US.

If this case study feels like a wild roller coaster, it is so because IP law is a wild roller coaster... Enjoy! :nerd_face:
:::

:::success
:bulb: [There is a GitHub repository with all assets and license information!](https://github.com/hkienle/cc-course-final)
:::

**CC Certificate for Educators - Fall 2022 - Final**
# a case study of licensing the 3D-printing workflow
[TOC]

## introduction

This case study looks at the workflow to produce a 3D artifact from its design to its physical instantiation with a 3D printer. The workflow produces several digital artifacts and in the end a physical artifact. The case study discusses intellectual property (IP) and licensing considerations for each artifact.

> ![](https://creativecommons.org/wp-content/uploads/2019/02/ccheart_black.png =x120)  
> *Starting point: CC heart logo*  
> [SVG image](https://creativecommons.org/about/downloads/) by Creative Commons, copyrighted, unlicensed, believed to be fair use as a subject of scholarly discussion.  
> Assumed to be a trademark by Creative Commons.

The starting point of the case study is the CC logo with a heart outline (2D).

> ![](https://i.imgur.com/U8yyVLk.png =x120)  
> Result: physical 3D object  
> Photo by Holger Kienle

At the end we will have produced a physical 3D object that can be used as a "badge/brooch" or function as a "rubber stamp".

### GitHub repository

All accompanying assets of this case study are available in the following GitHub repository: https://github.com/hkienle/cc-course-final

The motivation for doing so is that all assets of the project should be available in a self-contained repository that can be easily downloaded or cloned by others.

Since the repository is public with the intent to encourage remixing, it is important to license each file in the repository appropriately.

The **copyright and licensing information** for each relevant file is given in the repository's `README.md`: https://github.com/hkienle/cc-course-final/blob/main/README.md

### open and free

An important goal of the case study is to use [free and open-source software](https://en.wikipedia.org/wiki/Free_and_open-source_software) (FOSS) and to license all material with [free licenses](https://en.wikipedia.org/wiki/Free_license).

The following table gives an overview of the used software tools.
| FOSS | domain | FOSS license (SPDX) |
| -------- | -------- | -------- |
| Inkscape | vector graphics editor | GPL-3.0-or-later |
| FreeCAD | parametric 3D CAD modeler | LGPL-2.0-or-later |
| PrusaSlicer | 3D printer slicer | AGPL-3.0 |

For FOSS, not only the software, but typically the documentation is under a free license. For example, [FreeCAD is documented with a Wiki](https://wiki.freecadweb.org/) and the content is licensed under CC BY 3.0. This is very helpful when creating OER.

An aspect easily overlooked is that software should operate on [open file formats](https://en.wikipedia.org/wiki/Open_file_format), which are  defined by an openly published specification. Conversely, it is desirable to avoid [proprietary formats](https://en.wikipedia.org/wiki/Proprietary_file_format). This case study uses:
| format | domain | specification license |
| -------- | -------- | -------- |
| SVG     | vector images (2D) | [W3C Document License](http://www.w3.org/Consortium/Legal/copyright-documents) |
| STL | triangulated surfaces (3D objects) | [openly documented, but proprietary](https://www.loc.gov/preservation/digital/formats/fdd/fdd000504.shtml) (?)|
| g-code | machine control | openly documented, many variants
| markdown | documentation | several dialects, e.g., [CommonMark](https://spec.commonmark.org/) under CC BY-SA  |
| PNG | bitmap images (screenshots)| [W3C Software and Document Notice and License](https://www.w3.org/Consortium/Legal/2015/copyright-software-and-document)

Last but not least, the 3D printer that has been used is a Prusa MINI. It it is open source hardware (OSH) and documentation is available at its [GitHub repository](https://github.com/prusa3d/Original-Prusa-MINI). OSHWA has certified it with [UID CZ000002](https://certification.oshwa.org/cz000002.html).

:::success
**green boxes**

Writing in green boxes are used to discuss legal issues that are relevant for the case study.
:::


:::warning
**yellow boxes**

Writing in yellow boxes describe an artifact used or produced for the case study.
:::


:::danger
**red boxes**

Writing in red boxes ties to succinctly describe the legal situation and licensing of the case study's artifacts.
:::


## case study

We split the discussion into two parts, somewhat arbitrarily: We start with 2D, and then move on to 3D.

### 2D (SVG)

The first step in our workflow is to analyze the logo with the help of Inkscape. The logo is 2D and described with Scalable Vector Graphics (SVG). Inkscape can process SVG and its native file format is [SVG enhanced with Inkscape-specific meta data](https://inkscapetutorial.org/svg-file-format.html).


:::warning
**CC heart logo**

> ![](https://creativecommons.org/wp-content/uploads/2019/02/ccheart_black.png =x120)  
> *The CC heart logo (SVG file)*  
> [SVG image](https://creativecommons.org/about/downloads/) by Creative Commons, copyrighted, unlicensed, believed to be fair use as a subject of scholarly discussion.  
> Assumed to be a trademark by Creative Commons.

Our starting point, in the following called *heart logo*, has two graphical elements:
1. The heart shape, which forms the logo's outline.
2. The letters "cc", which are rendered in a specific font (CC Accidenz Commons).

The heart outline may be considered a *basic shape* -- part of the [suits of playing cards](https://en.wikipedia.org/wiki/Playing_card_suit), originating more than 500 years ago --, which is not protected by copyright.

> ![](https://upload.wikimedia.org/wikipedia/commons/7/7e/Heart_plot.svg =x150)  
> *Plot of a mathematical function that yields a heart symbol*  
> Screenshot by [Eviatar Bach](https://commons.wikimedia.org/wiki/File:Heart_plot.svg), placed in the public domain with CC Zero

(As a side note, it's fascinating that a heart shape can be defined with a mathematical function.)

The letter "c" itself is not under copyright and the particular shape of the "c" may be also not under copyright.
:::


:::success
**copyright and basic shapes**

There is no copyright of ideas (*idea-expression dichotomy*). There is no copyright of basic (abstract) shapes.
Generally, a work ["must have a minimum amount of creativity" to be under copyright](https://copyright.uslegal.com/enumerated-categories-of-copyrightable-works/creativity-requirement/).

(Before you get the idea that copyright might be sane after all: [4 minutes and 33 seconds of silence](https://ipkitten.blogspot.com/2012/04/price-of-silence-and-myth-of-batt-cage.html) may be under copyright protection.)

According to [Kattwinkel](https://www.owe.com/resources/legalities/legalities-15-is-a-shape-copyrightable-how-to-get-appropriate-rights-when-you-commission-graphic-design/), "no one can own exclusive copyright in a square, circle, oval, or diamond, or the common fleur de lis. Such shapes can be included as part of a more complex design, that as a whole is copyrighted".

While a simple rectangle and the abstract idea of a rectangle are not protected by copyright, depicting a rectangle in a distinctive and creative way probably yields copyright protection (e.g., the use of color-gradients and shadows may accomplish this). Generally, in copyright law ["the amount of creativity required is very little"](https://copyright.uslegal.com/enumerated-categories-of-copyrightable-works/creativity-requirement/).
:::


:::success
**trademark-copyright interaction**

The governing principle of trademark law is to prevent [likelihood of confusion](https://www.uspto.gov/trademarks/search/likelihood-confusion) by consumers. For logos, this means that if a logo has been claimed as a trademark by someone then someone else must not use this logo or a similar logo for their own (commercial) purpose.

The trademark of a logo and the copyright status of a logo exist independently of each other. Especially, [a trademark does not necessarily have copyright protection](https://www.schoenherr.eu/content/have-you-ever-wondered-whether-your-brand-is-a-copyright-protected-work/).

> ![](https://i.imgur.com/bcVA6nb.png =x100)  
> *A yellow rectangle on black background*  
> Copied and cropped from somewhere on the Internet, considered legal because basic shapes are not copyright protected.  
> Note that this has nothing to do with the National Geographic logo, any similarity would constitute a coincidence.

For example, a simple rectangle cannot be copyrighted, but a particular rectangle may be protected under trademark law (e.g., the [National Geographic](https://help.nationalgeographic.com/s/article/logo-use-and-trademark)) logo.

However, typically we can assume that a trademarked logo also enjoys copyright protection. Copyright applies automatically, whereas the trademark protection has be claimed (e.g., by applying "TM") and defended (e.g., with  having a track-record of using the mark and sending cease-and-desist letters).

Optionally, a trademark can be registered with the US Patent and Trademark Office. It is then recorded in a database (TESS) and it can be marked with ":registered:".

A trademark can have a *trademark policy* that governs the use of the trademark. A trademark policy is necessary if the trademark owner wants to allow third-parties to use it under certain conditions.
:::


:::success
**copyright and fonts**

A font, or typeface, has two separate concepts:
1.  The individual shapes of the letters -- or rather, more generally speaking: the [glyphs](https://en.wikipedia.org/wiki/Glyph) --  that make up the font.
2.  The digital encoding of a font with the help of a [font file](https://en.wikipedia.org/wiki/Computer_font).

It seems that fonts is an area of copyright law that can differ significantly on the jurisdiction. In the US, according to [Wikipedia](https://en.wikipedia.org/wiki/Intellectual_property_protection_of_typefaces),
1. "the **shapes** of typefaces are **not eligible for copyright**, though the shapes may be protected by design patent " (boldface added).
2. "a **font file** of computer instructions in a domain-specific programming language, may be **protectable by copyright**" (boldface added).

As a concrete example, the [CC Accidenz Commons](https://creativecommons.org/2019/10/28/accidenz-commons-open-licensed-font/) font is under a CC BY-SA 4.0 license. In the US, this license does not apply to the glyphs' shapes themselves because they are not covered by copyright.

If anything, the CC license applies to the font file, which encodes the glyphs in a high-level declarative specification language. According to [Goldman (2020)](https://ipandmedialaw.fkks.com/post/102giuw/battle-lines-drawn-over-font-copyright-protection) the US Copyright Office may now have the position that the declarative specification used in font files it not protected by copyright!
:::


:::danger
**CC heart logo**

If I had designed my own logo as a starting point for this case study, the IP analysis would be much easier. I would own the copyright in logo. Or the logo would not qualify for copyright protection all, which is rather unlikely if the logo would show a minimal creative spark. Also, the logo would no be (also) a trademark. Since I would be logo's copyright holder, I could create derivative works and I could license the logo any way I wished for.

However, now I have to deal with the repercussions of using someone else's work.

Is the CC heart logo protected by copyright? Regardless whether the individual graphical elements (heart and "c") have copyright protections or not, the [unique composition of the shapes](https://www.commarts.com/columns/is-it-true-that-copyright-doesn-t-protect-graphic-design) (i.e., a *collection* !?) that make up the heart logo result in copyright protection.

Perhaps the encoding of the "c" in the font file of CC Accidenz Commons is under copyright. CC seem to think so, because the font file is licensed with CC BY-SA 4.0. If the font file enoyed copyright protection, it may be still legal to redraw the "c" from scratch. (In this case, it would be a good idea to document how the letter was *reverse engineered* without copying from the font file in case there are legal proceedings.)

Is the CC heart logo a trademark? I could not find a definite answer. [Creative Commons has a trademark policy](https://creativecommons.org/policies#trademark) and claims various trademarks (which is independent of the trademark's copyright status):
> "Our registered trademarks and other trademarks include [...] CC (including the **CC in a circle logo (the “CC Logo”)** and CC standing alone) [...]"  
> (boldface added)  

The classic CC logo, referred to as "CC Logo", is explicitly claimed.

> ![](https://i.imgur.com/g3Un7Q0.png =x300)  
> Screenshot of [TESS](https://www.uspto.gov/trademarks/search/using-trademark-electronic-search-system) record of CC Logo  
> Screenshot by Holger Kienle,
> believed to be in the public domain in the US because it is a government web site and database, otherwise believed to be fair use

Moreover, the CC Logo is a *registered trademark* and recorded in the TESS database. In contrast, the CC heart logo is not recorded in the database and it is also not explicitly claimed in the trademark policy.
However, since a "consumer"/user who is familiar with the CC Logo, will also associate the CC heart logo with Creative Commons, we should assume that the CC heart logo is (indirectly) covered by the trademark policy!

Interestingly, even though the CC logo are copyright protected, they do not come with a CC license -- this is unfortunate for our use case because it would reduce legal uncertainty.

Creative Commons' rationale for not providing a CC license is that ["applying a CC license to your trademarks and logos could even result in a loss of your trademark rights altogether"](https://creativecommons.org/faq/#could-i-use-a-cc-license-to-share-my-logo-or-trademark).

Not everybody seem to share this rationale though: [Wikimedia has licensed its logos](https://diff.wikimedia.org/2014/10/24/wikimedia-logos-have-been-freed/) under CC BY-SA 3.0 even though they are trademarks and come with a trademark policy.

I can use the CC heart logo, if I am in compliance with the trademark policy. Most appliable to my use case, the policy states:
> "Descriptive uses: For the avoidance of doubt, you do not need our permission [...] for **descriptive use** (e.g., to describe CC licensing in explanatory materials), provided that such use does not imply endorsement by or association with Creative Commons.

Since it can do no harm and demonstrates good intentions, I have added a notice that this case study is not associated with Creative Commons.

For the CC hear logo, I operate on the following facts/assumptions:
- It is (automatically) copyrighted and has no CC license.
- It is a trademark and uses of it have to adhere to Creative Commons' trademark policy.
- The trademark policy "overrides" the copyright, because otherwise using/copying the logo would result in a copyright infringement punishable by law.
- My use of the CC heart logo is too far removed from the provisions of the trademark policy. As a result, without explicit consent from Creative Commons for my use I am in violation of the policy and infringing on copyright because I am copying and even make derivative works of the CC hear logo.
- I foolheartishly proceed with the case study...
:::

:::warning
**SVG encoding of the CC heart logo**

The CC heart logo can be [downloaded as a ZIP file](https://creativecommons.org/wp-content/uploads/2019/02/ccheart_black.svg_.zip) from the CC web site. The SVG encoding is text-based (not binary) and one can look at its [raw content](https://github.com/hkienle/cc-course-final/blob/main/ccheart_black.svg?short_path=637e186) with a text editor. The SVG file is surprisingly short, consisting of only 21 lines!

Here is an excerpt from the file (reformatted, comments start with `#`):
```
<path d="

  # draw first "c"
 
  M 22983.64 21630.19  # move to coordinates (absolute)
  l -2928.01 -1451.38  # draw straight line (relative)
  c -1017.73,1483.99 -1758.21,2488.33 -3897.08,1902.25 -1678.91,-460.05 -2175.85,-2300.18 -2239.67,-3843.76 -87.17,-2108.39 649.94,-4543.46 3168.15,-4413.24 1609.13,83.19 2294.75,1032.23 2661.15,1885.36  # draw cubic curve (relative)
  l 3196.99 -1638.9
  c -1574.75,-3004.31 -5265.13,-4026.05 -8393.32,-3188.81 -3328.66,890.9 -5014.61,3952.95 -4955.5,7255.23 60.43,3375.58 1680.8,6291.51 5161.55,7052.54 1697.16,371.06 3545.13,284.81 5116.74,-503.18 1216.27,-609.83 2567.56,-1786.86 3109,-3056.12
  z  # close path

  # draw second "c"
  ...
  "/>
```
A SVG file specifies drawing instructions along with coordinates. SVG is a [declarative language](https://anvaka.github.io/sj/compare/) that directly specifies "what" rather than requiring to program the "how". You can move to a coordinate (`m`), draw a line to a coordinate (`l`) and specify [cubic Bézier curves](https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial/Paths#curve_commands) (`c`). 

Perhaps amazingly, what you see in the above SVG excerpt is the first letter "c" in the heart logo. If you look closely, the "c" has 2 straight lines and 2 curvy parts -- and this is reflected in the SVG with 2 line commands (`l`) and 2 Bézier commands (`c`).

> ![](https://i.imgur.com/cUa6hpG.png =x300)  
> *Screenshot of "c" in CodePen*  
> Screenshot by Holger Kienle, licensed under CC BY-SA 4.0

I [uploaded the SVG excerpt to CodePen](https://codepen.io/anon42/pen/GRGBzoJ?editors=1000), which allows live-rendering and editing of the "c" letter.

As a side note, it would be possible to create a new SVG file with slightly changed coordinates. (This could be accomplished with "reverse engineering" the shapes by drawing them from scratch.) The result would look the same to the human eye, but the new SVG would not be the result of copying from the original file.
:::


:::danger
**SVG file of CC heart logo**

Is the logo's SVG file copyright protected? Strictly speaking, we can distinguish between the copyright in the logo as such and the copyright of the logo's SVG encoding. [Weinberg (2015)](https://publicknowledge.org/wp-content/uploads/2021/11/3_Steps_for_Licensing_Your_3D_Printed_Stuff.pdf) discusses this distinction with the example "between a digital photograph and a file that
contains a digital photograph" and says:
> in that case copyright can be thought of as **protecting the entire bundle**, which means that the distinction is not particularly meaningful. In large part, this is because the photograph itself is well within the scope of copyright protection.  
> (boldface added)

Thus, it makes sense to assume that both the heart logo and the corresponding file are copyright protected.

For convenience the [unzipped heart logo file has been committed to the case study's repository](https://github.com/hkienle/cc-course-final/commit/b49752fe7ddf617c2a781febcd6d103ebc459c93). Since the logo is copyrighted, this may be copyright infringement! Since the repository that contains the file is meant as OER to teach about copyright and CC licenses, the trademark policy may cover this use. However, the file in the repository is not a use of the logo per se. The copy is not strictly necessary to accomplish the OER.


I also uploaded a reformatted and annotated copy -- this may qualify as a derivative work -- of the SVG encoding of the letter "c" to the [repository](https://github.com/hkienle/cc-course-final/blob/main/ccheart_black-first_c.svg) and to [CodePen](https://codepen.io/anon42/pen/GRGBzoJ?editors=1000). Here, the answer seems less clear whether this constitutes a copyright infringement.

Interestingly, the font file of the letter "c" is under CC BY-SA 4.0. With Weinberg's "bundle" theory this may also mean that the shape of the "c" is licensed as such, independent of its encoding.

One other way to look at it is that we are dealing with a typeface's glyph, which is not necessarily protected by copyright (e.g., this is the case in the US). A declarative specification of the glyph is also not necessarily protected (e.g., this may be the case in the US). The SVG encoding of the "c" happens to be such a declarative specification!
:::


:::warning
**FreeCAD excursion: reverse engineering of shapes**

You can start with a 2D shape (say the glyph of a typeface) and recreate its shape. Technically, this is not copying, but reverse engineering. Generally speaking, reverse engineering is a well establish technique in engineering and it is legal. Recreating the letter of a font may be legal too.

> ![](https://i.imgur.com/LiK0Rqw.png)  
> *Tracing the outline of a handle in FreeCAD*.  
> Image by Jo Hinchliffe in [FreeCAD for Makers](https://hackspace.raspberrypi.com/books/freecad), HackSpace, September 2022. Licensed with CC BY-NC-SA 3.0.  
> Cropped from original  
> [PDF download](https://hackspace.raspberrypi.com/downloads/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBazhkIiwiZXhwIjpudWxsLCJwdXIiOiJibG9iX2lkIn19--5cc6d95c1be694fba3150e7c3f8f7245b090f203/HS_FreeCAD_Bookazine.pdf). 

FreeCAD can be used to recreate shapes approximately. For example, you can take a 2D picture of a 3D object and load the picture into FreeCAD. You can then trace the outline in FreeCAD to obtain a geometric encoding of the shape.
:::


:::warning
**Inkscape: Rendering and manipulating the heart logo**

Inkscape can load and render SVG files. Thus, we can load the heart logo with Inkscape and explore its properties.

> ![](https://i.imgur.com/odIzBFU.png =x250)  
> *Inkscape screenshot of first "c" in heart logo*  
> Screenshot by Holger Kienle, licensed under CC BY-SA 4.0

After ungrouping and using the [node tool](https://inkscape-manuals.readthedocs.io/en/latest/node-operations.html), we can graphically see the nodes that make up the "c".

> ![](https://i.imgur.com/YDIRp8Q.png =x250)  
> *Inkscape screenshot of mutilated "c" in heart logo*  
> Screenshot by Holger Kienle, licensed under CC BY-SA 4.0

The nodes can be interactively manipulated to arrive at a mutilated "c", creating a derivative work. Since the file that contains the "c" is CC BY-SA 4.0, the derived shape should be licensed likewise. Or is the font file a collection of glyphs? If so, we do not know the license of the individual glyphs and have to assume each glyph is copyrighted -- if copyright protection applies in the first place.

For our case study we will not change the shape of the heart logo, we are only [using Inkscape to resize](https://graphicdesign.stackexchange.com/questions/85077/how-do-i-resize-an-object-in-inkscape-to-an-absolute-size) the logo. The original logo is 52x45 cm! (It is not strictly necessary to resize with Inkscape, the logo could be resized at a later stage with FreeCAD or PrusaSlicer.)
:::


### virtual 3D (.FCStd, STL, and g-code)

We are now ready to enter the world of 3D with the help of FreeCAD, which allows us to view a flat (2D) object in 3D space and to *pad* a flat surface into a 3D object.


:::warning
**FreeCAD: importing the SVG of the heart logo**

FreeCAD can import an SVG image with `File > Import...`. Each SVG closed path is converted to a corresponding [FreeCAD `Wire`](https://wiki.freecadweb.org/Draft_Wire) object.

> ![](https://i.imgur.com/sK7d2TU.png)  
> *Imported heart logo into FreeCAD (with axis cross)*  
> Screenshot by Holger Kienle, licensed under CC BY-SA 4.0

Since the heart logo has 4 closed path, we get 4 corresponding `Wire` objects named `Path`, `Path001`, `Path002` and `Path003`. The objects are placed on the XY-plane in the 3D space.

We can rename the objects to more telling names: `heart-inner`, `heart-outer`, `c-first` and `c-second`, respectively.
:::


::: success
**adding a dimension: from 2D to 3D**

Let's say you select an existing 2D work by someone else that is under copyright and "extend" it into a 3D work. Your 3D work is a [sculpture, which is clearly protected by copyright](https://copyright.uslegal.com/enumerated-categories-of-copyrightable-works/pictorial-graphic-and-sculptural-work/). Generally speaking such a modification -- from 2D to sculpture -- creates a derivative work and is a copyright infringement.

> ![](https://i.imgur.com/rHmbG5t.png =x250)
![](https://i.imgur.com/IFTCs0N.png =x250)  
> From 2D to 3D. Left: detail of photograph (postcard) by Art Rogers, copyrighted. Right: corresponding detail of sculpture by Jeff Koons, copyrighted. Details of images taken from the article *Art Rogers vs. Jeff Koons* by [Jeff Traub](https://designobserver.com/feature/art-rogers-vs-jeff-koons/6467/), believed to be fair use to illustrate a legal issue in scholarly discussion

The artist [Jeff Koons]() used a photograph as a starting point to commission a sculpture. As Traub emphasizes, this "was not a case about two photographs, but about a sculpture and a [post]card." Traub also contrasts the quality of the different works: A cheap postcard for trivial amusement on the one side, a highly crafted artwork with carefully selected materials displayed in a museum on the other side. The effect of the sculpture was presumably quite stunning on the observer. According to Traub, Koon's lawyer "strongly questioned whether a sculpture could *ever* be considered a copy of a photograph, so great was the transformation required in the change of medium".

Regardless, the court focused on the basic fact that the sculpture was a ['substantially similar'](https://en.wikipedia.org/wiki/Substantial_similarity) copy of the original work (*substantial similarity test*). Thus, changing the media from 2D to 3D did not avoid infringement.

> ![](https://i.imgur.com/W488GCl.png =x300)  
> [*Super Mario Brothers Polymer Clay Sculpture*](https://www.instructables.com/Super-Mario-Brothers-Polymer-Clay-Sculpture/) by poofrabbit, image licensed under CC BY-NC-SA 4.0. Cropped from original. Probably a copyright infringement of the original author, used here as example to illustrate a legal issue

These copyright concerns are not restricted to expensive art and famous artists.
If you create a Super Mario sculpture yourself, it is an artistic work that is automatically protected under copyright. But you have also created a derivative work of a [2D original](https://supermarioplay.com/), thereby infringing on the original work's copyright.
:::


:::danger
**FreeCAD: applying a license**

By default the design in a FreeCAD file is `All rights reserved`. To change this, go to `File > Project information...` to pick a CC license.

> ![](https://i.imgur.com/XF8BDpa.png)  
> *FreeCAD dialog to pick a license*  
> Screenshot by Holger Kienle, placed into the public domain with CC Zero

The license URL is filled in automatically (with version 4.0). Note that CC Zero is not available, but you can use the `Other` category for more flexibility.

There is a `Created by` text field that can be used for the *A* in *TASL*. There is a also a `Comment` text field that can be (ab)used for more detailed attribution or licensing information.

I licensed the heart logo FreeCAD file with CC BY-SA 4.0 (1) within the file and (2) also gave this information in the repository's `README.md`. Note that if you accidentially use different licenses, you are effectively dual-licensing the file.

We now have the same shapes that make up the heart logo in a different encoding (FreeCAD's internal representation vs. SVG). That the logo can now be viewed in 3D space from different angles does not change the fact that it is a derived work. If a court would apply the substantial similarity test, it is very likely that it would affirm similarity.

Hypothetically speaking, if the logo was CC licensed then changing the format/encoding would be allowed under any CC license. However, presumably, for the ND license element changing the format should cause no (significant) changes to the work itself. By importing the SVG into FreeCAD we can now produce "distorted" views, which can change the work significantly. It is highly doubtful whether would be allowed by ND.

To summarize, by importing the logo's SVG (and going to a 3D space) we have created a copy and made a derivative work. Even though we are doing this in the context of non-commercial OER we cannot argue for fair use. However, the CC trademark policy may allow us to create a 3D "sculpture" of the heart logo in our OER context. Boldly, we proceed...
:::


:::warning
**FreeCAD: modeling the heart logo in 3D**

It is outside of the scope of the case study to describe the modeling details. I only want to give an impression of the basic idea. (Also, there are several techniques with different trade-offs that could be used.)

> ![](https://i.imgur.com/WaVYUi6.png)  
> *Heart shape in Sketcher workbench*  
> Screenshot by Holger Kienle, licensed under CC BY-SA 4.0

We convert the 2 `Wire` objects that make up the heart shape into a [`Sketch`](https://wiki.freecadweb.org/Sketcher_Workbench). The sketch looks rather cluttered because the heart shape is composed of 22 [`BSpline`](https://wiki.freecadweb.org/Sketcher_CreateBSpline) segments. We do not have to manipulate the sketch (luckily), but we can admire the result.

> ![](https://wiki.freecadweb.org/images/c/cc/PartDesign_Pad_example.svg =x150)  
> *Starting with a flat surface (A) and padding it into a 3D shape (B)*  
> Image [*PartDesign Pad example*](https://wiki.freecadweb.org/File:PartDesign_Pad_example.svg) by Normandc, licensed under BY SA 3.0

> ![](https://i.imgur.com/2WwhFI9.png)  
> *Padded heart shape in Part Design workbench*  
> Screenshot by Holger Kienle, licensed under CC BY-SA 4.0

Note, that we have an inner and an outer outline. In between we have a flat/planar surface (on the XY-plane). FreeCAD offers the [`Pad`](https://wiki.freecadweb.org/PartDesign_Pad/en) tool, which allows us to "pads up" the heart into a 3D volume (by pulling it along the Z-axis).

> ![](https://i.imgur.com/rqvITLE.png)  
> *3D heart logo with measurements*  
> Screenshot by Holger Kienle, licensed under CC BY-SA 4.0

The "cc" shape is done analogously. A box-like shape has been created first, which supports both the heart and "cc" shape. We are done with the 3D modeling.
:::

:::danger
**FreeCAD: licensing for open content**

The model is saved in FreeCAD's [native format](https://wiki.freecadweb.org/File_Format_FCStd#Change_the_source_of_the_file_.FCStd), which has `.FCStd` as suffix. It is important to make this file available, and to make it available under an OER license. If want to adhere to Open Source Hardware (OSH), it is also [important to allow commercial use](https://www.oshwa.org/faq/#noncommercial)! In effect, for CC licenses we can use CC BY and CC BY-SA. (As already mentioned above, I picked CC BY-SA 4.0.)

Why is it important to make the native file available and to pick a CAD tool that is FOSS such as FreeCAD? Only the `.FCStd` file contains the high-level modeling steps, which allows other to load and to easily inspect and manipulate it. 

In other words, poor choices of software and formats can make "open" content effectively less open or even closed. The [ALMS Framework](http://www.opencontent.org/definition/) provides a guide and further information in the context of OER.

> ![](https://i.imgur.com/DQGV0R8.png)  
> *[Excerpt of discussion of openness of Prusa MINI](https://github.com/prusa3d/Original-Prusa-MINI/issues/34#issuecomment-849795541)*  
> Screenshot by Holger Kienle, believed to be fair use

An example how "open" content can effectively be "closed" content, at least for a group of users, are the modeling files of the Prusa MINI 3D printer. The printer is certified as open source hardware, but it uses Autodesk Inventor as CAD software. Not only runs Inventor only on Windows, it is only available as costly subscription option (e.g., USD 290 per month as of December 2022). Additionally, there are annual Inventor releases and [older versions of Inventor cannot open files created with newer versions](https://knowledge.autodesk.com/support/inventor/troubleshooting/caas/sfdcarticles/sfdcarticles/How-can-I-open-Inventor-files-from-a-newer-version-than-the-version-that-I-have-purchased.html)! :shocked_face_with_exploding_head: 
:::


:::warning
**FreeCAD: from model to mesh**

FreeCAD's native `.FCStd` file format enables convenient analysis and modification. But it is understood by FreeCAD only.

The STL format is widely understood. It is the *lingua franca* for 3D objects. It somewhat compares to PDF in this respect: Word and LibreOffice can produce PDF, and virtually all printers accept PDF. Similarly, virtually all 3D printing software (so-called *slicers*) accept STL.

> ![](https://i.imgur.com/dveuoZB.png)  
> *Meshed CC heart logo*  
> Screenshot by Holger Kienle, licensed under CC BY-SA 4.0

To arrive at an STL file, we first create an in-memory representation, which is called a [triangle mesh](https://en.wikipedia.org/wiki/Triangle_mesh). In FreeCAD we only have to select the model (i.e., our CC heart logo) and apply the [create mesh operation](https://wiki.freecadweb.org/Mesh_FromPartShape) to it.

The STL format preserves key properties of the 3D object, namely its shape. However, even this is not quite true. STL only approximates the shape with many small planar surfaces. In effect, curves are approximated by straight lines.

> ![](https://i.imgur.com/6So4FhU.png =x200) Crude meshing  
> 
> ![](https://i.imgur.com/6vVRg0F.png =x200) Fine meshing
>
> *Different meshing algorithms and settings result in cruder or finer meshings*
> Screenshot by Holger Kienle, licensed under CC BY-SA 4.0

If the mesh's resolution is fine-grained enough for our intended purpose, the mesh's approximation will not matter. FreeCAD's default meshing works well for our needs. 

> ![](https://i.imgur.com/HKQG1d4.png =x250)  
> *Meshing-look for artistic effect*  
> 3D object [Lion](https://www.thingiverse.com/thing:728085) by 3DWP, licensed under CC BY-SA 3.0. Screenshot of 3D model by Holger Kienle, licensed under CC BY-SA 4.0

However, if the mesh's resolution is too course it can affect the 3D-printed object. A mesh-effect can be used on purpose as artistic effect.
:::


:::warning
**FreeCAD: exporting mesh to STL**

In FreeCAD, a mesh object can be exported with `File > Export`. STL files typically have the suffix `.stl`. If you use `.stl` then FreeCAD will produce a binary STL file, with `.ast` you will get a textual (ASCII) STL.

You can inspect a textual STL. It consists of geometric information (coordinates) that are impossible to comprehend by (ordinary) humans.

Here is the start of our STL file, which has 6135 lines in total:
```
solid Mesh
  facet normal -0.000000 -1.000000 0.000000
    outer loop
      vertex 47.730000 0.000000 0.000000
      vertex 0.000000 0.000000 0.000000
      vertex 0.000000 0.000000 -4.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 -0.000000
    outer loop
      vertex 47.730000 0.000000 0.000000
      [...]
```
:::


:::danger
**Licensing STL**

STL is essentially structured data. One can look at it as
- a [data file](https://en.wikipedia.org/wiki/Data_file)
- a data set (specifiying 3D coordinates for triangles)
- a simple database (with an [*implicit schema*](https://research.cs.queensu.ca/home/cordy/Papers/IWPC02_Exchange.pdf) that is described in a prose specification)

Even if we can view an STL as a simple database, this does not mean that the file is protected under [sui generis database rights]( https://en.wikipedia.org/wiki/Database_right) because the STL is generated without much effort and does not represent a significant investment.

These (technical) distinctions may perhaps not matter when selecting a license. The CC licenses cover may use cases, among them ["dissemination or reuse of data"](https://wiki.creativecommons.org/wiki/Data#What_is_the_difference_between_the_Open_Data_Commons_licenses_and_the_CC_4.0_licenses.3F)

In line with other assets of the case study, the STL file of the heart logo is licensed with CC BY-SA 4.0. (As discussed before, the STL is a derivative work of a work copyrighted by Creative Commons and the trademark policy may or may not sanction it.)

It is possible to add comments to a textual STL by starting them with a semicolon (`;`). This allows us to add licensing information directly within the file:
```
; Copyright Holger Kienle
; This work is licensed under CC BY-SA 4.0.
; To view a copy of this license, visit http://creativecommons.org/licenses/by-sa/4.0/.
solid Mesh
  facet normal -0.000000 -1.000000 0.000000
      [...]
```

There are also the Open Knowledge Foundation's [ODC-BY 1.0](https://opendatacommons.org/licenses/by/summary/) or [ODbL 1.0](https://opendatacommons.org/licenses/odbl/summary/) licenses -- the latter is a copyleft/share-alike license -- that specifically target databases, but they ["do not apply to the individual contents of the database"](https://wiki.creativecommons.org/wiki/Data#What_is_the_difference_between_the_Open_Data_Commons_licenses_and_the_CC_4.0_licenses.3F)! Since the STL is probably not a database in the legal sense, it seems best to stick to the more encompassing CC licenses.
:::


:::warning
**PrusaSlicer: from STL to g-code**

We are close to a physical print. PrusaSlicer is one of many FOSS slicers for 3D printers.

> ![](https://i.imgur.com/6ll3LDI.png)
> *CC heart logo imported to PrusaSlicer*  
> Screenshot by Holger Kienle, licensed under CC BY-SA 4.0

With PrusaSlicer we can import our STL file. After the import, we see a rendering of the object on the virtual build plate.

It looks not much different to what we see with FreeCAD. But in contrast to FreeCAD, PrusaSlicer only allows rudimentary modification of the object such as scaling. (It is a bit like having a document in LibreOffice versus PDF Reader.)

Most importantly, PrusaSlicer allows us to control how the object will be printed. There are actually many considerations and trade-offs, ranging from the print material, over the infill-pattern and wall strength to the print speed and quality.

> ![](https://i.imgur.com/92mtXlL.png)
> *Preview shows first print layer of the heart and "cc" shapes*  
> Screenshot by Holger Kienle, licensed under CC BY-SA 4.0

> ![](https://i.imgur.com/a1qyyET.png)
> *Detail of first layer of "c": Each colored line is a "thread" of filament that is squished out by the print head*  
> Screenshot by Holger Kienle, licensed under CC BY-SA 4.0

One key feature of PrusaSlicer is to simulate the print-run, layer by layer. PrusaSlicer also estimates  the print time and how much material (filament) will be consumed. With the default settings, the heart logo prints in 33 minutes.

> ![](https://i.imgur.com/xXAJwPB.png)
> *Left panel shows g-code instructions for moving the print head; main view shows the position of the print head for the correspondng g-code line*  
> Screenshot by Holger Kienle, licensed under CC BY-SA 4.0

The instructions that control the functioning of the printer are called g-code. One line of g-code only produces a tiny piece of the object: To print the outline of the "c" about 60 lines of g-code are needed. For our printout, the printer will do 2 outlines of the "c" shape (for more wall thickness and better strength). And it will do this for 10 layers such that the logo has some height.

Importantly, the generated g-code is for a specific 3D printer model, in our case the Prusa MINI. (G-code is like assembly code, which has to match the CPU.) You need the STL file and slicing software to generate g-code for your own 3D printer.

Usually, only the STL is published. But there is no harm in publishing the g-code for people that happen to have the same 3D printer model than you. This saves them the trouble of generating the g-code themselves (as long as they are happy with the settings that you used to produce the g-code).

While the STL of a 3D model can still be manipulated to some degree by the slicer or dedicated software (e.g., [MeshLab](https://www.meshlab.net/#)), g-code is usually just executed as-is.
:::


:::danger
**Licensing g-code**

For the first time we are licensing software code. G-code is a bit of a peculiar kind of programming language for controlling automated machine tools that originated in 1950s, but g-code are low-level software programs.

[Creative Commons does not recommend to license software with its licenses](https://creativecommons.org/faq/#can-i-apply-a-creative-commons-license-to-software). Among the reasons given, dedicated software licenses:
- may address patent rights (which is not covered by CC licenses).
- can use concepts such as source code, object code, system libraries, etc. to describe the rules of the license.

License compatibility can also be an important consideration for the purpose of "remixing" code.

Interestingly, [CC Zero can be used for software](https://wiki.creativecommons.org/wiki/CC0_FAQ#May_I_apply_CC0_to_computer_software.3F_If_so.2C_is_there_a_recommended_implementation.3F), but t "has not been approved by the Open Source Initiative".

The [GNU General Public License](https://www.gnu.org/licenses/licenses.html#GPL) (GPL) the most widely know and used software license and is used "by more than half of all free software packages". GPL is copyleft and in spirit very similar to the ShareAlike licensing element.

The GPL comes in various version, 3.0 is the latest, but 2.0 is still also relevant. Importantly, one can not only pick the version but also whether a user of the license has the option to apply a later version if she wishes to do so ("or any later version"). When denoting the license, [Richard Stallman](https://www.gnu.org/licenses/identify-licenses-clearly.html
) makes the plea to clearly say, for instance, "GPL-2.0-only" or "GPL-2.0-or-later".

I license the g-code with GPL-2.0-or-later because:
- I want a copyleft license and GPL is most well known.
- GPL is similar in spirit to CC BY-SA.
- Version 2.0 or later gives the most flexibility for future reuse.


Analogous to STL, the g-code file uses `;` for comments. We can open the g-code in a text editor and add copyright and license information:
```
; Copyright Holger Kienle
; Licensed under GNU General Public License v2.0 or later (SPDX: GPL-2.0-or-later)
; To view a copy of this license, visit https://www.gnu.org/licenses/gpl-2.0-standalone.html
[...g-code...]
```

Actually, when licensing g-code, a dedicated software license may not be strictly necessary because g-code is directly interpreted by a machine and the distinction between source and object/binary code does not apply. Also g-code has no concept of libraries or API calls. But using a dedicated software license feels the right thing to do.
:::


### physical 3D

:::warning
**Prusa MINI: printing the g-code**

{%youtube NZ0qzvlBQhs%}  
> *Printing the heart logo with the Prusa MINI (5x speedup)*  
> [Video](https://www.youtube.com/watch?v=NZ0qzvlBQhs
) by Holger Kienle, licensed under CC BY-SA 4.0

> ![](https://i.imgur.com/N9WczrZ.jpg =x300)  
> *Finished heart logo badge/stamp on the Prusa MINI's build plate*  
> Image by Holger Kienle, licensed under CC BY-SA 4.0

Finally, we can transfer the g-code to the Prusa MINI and hit the start button. (There are quite of few things that can go wrong during the print, but here we assume an ideal scenario.)
:::


:::danger
**publishing on printables.com**

@@@
:::

:::success
**mutually exclusive: copyright or patent**

To summarize what we already know: When dealing with artistic creations that are fixated in writing, on canvas, as recording, etc. then almost certainly the work is automatically protected under copyright. If the copyright has not expired and the work is in the public domain, the fair use doctrine applies, which permits limited use of the copyrighted work.
If the copyrighted work is claimed as a trademark then (1) you may use the work in a descriptive manner and/or (2) there may be a trademark policy that spells out how the work can be used.

When moving away from artistic creations to real-world (3D) objects, the starting point should be to question whether copyright actually applies. If the object is useful (i.e., it is serving a purpose) then copyright does not apply, but the object may be protect*able* with a (utility) patent. Note that protect*able* does not mean that the object is necessarily protected by a patent.)

As a general rule, Weinberg (2013) makes the point that
> "in a practical sense, **copyrights and patents are mutually exclusive**. If you have a useful article you cannot protect it with a copyright"  
> (boldface added).

If something is protected under copyright, it cannot be protected as patent; and vice versa. A chair is a useful object and if it embodies a novel invention then the chair can be patented. In other words, the product of an industrial design process is not copyright protected.

Conversely, a chair is not protected under copyright! If we have an ordinary, boring chair, no utility patent and no copyright can be claimed. A sculpture, in the sense of a 3D artwork, is (automatically) copyrighted. If, accidentially, you could abuse it as a chair or bottle opener, this does not make it patentable.

> ![](https://i.imgur.com/kXkojD9.png =x200)  
> [*New Shop-Vac Wet/Dry*](http://www.jeffkoons.com/artwork/the-new/new-shop-vac-wetdry) by Jeff Koons, copyright Jeff Koons, believed to be fair use to illustrate a scholarly legal discussion

Let's look at one more fun example. Let's say we have a vacuum cleaner. It clearly is a useful object that falls under patent law. Conversely, copyright law does not apply. (Yet another issue we have not looked at: The looks of the vacuum cleaner could be covered by a [design patent](https://en.wikipedia.org/wiki/Design_patent)). If the vacuum cleaner is used as part of a sculpture, the result is a piece of art, which is not a useful object. This is not a hypothetical example, as the sculpture *New Shop-Vac Wet/Dry* shows. Its materials are an industrial vacuum cleaner, acrylic, and fluorescent lights.

In practice, relatively few 3D objects in the physical world are protected by IP because most objects serve a utilitarian function and patenting them has several hurdles: the object must meet the criteria of non-obviousness, it must not have been patented before, and the patent must be applied for in a lengthy and costly process involving a lawyer.
:::


:::danger
**physical heart logo: copyright or patent viewpoint**

> ![](https://i.imgur.com/91dPSf1.jpg =x200) ![](https://i.imgur.com/jTSSE4h.jpg =x200)  
> *Left: 3D printed heart logo as nerdy badge/brooch*  
> *Right: 3D printed heart logo as (rubber-like) stamp*  
> Photos by Holger Kienle, licensed under CC BY-SA 4.0

For the printed out heart logo we can ask: Is it a useful object?

- Yes (it is a stamp): We can argue that it is a useful object because it can be used as a stamp: We can use a rubber-stamp pad to transfer the logo to a piece of paper. This would mean that our stamp has no copyright protection. But we could consider whether the stamp can be patented. Besides having no intention to do it seems unlikely that the stamp would be considered non-obvious. (But many trivial patents have been granted like [*method of swinging on a swing*](https://www.newscientist.com/article/dn2178-boy-takes-swing-at-us-patents/).)
- No (it is a badge): We can argue that the object is a decorative badge that is meant for wearing as a fashion accessory. In this case, it is not patentable. It may have an (automatic) copyright as an artistic brooch or mini-sculpture. (Remember, the threshold for "creative spark" is quite low.)
:::


:::success
**Janus-faced 3D objects**

I have not told the full story of the copyright-patent dichotomy. The real world is more difficult.

The copyright vs. utility patent rule breaks down for Janus-type objects that both (1) are useful and (2) have artistic elements. In such cases, the law tries to deconstruct the object into artistic elements and utilitarian functionality, and then applies copyright and patent law correspondingly (*conceptual severability test*). This approach works reasonably well if you image a chair with an artwork on its back rest, but often has high uncertainty. (Supreme court judges [disagreed](http://www.maw-law.com/copyright/r-p-conceptual-separability-test/) on an actual case.)

Most copyrighted works that we are dealing with are 2D. Most -- actually: all? -- real-world objects we are dealing with are 3D. As we learned, for 3D objects copyrightability vs. patentability needs to be considered. At one extreme, a 3D object may have neither copyright nor patent protection, at the other extreme it may have both copyright-protected and patented features.

For 3D objects (real or virtual) it is often the case that derived 2D works exist: For example, a 2D photograph is taken of a 3D sculpture. Or a blueprint is created from a 3D CAD model (FreeCAD supports this with the [Techdraw workbench](https://wiki.freecadweb.org/TechDraw_Workbench)).

The other way around, 2D artwork can be applied to a 3D object: An photo can be printed on a T-shirt, a fabric design is applied to a [cheerleader uniform](https://en.wikipedia.org/wiki/Star_Athletica%2C_LLC_v._Varsity_Brands%2C_Inc.). Neither the cut of the T-shirt nor the cut of the uniform can be copyrighted, but the artwork is. This is especially clear if the artwork existed first in 2D, regardless whether in its final form of as a conceptual sketch from which the final work has been derived.
:::


:::danger
**physical heart logo: Janus-faced viewpoint**

> ![](https://i.imgur.com/zIZ6ZBX.png =x150)  
> *Has the physical Coca-Cola rubber stamp no coypright protection because it is strictly serving a utilitarian function of stamping?*  
> Taken from image search, copyright status unknown, believed to be fair use to illustrate a legal issue in scholarly discussion

So, the strict dichotomy between copyright and patent does not exist for all 3D objects. For our printed heart logo this approach makes more sense. We can try to apply the conceptual severability test:
- logo as artistic elements: The logo is an artistic element that can be separated out.
    - If we view our 3D object as a brooch/badge, it is ornamental and has not utility.
    - If the 3D object functions as a stamp, it (also) serves a utilitarian functions. I have no idea how copyright law would resolve this dilemma, but it would seem strange to resolve the logo's copyright protect -- think of famous logos such as Coca-Cola -- on the ground of the intended/advertised use of the 3D object (brooch vs. stamp).
- utilitarian functionality: The base that carries the 3D logo is of utilitarian nature to support the artistic element. It is the result of a rudimentary industrial design process: Selecting suitable dimensions and thickness to have sufficient strength. As mentioned before, the result of an industrial design process is not copyright protected.
:::


## parting thoughts

> ![](https://i.imgur.com/Pcl7gSC.png =x80)
>
> *Not exactly a unanimous decision by the Supreme Court involving an IP case: [Star Athletica LLC v. Varsity Brands](https://www.supremecourt.gov/opinions/16pdf/15-866_0971.pdf)*, screenshot from PDF, believed to be in the public domain in the US, otherwise believed to be fair use

Perhaps once in a while you reach the point where you feel utterly confused about copyright and its many interacting laws: trademarks, contract law, utility patents, design patents. And the doctrines and test to sort out copyright and IP: idea-expression dichotomy, transformational use doctrine, substantial similarity test, conceptual severability test, etc.

Well, do not despair: Supreme Court judges cannot agree either on what is going on ([Star Athletica LLC v. Varsity Brands](https://www.supremecourt.gov/opinions/16pdf/15-866_0971.pdf)). :confused:

The best we can do is to remember: There is the strictly legal side, but there is also the human side and its desire to remix and to be part of a community. When it comes to licensing and sharing, let's proceed with the best of intentions and hope that others will act likewise.

> ![](https://i.imgur.com/hc1F6W2.png =x300)  
> *The stamp in action...wait a minute, what's that!?...:anguished:*  
> *It looks like we need at least one more iteration before we can start to roll out high-volume production...*  
> Photo by Holger Kienle, licensed under CC BY-SA 4.0

With licensing, as with real life, sometimes you won't quite get the expected result. But keep trying! :nerd_face:
