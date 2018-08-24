# hexo-theme-bootstrap4

A modern [Bootstrap 4](http://getbootstrap.com/) blog theme for [Hexo](https://hexo.io).

**[Demo Site](https://www.andrewzigler.com/blog)**

Based on the [official Bootstrap 4 blog example template](https://getbootstrap.com/docs/4.0/examples/blog/).

Uses [Fancybox](http://fancybox.net/) for images.

## Installation

**This theme was built with Hexo 3.2.**

### Clone the repository

```bash 
$ cd site-folder
$ git clone https://github.com/jodumont/hexo-theme-bootstrap4.git themes/hexo-bootstrap4
```

### Update the site's _config.yml
```yml
# Extensions
theme: hexo-theme-bootstrap4
```

## Configuration

```yml
# Header
navbar_brand:
menu:
  Index: /
  Archive: archive/

# RSS
rss:

# Theme Color
color: '#ffffff'

# Content
favicon: favicon.ico
excerpt_link: Read More
fancybox: true

# Sidebar
widgets:
- about
- category
- tag
- tagcloud
- archive
- recent_posts
about_widget_content: >
  <p>Etiam porta <em>sem malesuada magna</em> mollis euismod.
  Cras mattis consectetur purus sit amet fermentum. Aenean
  lacinia bibendum nulla sed consectetur.</p>

# Widgets
archive_type: 'monthly'
show_count: true

# Meta Maker
title_divider:
twitter_creator:
twitter_site:
google_plus:
fb_personal_id: ""
fb_page_id:
fb_admins:
fb_app_id:
og_image_url: ""

# Analytics
google_analytics:
```

### Header

- *navbar_brand:* text for navbar head
- *menu:* hyphenated list of menu links

### RSS

- *rss:* relative URL for atom.xml file

> It works well with [hexo-generator-feed](https://github.com/hexojs/hexo-generator-feed)

### Color

- *color:* will define the theme-color for browsers and platforms

> 1. generate your logo with [Real Favicon Generator](https://realfavicongenerator.net);
> 2. put these inside your ./source folder;
> 3. choose a color for your theme (generally is the main color of your logo).  
> Don't forget the **' '** and the **#** before your color code.

### Content

- *favicon:* filename of favicon.ico in main directory
- *excerpt_link:* text for excerpt button, default is 'Read More'
- *fancybox:* default is true, allows Fancybox for better images

### Sidebar

- *widgets:* hypenated list of widget partials in folder
- *about_widget_content:* the sidebar's about text

### Widgets

- *archive_type:* measurement for archive, default is 'monthly'
- *show_count:* If true, show post count after categories and tags

### Meta Maker

- *title_divider:* divider symbol in titles between site and page name
- *twitter_creator:* author's Twitter username (include @ in double quotes)
- *twitter_site:* Twitter brand/company username (include @ in double quotes)
- *google_plus:* Google+ ID (in double quotes)
- *fb_personal_id:* Facebook vanity URL username of author
- *fb_page_id:*
- *fb_admins:*
- *fb_app_id:*
- *og_image_url:* absolute path

### Analytics

- *google_analytics:* Google Analytics tracking ID for site

## Features

### Callouts

Bootstrap doesn't have [callouts](https://codepen.io/chrisdpratt/pen/IAymB) enabled by default, but their styles have been reconstructed and included in this theme. You can use the following tag to include a callout:

```
{% callout [type:default|primary|success|info|warning|danger] %}
This is where the text goes...
{% endcallout %}
```

### Sidebar Widgets

This theme has 6 default widgets that can be displayed in the sidebar:

- *[about](./layout/_widget/about.ejs):* the `about_widget_content` field in the theme's `_config.yml`
- *[category](./layout/_widget/category.ejs):* list of post and page categories
- *[tag](./layout/_widget/tag.ejs):* list of post and page tags
- *[tagcloud](./layout/_widget/tagcloud.ejs):* cloud of tags by frequency
- *[archives](./layout/_widget/archives.ejs):* list of archives
- *[recent_posts](./layout/_widget/recent_posts.ejs):* list of recent posts

### Bootstrap Paginator Helper

A custom `bs_paginator()` helper is used to produce [pagination markup for Bootstrap 4.1](https://getbootstrap.com/docs/4.1/components/pagination/). It is used in place of Hexo's default `paginator()`.

```
<%- bs_paginator({
      prev_text: __('previous'),
      next_text: __('next')
     }) %>
```

### Meta Maker & Schema

Use instead of Hexo's default `open_graph()` helper on every page. It pulls OG data from your site's `_config.yml` files to ensure every page has meta data for all major social media networks (Facebook, Twitter, LinkedIn, and Google+).

```
<%- meta_maker() %>
```

The article partials also include schema tags from [Schema.org](https://schema.org/) and pre-optimized. You can use the [Google Structured Data Testing Tool](https://search.google.com/structured-data/testing-tool/u/0/) to verify the schema integrity of your articles.

## MIT License

Copyright © 2018 JOduMonT (legal@jodumont.com)
Copyright © 2017 Andrew Zigler (andrewzigler@gmail.com)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.