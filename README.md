#jameh.github.io
This is my little blogging site, hosted here on Github! The site uses [Jekyll][1] to generate blog pages from Markdown files and [Liquid Templates][2]. All the site generation is done server-side by [Github Pages][3], so the repo stays nice and clean.

##Usage
###Jekyll setup
To most accurately replicate Github's server-side setup for development purposes, follow the instructions [here][4] - quickly, clone the repo

```bash
git clone https://github.com/jameh/jameh.github.io
cd jameh.github.io/
```

and install the "github-pages" gem using bundler

```bash
gem install bundler
bundle install
```

Then serve locally at <http://0.0.0.0:4000>:

```bash
bundle exec jekyll serve
```

###Markdown Blog Posts
To add a post to be published, create a .md file in `_posts` with the naming convention "yyyy-mm-dd-title.md", and include the YAML header at the top of the file like so:

```md
---
layout: post
title: Hello, World.
---
#Testing, *123*.
```

Then run:

```
bundle exec jekyll serve --watch
```

To deploy to Github, just push to your pages repo (note the repo name "username.github.io", see [Github Pages][3])

```
git push
```

For more in-depth (bottom-up) instructions, see the [Jekyll docs][5].

[1]: http://jekyllrb.com/
[2]: http://liquidmarkup.org/
[3]: http://pages.github.com/
[4]: https://help.github.com/articles/using-jekyll-with-pages#installing-jekyll
[5]: http://jekyllrb.com/docs/home/
