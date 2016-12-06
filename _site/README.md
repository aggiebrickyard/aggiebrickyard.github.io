# The Aggie Brickyard

Welcome...this website is build using the **Voyager** jekyll theme (<http://redvi.github.io/voyager>).

For more info on the Features and Options, visit the **[voyager github repo](https://github.com/redVi/voyager)**.

### Notes For Website Maintenance

 - Keep photos compressed if possible, jpgs are fine. Can use `imagemagick` command such as:

 > `convert -strip -interlace Plane -gaussian-blur 0.05 -quality 85% source.jpg outfile.jpg`

 - Try export optimized PDFs, a relatively high quality version but at a much smaller size (~10 MB instead of ~100 MB). For most viewing on a computer, the difference in quality isn't worth the large load times.

To View site locally use: `bundle exec jekyll serve`

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
