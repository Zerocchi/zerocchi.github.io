---
layout: post
title: "PHPfied CSS?"
date: 2026-01-09T09:21:57+0800
lastmod: 2026-01-15T06:43:39+0800
type: post
categories:
- "Posts"
- "Programming"
thumbnail: https://s3.amazonaws.com/micro.blog/thumbnails/2026/01/14/blog.zerocchi.com/3923841ffd4511f7a051575234984012.png
opengraph:
  title: "Zerocchi Blog - PHPfied CSS?"
  image: https://s3.amazonaws.com/micro.blog/opengraph/2026/01/14/5703270.png
url: "/2026/01/09/phpfied-css.html"
bluesky:
  id: "bafyreigvxpfhx4hpqvhusxofnwdxiiijel4geflhhh2zi27tkkxh4rtfh4"
  url: "at://did:plc:wpdbknogd47ooysv6eau2yjt/app.bsky.feed.post/3mbxdjj2x7k2g"
  link: "https://bsky.app/profile/did:plc:wpdbknogd47ooysv6eau2yjt/post/3mbxdjj2x7k2g"
  handle: "zerocchi.com"
  hostname: "bsky.social"
  did: "did:plc:wpdbknogd47ooysv6eau2yjt"
---
I was this years old to know aside of HTML, you can also convert CSS  file to PHP in order to use some PHP shenanigans. Just add a header to  indicate that it’s of type `text/css`:

```css
<?php header("Content-Type: text/css"); ?>
@import url('../styles.css?v=<?=filemtime('../styles.css')?>');

.category-header {
    background-color: var(--color-bg-alt);
    backdrop-filter: blur(5px);
    ...
}
```
and inside the HTML file you can link the stylesheet like usual, except changing the `.css` to `.php`

```html
<link rel="stylesheet" href="gallery.php">
```
Wild.
