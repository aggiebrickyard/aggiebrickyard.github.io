# The Aggie Brickyard

Welcome...this website is build using the **Voyager** jekyll theme (<http://redvi.github.io/voyager>).

For more info on the Features and Options, visit the **[voyager github repo](https://github.com/redVi/voyager)**.

## Notes For Website Maintenance

To preview site locally use: `bundle exec jekyll serve` in terminal window (in folder where repo housed), then go to http://127.0.0.1:4000/

### Photos:

 - Keep photos compressed if possible, jpgs are fine. Can use `imagemagick` command such as:

 > `convert -strip -interlace Plane -gaussian-blur 0.05 -quality 85% source.jpg outfile.jpg`

### PDFs

#### Optimizing Size
 - Try export optimized PDFs, a relatively high quality version but at a much smaller size (~10 MB instead of ~100 MB). For most viewing on a computer, the difference in quality isn't worth the large load times.
 - **If using OSX**, *Preview* has some ability to reduce the pdf size without sacrificing much in the way of quality. I added a quartz filter which reduces a pdf to 75% quality, a decent tradeoff in size vs clarity of pictures, graphics etc. It will take a ~130MB to about 15 MB.
     - To do so, grab the **ReduceFileSize_75.qfilter** file in the Dropbox folder under *`final_pdfs`
     - Save it to the `~/Library/Filters` or `Library/PDF Services` folder
     - Open the PDF (high res version) with Preview, go to File > Export from Preview, select "*Reduce File Size 75%*"" under the Quartz filter drop down. 75% is not the overall reduction, rather how it is reduced.

#### Embedding PDFs

_**To Embed from Box**_, right click on the file, `More Actions` and `Embed Widget`. Click `Custom`, and select `Embed Widget`> Custom and select 600 width, and 775 height, copy the link and add to your markdown.

_**To embed from Dropbox**_, put a copy of the pdf in your Public folder and the Brickyard website already has an `embedpdf.html` script in the `_includes` folder for embedding from Dropbox. You simply right click on your file of interest in Dropbox, copy the end of the public link into the script and your done. See Fall 2016 for an example.

#### **For Posts**

Use **`layout: post`** in `yaml`.

```
---
layout: post
bg: 'background.jpg'
title: "Post Heading"
date: 2016-06-29
tags : ['front-end']
author: "Author"
categories: posts
---
```

#### **For Pages**

If page contains `active` tag, it will display as a tab on the site menu.

```
---
layout: page
title: "About"
permalink: /about/
active: about
---
```

#### **Archive Page**

The Archive page sorts posts by tags. No more than one tag in one post, e.g.:

*Good:*

```
tags : ['front-end']
```

*Bad:*

```
tags : ['front-end', 'jekyll']
```
