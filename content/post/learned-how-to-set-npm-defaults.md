+++
showonlyimage = true
draft = false
image = "/img/post_npm_init_defaults.jpg"
date = "2017-09-01T20:15:00+02:00"
title = "Setting NPM init defaults"
weight = 0
+++

One of the first npm things I learned was how to set default author details
<!--more-->

## npm init
Does the email address you use change between projects? Not very likely! How about your name? Or your website url?
Chances are these don't change all that often, yet when you run `npm init` it'll ask you to fill these in every time.
And yeah.. you can skip these - but there's a better way!

Just like how `git` lets you set a [user name and email address](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup), npm allows you to set a default name, email address and url.

![Set defaults using npm set](/img/post_npm_defaults_term.jpg "Set defaults using npm set")

To set your username, use `npm set init-author-name "My name"`. To set an email address, use `npm set init-author-email "my@email.com"`. 

The full list of available defaults can be found in the [npmjs docs](https://docs.npmjs.com/misc/config).

