

View the site at http://j12y.github.io/ 

Test locally on http://localhost:4000/ with official docker image
```
  $ docker run --rm --label=jekyll --volume=$(pwd):/srv/jekyll -it -p 127.0.0.1:4000:4000 jekyll/jekyll
```

Or with livereload working / connected with chrome browser extension
```
docker run --rm --volume=$(pwd):/src -p 4000:4000 -p 35729:35729
markkimsal/jekyll-plus
```
