---
title: "Creating a New Theme"
date: 2019-04-01T14:26:00+08:00
draft: false
tags: ["English", "Theme"]
slug: "English Preview"
---

## Introduction

{{< bilibili 925044144 >}}


<iframe src="https://open.spotify.com/embed/track/3XdIJo4Myqjne3EvxNRZFo" style="border-radius: 5px" width="100%" height="300" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"></iframe>


{{< spotify type="track" id="3XdIJo4Myqjne3EvxNRZFo" >}}



<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=100% height=86 src="//music.163.com/outchain/player?type=2&id=4940920&auto=0&height=66"></iframe>

{{< neteasemusic 2 4940920 >}}



This tutorial will show you how to create a simple theme in Hugo. I assume that you are familiar with HTML, the bash command line, and that you are comfortable using Markdown to format content. I'll explain how Hugo uses templates and how you can organize your templates to create a theme. I won't cover using CSS to style your theme.
<!--more-->
We'll start with creating a new site with a very basic template. Then we'll add in a few pages and posts. With small variations on that, you will be able to create many different types of web sites.

In this tutorial, commands that you enter will start with the "$" prompt. The output will follow. Lines that start with "#" are comments that I've added to explain a point. When I show updates to a file, the ":wq" on the last line means to save the file.

Here's an example:


## Sharing Templates

If you've been following along, you probably noticed that posts have titles in the browser and the home page doesn't. That's because we didn't put the title in the home page's template (layouts/index.html). That's an easy thing to do, but let's look at a different option.

We can put the common bits into a shared template that's stored in the themes/zafta/layouts/partials/ directory.

### Create the Header and Footer Partials

In Hugo, a partial is a sugar-coated template. Normally a template reference has a path specified. Partials are different. Hugo searches for them along a TODO defined search path. This makes it easier for end-users to override the theme's presentation.


