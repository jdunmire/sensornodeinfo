This is the drafts folder for components. To preview these drafts, run
jekyll with the --drafts option:

    $ jekyll server --drafts

Components should begin with a header like this:

---
layout: component
title:  "title of the component"
summary: ""
started: YYYY-MM-DD
#date: YYYY-MD-DD  # last modified if different from filename/modification time
status: active|dev|concept|Obsolete
repository: https://github.com/jdunmire/<repo>
#commentIssueId: <issue number>  # optional, no comments if not defined
permalink: /component/unique-title
categories:
- component
- <one or more categories, one per line. Firmware|Hardware|???>
img: 640x480_image.jpg|png
thumb: 70x53_image.jpg|png or 70x70_image.jpg|png
#carousel:  # Optional
#- <imagename>,Title
#- <image2>,Title2

---

When the draft is complete, move it from this directory to the
_posts/components directory. The file name in the _posts/components
directory must begin with a date in YYYY-MM-DD-<name>.md format.

The img: file should be placed in assets/img/components/.
The thumb: file should be placed in assests/img/components/thumbs/.
Carousel images go in the assets/img/components/carousel/ directory.
