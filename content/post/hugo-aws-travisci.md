+++
showonlyimage = true
draft = false
image = "img/post_travis_aws.jpg"
date = "2017-08-22T09:00:22+05:30"
title = "Hugo, Travis CI & AWS"
weight = 0
+++

How I set up a static https website using S3 buckets, Cloudfront, Route S3, Hugo and Travis CI.
<!--more-->

When I decided to move this site away from Github pages one of the first things people suggested to me was AWS. It's cheap, reliable and easy! Not only did I move from GH to an S3 bucket, I also abandoned [Jekyll](https://jekyllrb.com/) in favour of [Hugo](https://gohugo.io).

This post describes the actions taken and lessons learned.

## Hugo & AWS
Hugo is an open-source static website generator that requires the user to write content using markdown and then generates HTML. The HTML/CSS/image files can then be uploaded to any web host. Amazon Web Services provides the perfect platform for a static website. I used [continuous failure's](http://continuousfailure.com/post/s3_blog/) terraform script to set up my amazon S3 buckets, route s3 and domains. I used [Cloudfront](https://deliciousbrains.com/wp-offload-s3/doc/custom-domain-https-cloudfront/) to set up free https on the account.

## Travis CI
Manually uploading the generated HTML becomes tiresome after a while so I followed the rest of the [continuous failure blog](http://continuousfailure.com/post/s3_blog/) and registered a [Travis CI](https://travis-ci.org) account to make sure the site gets rebuilt and uploaded every time I commit a new change to [github](https://github.com/tseidler/terryseidler.com).

