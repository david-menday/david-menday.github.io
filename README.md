# david-menday.github.io

Source for a GitHub Pages site built with Jekyll.

## Setup

Install Ruby `3.3.11` or use a Ruby version manager that reads `.ruby-version`.

Install the site dependencies:

```sh
bundle install
```

## Run Locally

Serve the site locally with live reload:

```sh
bundle exec jekyll serve --livereload
```

Jekyll will print a local URL, usually `http://127.0.0.1:4000/`. Open that URL in a browser to preview the site.

## Writing

Published posts live in `_posts/` and use Jekyll's date-prefixed filename format:

```text
YYYY-MM-DD-post-title.markdown
```

Use `_drafts/` for posts that are still being written and should not publish yet. Draft filenames do not need a date prefix.

To preview drafts locally:

```sh
bundle exec jekyll serve --livereload --drafts
```

When a draft is ready to publish, move it from `_drafts/` to `_posts/` and rename it with the publish date.

## Publishing

Push changes to the repository's GitHub Pages branch. GitHub Pages builds the site using the `github-pages` gem configured in `Gemfile`.

Generated local build files such as `_site/`, `.jekyll-cache/`, `.sass-cache/`, `.bundle/`, and `vendor/` are ignored by Git.
