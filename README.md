<img src="logo-readme.png" alt="CatSource"></p>

CatSource is an open-source blog for tutorials about, resources and more for the [Scratch](https://scratch.mit.edu) coding program.  
It is built as a static website on Jekyll (ruby), hosted on GitHub Pages.

The blog's posts are in the [content submodule](https://github.com/csourcesc/posts).

# Installation

These instructions are based upon Jekyll's [Quickstart guide](https://jekyllrb.com/docs/).

## Prerequisites
* Ruby 2.4.0 or higher
* RubyGems
* GCC and Make

More information and how to install them at [Jekyll's docs](https://jekyllrb.com/docs/installation/#requirements).

## Instructions 
1. Clone the repo  
`git clone https://github.com/csourcesc/csourcesc.github.io.git --recursive`
2. Install the jekyll and bundler gems  
`gem install jekyll bundler`
3. Go to the directory  
`cd csourcesc.github.io`
4. Install dependencies  
`bundle install`

# Run
1. Build the site and serve it  
`bundle exec jekyll serve`
2. In your browser, go to  
`http://localhost:4000`
