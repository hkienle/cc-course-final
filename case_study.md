---
name: cc-course-case_study
tags: cc, course-cc
---

:::info
**legal information**

(c) Holger Kienle

![](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/by-sa.svg =x40)  
Except where otherwise noted, this document's content is licensed under the [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) license.
Please attribute this document to *hmk* (pseudonym) and link it with [https://hackmd.io/@hkienle/course-cc-final/](https://hackmd.io/@hkienle/course-cc-final/)

For **screenshots** made by the author:
- Making a screenshot is believed to be [fair use](https://psu.libanswers.com/faq/333836), thus not violating any copyright that may exist in the depicted GUI.
- To remove doubt, if the screenshot depicts content by the author, it is licensed under CC BY-SA 4.0.
:::

**CC Certificate for Educators - Fall 2022 - Final**
# a case study of licensing the 3D-printing workflow
[TOC]

## introduction

This case study looks at the workflow to produce a 3D artifact from its design to its physical instantiation with a 3D printer. The workflow produces several digital artifacts and in the end a physical artifact. The case study discusses intellectual property (IP) and licensing considerations for each artifact.

> ![](https://creativecommons.org/wp-content/uploads/2019/02/ccheart_black.png =x120)  
> *Starting point: CC heart logo* by Creative Commons, copyrighted, trademark policy applies, believed to be fair use as a subject of scholarly discussion

The starting point of the case study is the CC logo with a heart outline (2D).

> @@@  
> Result: stamp

At the end we will have produced a physical 3D object that can function as a "rubber stamp".


### open and free

An important goal of the case study is to use [free and open-source software](https://en.wikipedia.org/wiki/Free_and_open-source_software) (FOSS) and to license all material with [free licenses](https://en.wikipedia.org/wiki/Free_license).

The following table gives an overview of the used software tools.
| FOSS | domain | license (SPDX) |
| -------- | -------- | -------- |
| Inkscape | vector graphics editor | GPL-3.0-or-later |
| FreeCAD | parametric 3D CAD modeler | LGPL-2.0-or-later |
| PrusaSlicer | 3D printer slicer | AGPL-3.0 |


An aspect easily overlooked is that software should operate on [open file formats](https://en.wikipedia.org/wiki/Open_file_format), which are  defined by an openly published specification. Conversely, it is desirable to avoid [proprietary formats](https://en.wikipedia.org/wiki/Proprietary_file_format). This case study uses:
| format | domain | specification license |
| -------- | -------- | -------- |
| SVG     | vector images (2D) | [W3C Document License](http://www.w3.org/Consortium/Legal/copyright-documents) |
| STL | triangulated surfaces (3D objects) | [openly documented, but proprietary](https://www.loc.gov/preservation/digital/formats/fdd/fdd000504.shtml) (?)|
| markdown | documentation, many dialects | [CommonMark Spec](https://spec.commonmark.org/): CC BY-SA  |
| PNG | bitmap images (screenshots)| [W3C Software and Document Notice and License](https://www.w3.org/Consortium/Legal/2015/copyright-software-and-document)


## meta

::: danger
**caveat**

I cannot give legal advice and I am not a lawyer anyways. What I can do is to make you aware of certain considerations about the intersection of intellectual property (IP), licenses, and technical artifacts. It is a starting point to form your own opinions and conclusions.

Whenever you read a sentence discussing legal issues, you should prepend it with: As you know, the author is not a lawyer and only gives his opinion as a lay person for entertainment purposes only. Also, the specifics of the law will vary depending on the country.

It this case study feels like a wild roller coaster, it is so because IP law is a wild roller coaster... :nerd_face:
:::

:::success
**green boxes**

Writing in green boxes are used to explain legal or technical issues, which are relevant for the case study
:::


:::warning
**yellow boxes**

Writing in yellow boxes describe an artifact used or produced for the case study.
:::


## case study

We split the discussion into two parts, somewhat arbitrarily: We start with 2D, and then move on to 3D.

### 2D

The first step in our workflow is to analyze the logo with the help of Inkscape. The logo is 2D and described with Scalable Vector Graphics (SVG). Inkscape can process SVG and its native file format is [SVG enhanced with Inkscape-specific meta data](https://inkscapetutorial.org/svg-file-format.html).


:::warning
**CC heart logo**

> ![](https://creativecommons.org/wp-content/uploads/2019/02/ccheart_black.png =x120)  
> [*CC heart logo*](https://creativecommons.org/about/downloads/) by Creative Commons, copyrighted, no copyright license. Should be considered a trademark by Creative Commons.

Our logo, in the following called *heart logo*, is an interesting case to consider:
- It is (automatically) copyrighted and has no CC license.
- It is a trademark and uses of it have to adhere to Creative Commons' trademark policy.
- It is a 2D work that we want to extend to a 3D object.

The hear logo has two graphical elements:
1. The heart shape, which forms the logo's outline.
2. The letters "cc", which are rendered in a specific font (CC Accidenz Commons).

The heart outline may be considered a *basic shape* -- part of the [suits of playing cards](https://en.wikipedia.org/wiki/Playing_card_suit), originating more than 500 years ago --, which is not protected by copyright. (As a side note, it's fascinating that a heart shape can be defined with a mathematical function.)

> ![](https://upload.wikimedia.org/wikipedia/commons/7/7e/Heart_plot.svg =x150)  
> *Plot of a mathematical function that yields a heart symbol* by [Eviatar Bach](https://commons.wikimedia.org/wiki/File:Heart_plot.svg), placed in the public domain with CC Zero

The letter "c" itself is not under copyright and the particular shape of the "c" may be also not under copyright. The encoding of the "c" in the font file of CC Accidenz Commons may be under copyright (and this file is licensed with CC BY-SA 4.0).

Regardless whether the individual graphical elements (heart and "c") have copyright protections or not, the unique composition of the shapes that make up the heart logo result in copyright protection!

Independently of the logo's copyright status, the heart logo is (indirectly) claimed as a trademark of Creative Commons:
> Our registered trademarks and other trademarks include [...] CC (including the **CC in a circle logo** (the “CC Logo”) and CC standing alone) [...]  
> (boldface added)

The heart logo has not been registered, but the more common CC logo with a circle is.
:::


:::success
**copyright and basic shapes**

There is no copyright of ideas. There is no copyright of basic (abstract) shapes. (Before you get the idea that copyright might be sane after all: perhaps [4 minutes and 33 seconds of silence](https://ipkitten.blogspot.com/2012/04/price-of-silence-and-myth-of-batt-cage.html) may be copyrighted.)

According to [Kattwinkel](https://www.owe.com/resources/legalities/legalities-15-is-a-shape-copyrightable-how-to-get-appropriate-rights-when-you-commission-graphic-design/), "no one can own exclusive copyright in a square, circle, oval, or diamond, or the common fleur de lis. Such shapes can be included as part of a more complex design, that as a whole is copyrighted". Generally, a work ["must have a minimum amount of creativity" to be under copyright](https://copyright.uslegal.com/enumerated-categories-of-copyrightable-works/creativity-requirement/).

While a simple rectangle and the abstract idea of a rectangle are not protected by copyright, depicting a rectangle in a distinctive and creative way probably yields copyright protection (e.g., the use of color-gradients and shadows may accomplish this). Generally, in copyright law ["the amount of creativity required is very little"](https://copyright.uslegal.com/enumerated-categories-of-copyrightable-works/creativity-requirement/).

> ![](https://i.imgur.com/bcVA6nb.png =x100)  
> *A yellow rectangle on black background*, copied and cropped from somewhere on the Internet, considered fair use. Note that this has nothing to do with the National Geographic logo, any similarity would constitute a coincidence.

A simple rectangle cannot be copyrighted, but a particular rectangle may be protected under trademark law (e.g., [National Geographic](https://help.nationalgeographic.com/s/article/logo-use-and-trademark)).
:::


:::success
**trademarks-copyright interaction**

A logo can enjoy both copyright and trademark protection. Copyright applies automatically, whereas the trademark protection has be claimed (e.g., by applying "TM") and defended (e.g., with  having a track-record of using the mark and sending cease-and-desist letters).

Optionally, a trademark can be registered with the US Patent and Trademark Office. It is then recorded in a database and it can be marked with :registered:. The CC logo is an example of a registered trademark.

> ![](https://i.imgur.com/g3Un7Q0.png =x300)  
> Screenshot of [TESS](https://www.uspto.gov/trademarks/search/using-trademark-electronic-search-system) record, believed to be in the public domain in the US because "most government-produced materials appearing on this website are not subject to copyright restrictions within the United States"; screenshot by hmk

A trademark can have a *trademark policy* that governs the use of the trademark. A trademark policy is necessary if the trademark owner wants to allow third-parties to use it under certain conditions. [Creative Commons has a trademark policy](https://creativecommons.org/policies) for its CC logos, buttons, license elements, etc.

The artworks are covered by the CC trademark policy are (automatically) copyrighted. However, they do not have a CC license because ["applying a CC license to your trademarks and logos could even result in a loss of your trademark rights altogether"](https://creativecommons.org/faq/#could-i-use-a-cc-license-to-share-my-logo-or-trademark)! (Conversely, [Wikimedia has licensed its logos](https://diff.wikimedia.org/2014/10/24/wikimedia-logos-have-been-freed/) under CC BY-SA 3.0 even though they are trademarks and come with a trademark policy.)
:::


:::warning
**SVG encoding of the CC heart logo**

The CC heart logo can be [downloaded as a ZIP file](https://creativecommons.org/wp-content/uploads/2019/02/ccheart_black.svg_.zip) from the CC web site. For convenience the [unzipped file has been committed to the case study's repository](https://github.com/hkienle/cc-course-final/commit/b49752fe7ddf617c2a781febcd6d103ebc459c93). The motivation for doing this is that all assets of the project should be available in a self-contained repository. This copy of the logo is a violation of copyright! A possible defense is that the logo is used as part of OER to teach about copyright and CC licenses -- and this use may be allowed by CC's trademark policy.

The SVG encoding is a text-based (not binary) and one can look at its [raw content in the repository](https://github.com/hkienle/cc-course-final/blob/main/ccheart_black.svg?short_path=637e186). The SVG file is actually quite short!

Here is an excerpt from the file (reformatted):
```
<path d="

  ## draw first "c"
 
  M 22983.64 21630.19  # move to coordinates (absolute)
  l -2928.01 -1451.38  # draw straight line (relative)
  c -1017.73,1483.99 -1758.21,2488.33 -3897.08,1902.25 -1678.91,-460.05 -2175.85,-2300.18 -2239.67,-3843.76 -87.17,-2108.39 649.94,-4543.46 3168.15,-4413.24 1609.13,83.19 2294.75,1032.23 2661.15,1885.36  # draw cubic curve (relative)
  l 3196.99 -1638.9
  c -1574.75,-3004.31 -5265.13,-4026.05 -8393.32,-3188.81 -3328.66,890.9 -5014.61,3952.95 -4955.5,7255.23 60.43,3375.58 1680.8,6291.51 5161.55,7052.54 1697.16,371.06 3545.13,284.81 5116.74,-503.18 1216.27,-609.83 2567.56,-1786.86 3109,-3056.12
  z  # close path

  ## draw second "c"
  ...
  "/>
```
A SVG file specifies drawing instructions along with coordinates. You can move to a coordinate (`m`), draw a line to a coordinate (`l`) and specify [cubic Bézier curves](https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial/Paths#curve_commands) (`c`). SVG is a [declarative language](https://anvaka.github.io/sj/compare/) that directly specifies "what" rather than requiring to program the "how".

Perhaps amazingly, what you see in the SVG excerpt is the first letter "c" in the heart logo. If you look closely, the "c" has 2 straight lines and 2 curvy parts -- and this is reflected in the SVG with 2 line commands (`l`) and 2 Bézier commands (`c`).

> ![](https://i.imgur.com/cUa6hpG.png =x300)  
> *Screenshot of "c"* in CodePen by hmk

I [uploaded the SVG excerpt to CodePen](https://codepen.io/anon42/pen/GRGBzoJ?editors=1000), which allows live-rendering and editing the "c" letter.

It is an interesting question whether a declarative specification, such as SVG commands, qualifies as source code, which would be automatically protected by copyright. The copyright cannot extend to the shape of the letter "c", but it may cover the (exact) content of the SVG file. In other words, the general idea or the [algorithm of drawing a "c" with SVG commands cannot be copyrighted](https://law.stackexchange.com/questions/4097/does-copyrighted-code-protect-intellectual-property-rights-on-novel-algorithms-i). But a particular specification of drawing a "c" may well be.

As a side note, it would be possible to create a new SVG file with slightly changed coordinates. (This could be also accomplished with "reverse engineering" the shape by drawing it from scratch.) The result would look the same to the human eye, but would obfuscate that the new SVG is an excerpt from Creative Commons' SVG file.
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

If anything, the CC license applies to the font file, which encodes the glyphs in a high-level declarative specification language. According to [Goldman](https://ipandmedialaw.fkks.com/post/102giuw/battle-lines-drawn-over-font-copyright-protection) (2020) the US Copyright Office may now have the position that the declarative specification used in font files it not protected by copyright!
:::


:::warning
**FreeCAD excursion: reverse engineering of shapes**

You can start with a 2D shape (say the letter of a font) and recreate its shape. Technically, this is not copying, but reverse engineering. Generally speaking, reverse engineering is a well establish technique in engineering and it is legal. Recreating the letter of a font may be legal too.

> ![](https://i.imgur.com/LiK0Rqw.png)  
> *Tracing the outline of a handle in FreeCAD*. [FreeCAD for Makers](https://hackspace.raspberrypi.com/books/freecad), Jo Hinchliffe, HackSpace, September 2022. Licensed with CC BY-NC-SA 3.0. [PDF download](https://hackspace.raspberrypi.com/downloads/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBazhkIiwiZXhwIjpudWxsLCJwdXIiOiJibG9iX2lkIn19--5cc6d95c1be694fba3150e7c3f8f7245b090f203/HS_FreeCAD_Bookazine.pdf). Cropped from original

FreeCAD can be used to recreate shapes approximately. For example, you can take a 2D picture of a 3D object and load the picture into FreeCAD. You can then trace the outline in FreeCAD to obtain a geometric encoding of the shape.
:::


:::warning
**Inkscape: Rendering and manipulating the heart logo**

Inkscape can load and render SVG files. Thus, we can load the heart logo with Inkscape and explore its properties.

> ![](https://i.imgur.com/odIzBFU.png =x250)  
> *Inkscape screenshot of first "c" in heart logo* by hmk

Ofter ungrouping and using the [node tool](https://inkscape-manuals.readthedocs.io/en/latest/node-operations.html), we can graphically see the nodes that make up the "c".

> ![](https://i.imgur.com/YDIRp8Q.png =x250)  
> *Inkscape screenshot of mutilated "c" in heart logo* by hmk

The nodes can be interactively manipulated to arrive at a mutilated "c", creating a derivative work. Since the file that contains the "c" is CC BY-SA 4.0, the derived shape should be licensed likewise. Or is the font file a collection of glyphs? If so, we do not know the license of the individual glyphs and have to assume each glyph is copyrighted -- if copyright protection applies in the first place.

For our case study we will not change the shape of the heart logo, we are only [using Inkscape to resize](https://graphicdesign.stackexchange.com/questions/85077/how-do-i-resize-an-object-in-inkscape-to-an-absolute-size) the logo. The original logo is 52x45 cm! (It is not strictly necessary to resize with Inkscape, the logo could be resized at a later stage with FreeCAD or PrusaSlicer.)
:::


:::warning
**FreeCAD: importing the SVG of the heart logo**

FreeCAD can import an SVG image with `File > Import...`. Each SVG closed path is converted to a corresponding [FreeCAD `Wire`](https://wiki.freecadweb.org/Draft_Wire) object.

> ![](https://i.imgur.com/sK7d2TU.png)
> *Imported heart logo into FreeCAD (with axis cross)* by hmk

Since the heart logo has 4 closed path, we get 4 corresponding `Wire` objects named `Path`, `Path001`, `Path002` and `Path003`. The objects are placed on the XY-plane in the 3D space.

We can rename the objects to more telling names: `heart-inner`, `heart-outer`, `c-first` and `c-second`, respectively.

We now have the same shape in a different encoding. (Changing the format/encoding is allowed for all CC licenses, even with a ND license element; but remember, the heart logo has no CC license.)
:::


:::warning
**FreeCAD: applying a license**

By default the design in a FreeCAD file is `All rights reserved`. To change this, go to `File > Project information...` to pick a CC license.

> ![](https://i.imgur.com/XF8BDpa.png)  
> This screenshot by *hmk* is licensed under CC BY. Placed into the public domain with CC Zero

The license URL is filled in automatically (with version 4.0). Note that CC Zero is not available, but you can use the `Other` category for more flexibility.

There is a `Created by` text field that can be used for the *A* in *TASL*. There is a also a `Comment` text field that can be (ab)used for more detailed attribution or licensing information.

I licensed the heart logo FreeCAD file with CC BY-SA 4.0 and gave `hmk` as creator.
:::


### 3D

We are now ready to enter the world of 3D with the help of FreeCAD, which allows us to *extrude* a flat surface into a 3D object.

::: success
**adding a dimension: from 2D to 3D**

Let's say you select an existing 2D work under copyright and "extend" it into a 3D work. For example, you select a cartoon character that previously existed on paper only and make a sculpture out of it. Generally speaking such a modification is a copyright infringement.

> ![](https://i.imgur.com/rHmbG5t.png =x250)
![](https://i.imgur.com/IFTCs0N.png =x250)  
> From 2D to 3D. Left: detail of photograph (postcard) by Art Rogers, copyrighted. Right: corresponding detail of sculpture by Jeff Koons, copyrighted. Details of images taken from the article *Art Rogers vs. Jeff Koons* by [Jeff Traub](https://designobserver.com/feature/art-rogers-vs-jeff-koons/6467/), believed to be fair use to illustrate a legal issue in scholarly discussion

The artist [Jeff Koons]() used a photograph as a starting point to commission a sculpture. As Traub emphasizes, this "was not a case about two photographs, but about a sculpture and a [post]card." Traub also contrasts the quality of the different works: A cheap postcard for trivial amusement on the one side, a highly crafted artwork with carefully selected materials displayed in a museum on the other side. The effect of the sculpture was presumably quite stunning on the observer. According to Traub, Koon's lawyer "strongly questioned whether a sculpture could *ever* be considered a copy of a photograph, so great was the transformation required in the change of medium".

Regardless, the court focused on the basic fact that the sculpture was a ['substantially similar'](https://en.wikipedia.org/wiki/Substantial_similarity) copy of the original work. Thus, changing the media from 2D to 3D did not avoid infringement.
:::


:::warning
**FreeCAD: modeling the heart logo in 3D**

The original heart logo is under copyright protection. Adding a dimension in going to 3D creates a derivative work. This is a copyright infringement, we cannot hope to argue with fair use. If we had chosen a logo with a CC license without ND it would be perfectly allowed add a dimension.

However, the CC trademark policy may allow us to create a 3D "sculpture" of the heart logo in our OER context. Boldly, we proceed...

It is outside of the scope of the case study to describe the modeling details. I only want to give an impression of the basic idea. (Also, there are several techniques with different trade-offs that could be used.)

> ![](https://i.imgur.com/WaVYUi6.png)  
> *Heart shape in Sketcher workbench* by hmk, licensed under CC BY-SA 4.0

We convert the 2 `Wire` objects that make up the heart shape into a [`Sketch`](https://wiki.freecadweb.org/Sketcher_Workbench). The sketch looks rather cluttered because the heart shape is composed of 22 [`BSpline`](https://wiki.freecadweb.org/Sketcher_CreateBSpline) segments. We do not have to manipulate the sketch (luckily), but we can admire the result.

> ![](https://wiki.freecadweb.org/images/c/cc/PartDesign_Pad_example.svg =x150)  
> [*PartDesign Pad example*](https://wiki.freecadweb.org/File:PartDesign_Pad_example.svg) by Normandc, licensed under BY SA 3.0

> ![](https://i.imgur.com/2WwhFI9.png)  
> *Padded heart shape in Part Design workbench* by hmk, licensed under CC BY-SA 4.0

Note, that we have an inner and an outer outline. In between we have a planar surface (on the XY-plane). FreeCAD offers the [`Pad`](https://wiki.freecadweb.org/PartDesign_Pad/en) tool, which allows us to "pads up" the heart into a 3D volume (by pulling it along the Z-axis).

> ![](https://i.imgur.com/rqvITLE.png)  
> *3D heart logo with measurements* by hmk, licensed under CC BY-SA 4.0

The "cc" shape is done analogously. A box-like shape has been created first, which supports both the heart and "cc" shape. We are done with the 3D modeling.

The model is saved in FreeCAD's [native format](https://wiki.freecadweb.org/File_Format_FCStd#Change_the_source_of_the_file_.FCStd), which has `.FCStd` as suffix. It is important to make this file available, and to make it available under a CC license. Only the `.FCStd` file contains the high-level modeling steps, which allows other to load it into FreeCAD and to easily inspect and manipulate it. The file is available in the GitHub repository with a CC BY-SA license (corresponding to the file's license information; see above): https://github.com/hkienle/cc-course-final/blob/main/ccheart.FCStd
:::


:::warning
**FreeCAD: from model to mesh**

FreeCAD's native `.FCStd` file format preserves convenient analysis and modification. But it is understood by FreeCAD only.

The STL format is widely understood. It is the lingua franca for 3D objects. It somewhat compares to PDF in this respect: Word and LibreOffice can produce PDF, and virtually all printers accept PDF. Similarly, virtually all 3D printing software (so-called slicers) accepts STL.

To arrive at STL, we first create an in-memory representation of the STL, which is called a [triangle mesh](https://en.wikipedia.org/wiki/Triangle_mesh). In FreeCAD we only have to select the model (i.e., or CC heart logo) and apply the [create mesh operation](https://wiki.freecadweb.org/Mesh_FromPartShape) to it.

> ![](https://i.imgur.com/MsEgIwV.png)  
> *Meshed CC heart logo* by hmk



The STL format preserves key properties of the 3D object, namely its shape. However, even this is not quite true. STL only approximates the shape with many small surfaces. If the resolution is fine-grained enough for our intended purpose, it will not matter. FreeCAD's default meshing works well for our needs. However, if 

:::


:::success
**2D versus 3D, copyright versus patent**

Does it make a fundamental difference if a work is fixated on a canvas (2D) or fixated with a sculpture (3D)? If it is a purely artistic work there is no fundamental difference -- copyright applies to both.

> ![](https://i.imgur.com/W488GCl.png =x150)  
> [*Super Mario Brothers Polymer Clay Sculpture*](https://www.instructables.com/Super-Mario-Brothers-Polymer-Clay-Sculpture/) by poofrabbit, image licensed under CC BY-NC-SA 4.0. Cropped from original. Probably a copyright infringement of the original author, used here as example to illustrate a legal issue

If you create a 3D sculpture of Super Mario, it is an artistic work that is automatically protected under copyright. (You also created a derivative work of a 2D original, thereby infringing on the original work's copyright.)

However, if a 3D object is a useful object (i.e., it is serving a purpose) then the object may be applicable for patent protection. Weinberg (2013) makes the point that "in a practical sense, **copyrights and patents are mutually exclusive**. If you have a useful article you cannot protect it with a copyright" (boldface added).

As a consequence relatively few 3D objects in the physical are protected by IP because patenting an objects has several hurdles: the object must meet the criteria of non-obviousness, it must not have been patented before, and the patent must be applied for in a lengthy and costly process involving a lawyer. In contrast, if copyright applies to a work it is automatically granted with its fixation.
:::


:::success
**copyright, utility patent, design patent**

Nothing is ever clear cut. Let's say we have a vacuum cleaner. It clearly is a useful object that falls under patent law. Conversely, copyright law does not apply. The looks of the vacuum cleaner could be covered by a [design patent](https://en.wikipedia.org/wiki/Design_patent). If the vacuum cleaner is used as part of a sculpture, the result is a piece of art, which is not a useful object. The [sculpture is protected by copyright](https://copyright.uslegal.com/enumerated-categories-of-copyrightable-works/pictorial-graphic-and-sculptural-work/).

> ![](https://i.imgur.com/kXkojD9.png =x200)  
> [*New Shop-Vac Wet/Dry*](http://www.jeffkoons.com/artwork/the-new/new-shop-vac-wetdry) by Jeff Koons, copyright Jeff Koons, believed to be fair use to illustrate a scholarly legal discussion

This is not a hypothetic example, as the sculpture *New Shop-Vac Wet/Dry* shows. Its materials are an industrial vacuum cleaner, acrylic, and fluorescent lights.
:::




:::warning
**what is a stamp?**

Copyright of a 3D shape (candlestick)
:::


freecad documentation has CC license


@@@ Poor Technical Choices Make Open Content Less Open http://www.opencontent.org/definition/


## ordering the skeins

> ![](https://i.imgur.com/Pcl7gSC.png)
>
> *Not exactly a unanimous decision by the Supreme Court involving an IP case: [Star Athletica LLC v. Varsity Brands](https://www.supremecourt.gov/opinions/16pdf/15-866_0971.pdf)*, screenshot from PDF, believed to be in the public domain in the US, otherwise believed to be fair use

Let's try to organize key points succinctly.

When dealing with artistic creations that are fixated in writing, on canvas, as recording, etc. then almost certainly the work is automatically protected under copyright. If the copyright has not expired and the work is in the public domain, the fair use doctrine applies, which permits limited use of the copyrighted work. 

If the copyrighted work is claimed as a trademark then (1) you may use the work in a descriptive manner and/or (2) there may be a trademark policy that spells out how the work can be used.

When moving away from artistic creations to real-world objects, the starting point should be to question whether copyright actually applies. If the object is useful (i.e., it is serving a purpose) then copyright does not apply, but the object may be protect*able* with a (utility) patent. Note that protect*able* does not mean that the object is necessarily protected by a patent.)

As a general rule: If something is protected under copyright, it cannot be protected as patent; and vice versa. A chair is a useful object and if it embodies a novel invention then the chair can be patented. In other words, the product of an industrial design process is not copyright protected.

Conversely, a chair is not protected under copyright! If we have an ordinary, boring chair no utility patent and no copyright can be claimed. A sculpture, in the sense of a 3D artwork, is copyrighted. If, accidentially, you could abuse it as a chair or bottle opener, it does not make it patentable.

The copyright vs. utility patent rule breaks down for Janus-type objects that both (1) are useful and (2) have artistic elements. In such cases, the law tries to deconstruct the object into artistic elements and utilitarian functionality, and then applies copyright and patent law correspondingly (*conceptual severability test*). This approach works reasonably well if you image a chair with an artwork on its back rest, but often has high uncertainty. (Supreme court judges [disagreed](http://www.maw-law.com/copyright/r-p-conceptual-separability-test/) on a actual case.)


Most copyrighted works that we are dealing with are 2D. Most -- actually: all? -- real-world objects we are dealing with are 3D. As we learned, for 3D objects copyrightability vs. patentability needs to be considered. At one extreme, a 3D object may have neither copyright nor patent protection, at the other extreme it may have both copyright-protected and patented features.

For 3D objects (real or virtual) it is often the case that derived 2D works exist: For example, a 2D photograph is taken of a 3D sculpture. Or a blueprint is created from a 3D CAD model (FreeCAD supports this with the [Techdraw workbench](https://wiki.freecadweb.org/TechDraw_Workbench)).

The other way around, 2D artwork can be applied to a 3D object: An photo can be printed on a T-shirt, a fabric design is applied to a [cheerleader uniform](https://en.wikipedia.org/wiki/Star_Athletica%2C_LLC_v._Varsity_Brands%2C_Inc.). Neither the cut of the T-shirt nor the cut of the uniform can be copyrighted, but the artwork is. This is especially clear if the artwork existed first in 2D, regardless whether in its final form of as a conceptual sketch from which the final work has been derived.




- idea-expression dichotomy
- transformational use doctrine
- substantial similarity test
- conceptual severability test


## parting thoughts



Copyright covers many domains: text, sound, images
sui generis



## appendix: troubleshooting

> ![](https://i.imgur.com/ClYPreh.png)
> Import from SVG causes self-intersecting wires