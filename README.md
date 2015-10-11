Sensor Node Information
=======================
This a Jekyll based website to document the design and use of ESP-8266
Sensor Nodes.

The theme for this web site is based on
[solid-jekyll](https://github.com/st4ple/solid-jekyll). The starting
point is commit cd5c599e9d on the master branch. The project was cloned
and then the git archive command was used to transfer the files to this
archive:

    $ git clone git@github.com:st4ple/solid-jekyll.git
    $ cd solid-jekyll
    $ git archive --format=tar HEAD | (cd ../sensornodeinfo/ && tar xf -)


Setup
-----
If these files are committed to the `gh-pages` branch of a git
repository hosted on [GitHub](https://github.com), then
[Jekyll](https://jekyllrb.com) will be run automatically and a
functional web site will be available at
http://<YourName>.github.io/<RepositoryName>/

To view the web site locally you can install
[Jekyll](https://jekllrb.com) locally.  On Ubuntu
[Jekyll](https://jekyllrb.com/) and all required dependencies can be
installed using a simple `apt-get`:

    $ sudo apt-get install jekyll

To view the web site, start the Jekyll web server:

    $ jekyll --server

And direct your browser to http://localhost:4000/


License
-------
  Copyright (C) 2015 Jerry Dunmire
  This file is part of SensorNodeInfo

  SensorNodeInfo is a web site. You can redistribute it and/or modify it
  under the terms of the _Creative Commons Attribution-ShareAlike 4.0
  International Public License_ unless otherwise noted in specific
  files.
