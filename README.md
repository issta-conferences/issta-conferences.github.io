This is the website of the ISSTA conference series, hosted at https://www.issta.org/

The website uses a local, customized copy of the Minimal theme for GitHub Pages:
https://github.com/pages-themes/minimal 

The layouts, Sass, fonts, and JavaScript are maintained in this repository;
no remote theme download is needed. Dependencies are managed directly through
Bundler rather than the `github-pages` gem.

To preview the site locally, use Ruby 3.3 (see `.ruby-version`):
```
$ ./script/bootstrap
$ bundle exec jekyll serve
```

Then open http://127.0.0.1:4000 in your browser

Bootstrap uses the Bundler version from `Gemfile.lock` and installs dependencies
into `vendor/bundle`, without requiring administrator permissions. If Bundler
needs to be installed, bootstrap installs it for your user. If your shell cannot
find `bundle` afterward, add Ruby's user gem directory to your PATH:
```
export PATH="$(ruby -e 'require "rubygems"; puts File.join(Gem.user_dir, "bin")'):$PATH"
```

Run `bundle exec script/cibuild` to check the production build locally.

GitHub Actions builds pull requests and deploys pushes to `main` to GitHub Pages.
For initial setup, select **GitHub Actions** under **Settings → Pages → Build
and deployment → Source**. Keep the custom domain set to `www.issta.org`.
