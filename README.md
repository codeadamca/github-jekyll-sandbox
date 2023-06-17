# GitHub Pages and Jekyll

> **Warning**  
> This repo is a work in progress!

A sandbox for testing out GutHub Pages and [Jekyll](https://jekyllrb.com/).

## Install Ruby

On a Mac use Homebrew to install Ruby 3.0. A Mac ships with Ruby, but it will be an outdated version. 

```sh
brew install ruby@3.0
```

We do want Ruby first in our PATH. Check which verion of Shell you are using:

```sh
echo $SHELL
```

If the result is `/bin/zsc`, run this command:

```sh
echo 'export PATH="/opt/homebrew/opt/ruby/bin:$PATH"' >> ~/.zshrc
```

If the result is `/bin/bash`, run this commant:

```sh
echo 'export PATH="$HOME/.gem/ruby/X.X.0/bin:$PATH"' >> ~/.bash_profile
```

> Note: The recommendation in your terminal may be slightly different than the above command. Use the version in your terminal.

Close your Terminal and reopen it. Check your version of Ruby:

```sh
ruby -v
```

You should see a version of 3.0 or highter. 

## Install Bundler and Jekyll

Run this command to install [Bundler](https://bundler.io/) and [Jekyll](https://jekyllrb.com/):

```sh
gem install --user-install bundler jekyll
```

If you Shell is zsh, run:

```sh
echo 'export PATH="$HOME/.gem/ruby/3.0.0/bin:$PATH"' >> ~/.zshrc
```

If your Shell is bash, run:

```sh
echo 'export PATH="$HOME/.gem/ruby/3.0.0/bin:$PATH"' >> ~/.bash_profile
```

## Create a Repo

Create a repo for this project and add the following for your `.gitignore`:

```
_site/
.sass-cache/
.jekyll-cache/
.jekyll-metadata
.bundle/
vendor/
.DS_Store
```
## Create a Jekyll Website

Run the following commands:

```sh
bundle init
bundle add jekyll --version "~>4.2"
bundle config set --local path 'vendor/bundle'
bundle install
bundle exec jekyll new --force --skip-bundle .
bundle add webrick
bundle install
bundle update
```

## Start the Jekyll Website

```sh
bundle exec jekyll serve --livereload
```

Open the provided URL in a browser, something like `http://127.0.0.1:4000/`, and start editing!

> This page is available to view at [https://jekyll.codeadam.ca](https://jekyll.codeadam.ca).

---

## Repo Resources

- [GitHub Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll)
- [Jekyll](https://jekyllrb.com/)

<a href="https://codeadam.ca">
<img src="https://codeadam.ca/images/code-block.png" width="100">
</a>
