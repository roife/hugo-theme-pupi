+++
title = "Pupi - Getting Started"
date = 2022-08-09T15:38:30+08:00
header_img = ""
toc = true
tags = ["documentation", "guide"]
series = ["Themes Guide"]
+++

Pupi is a responsive, simple and clean [Hugo](https://gohugo.io/) theme based on the [Huxblog Jekyll theme](https://github.com/Huxpro/huxpro.github.io).

<!--more-->

## Install Hugo

Make sure you have installed the latest version of [Hugo-extented](https://gohugo.io/getting-started/installing/).

## Create a New Site

```
hugo new site mysite
```

## Add the Theme

You can download and unpack the theme manually from Github or use git to clone the theme into your site's `themes` directory.

```bash
cd mysite
git init
git clone https://github.com/roife/hugo-theme-pupi.git themes/pupi
```

Or you can add the theme as a submodule.

```bash
cd mysite
git init
git submodule add https://github.com/roife/hugo-theme-pupi.git themes/pupi
git submodule update --init --recursive
```

That’s all, Pupi is ready to be used.


## Add Config Files

For getting started, you can copy the `config.toml` file from the theme's exampleSite directory to the root directory of your site.

```bash
cp themes/pupi/exampleSite/config.toml .
```

> Note: You may need to delete the `themesDir` line in the config file.

## Add Some Content

Create a new post with the following command.

```bash
hugo new posts/my-first-post.md
```

Edit the content of the post.

```markdown
+++
title = "{{ replace .Name "-" " " | title }}"
date = {{ .Date }}
description = ""
draft = true
subtitle = ""
header_img = ""
toc = true
tags = []
categories = []
series = []
comment = true
+++

Your content here...
```

Some front-matter used for SEO, others used for displaying contents, configuration, etc.

## Run example site

From the root of themes/pupi/exampleSite:

```bash
hugo server --themesDir ../..
```
