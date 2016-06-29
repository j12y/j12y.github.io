---
layout: post
title:  Blogging like a Containers Containers Containers
date:   2016-06-28 14:00:44
categories: jekyll docker markdown github livereload
---

# Blogging like a Hacker

I've often subscribed to the ideology that content is king.  I want style too
of course, but substance is first in my mind.  For this reason I was inspired
by various bloggers who have used **Jekyll** and **Github Pages** to simply
author posts in **Markdown**.

Instead of installing `jekyll` on my local machine(s), I wanted to also run
everything in a `docker` container ~~for giggles~~ in case I jump from
one machine to another to maintain consistency and make setup of a new machine
relatively easy.

I don't think I'm adding a whole lot to the conversation on this topic, so I'm
mostly going to document my learning path to a set of publishing tools and
workflows.

## Getting Started

The [official Jekyll Docker image][jekyll-dh] allows you to fire up a running
jekyll instance to serve your content or build a new site to begin with.

```
$ docker run --rm --label=jekyll --volume=$(pwd):/srv/jekyll -it -p 127.0.0.1:4000:4000 jekyll/jekyll
```

This is the image I'm using to connect `jekyll` with the LiveReload Chrome
extension to see updates immediately in the browser.

```
$ docker run --rm --volume=$(pwd):/src -p 4000:4000 -p 35729:35729
markkimsal/jekyll-plus
```

# Citation Required

The learning path I took to lead me to this setup includes the following
resources.

- [ ] [Official Jekyll Docs][jekyll]
- [ ] [Jekyll Github Repo][jekyll-gh]
- [ ] [Jekyll's Help Repository][jekyll-help]
- [ ] [Jekyll Docker Image Repos][jekyll-docker-gh]
- [ ] [Preview a Jekyll site with Docker on Windows][jekyll-docker-preview]
- [ ] [Build a Blog with Jekyll and GitHub Pages][jekyll-gh-pages] (aka Jekyll Now)


---
[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
[jekyll-docker-gh]: https://github.com/jekyll/docker
[jekyll-dh]:   https://hub.docker.com/r/jekyll/jekyll/
[jekyll-docker-preview]:  https://getcarina.com/docs/tutorials/preview-jekyll-with-docker-on-mac/
[jekyll-gh-pages]: https://www.smashingmagazine.com/2014/08/build-blog-jekyll-github-pages/
