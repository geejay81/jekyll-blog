---
layout: post
date: "2017-11-26 20:57:00"
categories: Jekyll Github Hosting
---

Hosting a Jekyll site on Github pages is pretty easy. Here's what I had to do to host this site.

> Assuming that you have a Gihub account and Jekyll site already set up.

1. Firstly, we need to create a repository in our Github account. I've called mine jekyll-blog, [at this link](https://github.com/geejay81/jekyll-blog).

2. Next, we will edit the _config.yml file. Change the baseurl value to the same name as your Github repository. Here I have changed mine to jekyll-blog as this is the name of my repository.

``` yaml
baseurl: "jekyll-blog"
```