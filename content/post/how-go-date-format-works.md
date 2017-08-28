+++
showonlyimage = true
draft = false
image = "/img/post_go_date_format.jpg"
date = "2017-08-28T18:10:00+02:00"
title = "Date formatting in Go"
weight = 0
+++

Today I learned how Go date formatting works.
<!--more-->

When I posted my second article on this blog I noticed all the dates said "august 17". At first I thought I f'ed up the posts' timestamps, but after checking them it turned out to be a bug in the [Hugo Tracks template](https://github.com/ageekymonk/hugo-tracks-theme/).

## Date formatting
The Hugo Tracks template formats dates using {{< highlight go >}}.Date.Format "January 06"{{< /highlight >}}. I assumed this meant "output the name of the month and use two digits for the day of the month". Makes sense and I couldn't figure out what was wrong - until I read the [Hugo(https://gohugo.io/functions/format/)] and [Go docs](https://golang.org/pkg/time/) and noticed that it should read "January **02**". 

> The reference time used in the layouts is the specific time:
> > Mon Jan 2 15:04:05 MST 2006
> To define your own format, write down what the reference time would look like formatted your way;

I fixed the templates and opened a [pull request](https://github.com/ageekymonk/hugo-tracks-theme/pull/6/files). The fix was merged into master just one hour later!

![Pull request diff](/img/post_go_date_diff.png "Pull request diff")