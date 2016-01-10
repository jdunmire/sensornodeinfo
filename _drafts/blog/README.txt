This is the drafts folder for blog posts. To preview these drafts, run
jekyll with the --drafts option:

    $ jekyll server --drafts

Posts should begin with a header like this:

---
layout: post
title:  "title of the post"
#date: YYYY-MM-DD  # last modified if different than the filename/modification time
permalink: /blog/YYYY/MM/DD/unique-name
#commentIssueId: <issue number>  # optional, no comments if not defined
categories:
- blog
- <one or more categories, one per line>
img: 640x480_image.jpg|png
thumb: 70x53_image.jpg|png or 70x70_image.jpg|png

---

When the draft is complete, move it from this directory to the
_posts/blog directory. The file name in the _posts/blog
directory must begin with a date in YYYY-MM-DD-<name>.md format.

The img: file should be placed in assets/img/blog/
The thumb: file should be placed in assests/img/blog/thumbs/

