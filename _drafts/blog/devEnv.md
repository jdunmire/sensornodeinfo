---
layout: post
title: "Developement Environment"
author: Jerry
#date: YYYY-MM-DD  # last modified if different than the filename/modification time
permalink: /blog/2016/01/31/devEnv
#commentIssueId: <issue number>  # optional, no comments if not defined
categories:
- blog
- tools
img: bogdanco-Toolkit_144x144.png
thumb: bogdanco-Toolkit_70x70.png

---

When you start working with a new processor, or language, the question of
how to organize you development environment is important. You want
tools where they can be used for multiple programs and your project
sources where they can be isolated from each other.
And of course you want to be able to easily find what you
are looking for!

This post covers the arrangement I'm using for the ESP-8266 with some
background on why I arrange things as I do. All of my development work
is done on Ubuntu, but my comments apply to just about any Linux system.

<!--more-->
Definitions
-----------
Before we go on, lets agree on some terms:
  * __bundle__: This is a group of files to be installed on your system.
      Bundles are usually installed manually, often multi-platform, and
      are not a _package_. Bundles deal with dependencies in an ad-hoc
      manner. There may be installation scripts that check for and
      attempt to install the dependencies, the installation scripts my
      just report the missing dependencies, or the dependencies might
      only be listed in the documentation.

  * __package__: A package is a group of files to be installed on your
      system along with information that identifies dependencies on othe
      packages, and configuration information. Packages generally can
      not be installed without the use of a package manager. Common
      Linux package format are DEB and RPM.

  * __package manager__: A package manager installs, configures, and
      tracks packages. The common work of identifying conflicts and
      resovling dependencies is part of the package manager rather than
      being built-in to each package.

  * __SDK__: A Software Developement Kit contains the toolchain and
      libraries for a specific processor and may be specific to a target
      operating system.

  * __toolchain__: A toolchain is the group of programs that are used to
      transform source code into an exectuable program. If the target
      (the CPU and OS where the resulting program will run) is the same
      as the the CPU+OS where the toolchain program run, then the
      toolchain is _native_. A _cross_ toolchain is one that runs on
      CPU+OS and builds exectuables for a a different CPU+OS.

When you start working with a new processor you have to find a toolchain
that supports it and libraries to use with it. You will probably find a
suitable toolchain from one or more of these sources:

  * __OS Packages__:
  * __OS Specific 3d party packages__:
  * __3d party bundles__:
Arduino, Eclipse, Visual
Studio, 
Source for tools
  - Depends on target environment
  - Packages - easy but hard to control versioning
      - OS packages - easy, but often out of date
      - OS specific 3d party packages - almost as easy, and very up-to-date
      - 3d party bundles

bundles vs packages: packages are build with and for specific package
managers, APT, YUM, etch.

target - definition needed
toolchain- definition needed
SDK - definition needed

binary or source
I tend to avoid building toolchains from source: I've done it enough
times already. Time I spend building and maintaining the toolchain is
time I don't get to spend on the original project itself.

Building toolchains from source tends to be time-consuming and
frustrating. On the upside you do get great control over defaults and
optimizations. Working with tools you've built from source can also
enable you to fix problems which impact you but might not be the highest
priority to the tool developer(s). If you have the time and interest,
building and maintaining your toolchain from source can be a rewarding,
though time consuming, part of a project.

Development Environments
------------------------
An _Integrated_ development environment (IDE) is probably the most common
development choice these days. It is easy to setup, easy to use, comes
with a GUI and designed for the target you've chosen. What's not to
like? Well:

 * You are stuck with the IDE tools. For example, if you don't like
   or want to learn a new editor, you are probalby stuck.
 * Automation can be a problem. An IDE may have a way to automate
     sequences and the best do it with a language rather than simple
     configuration choices. But the automation is generally only
     available from within the IDE itself, so it still requires a button
     click to get things started.
 * If you don't have the very best understanding of the IDE, you are
     probably going to get IDE configuration files mixed in with your
     project code. Until you get the developer specific parts of the
     configuration separated from the configuration that defines the
     project to the IDE, you will have serious problems sharing your
     code with other developers.

There are IDEs that are very versatile and that attempt to solve the
problems I've mentioned (Eclipse is a good one). 

SDK vs IDE

  - SDK
      - binary/mixed
      - source
  - IDE - tied in to the whole tool chain: editor, SCM, build system,
      languages, debugger

Command line or IDE?


Locations:

/opt/vendor/toolchain

~/working/project/

Project config files in preference to environment variables in
preference to dot-files.
