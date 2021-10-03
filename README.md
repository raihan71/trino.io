# trino.io

<img alt="Trino Logo" src="./assets/images/trino-logo/trino-ko_tiny-alt.svg" width="15%" align="right" />

The source for the Trino community website available at
[https://trino.io/](https://trino.io/).

The site uses [Jekyll](https://jekyllrb.com/) and markdown.
It is hosted on [Netlify](https://www.netlify.com/).

## Build and run locally

In general, you need Ruby, gems, Bundler, Jekyll,
and [Netlify Dev](https://www.netlify.com/products/dev/).

Detailed steps for macOS follow below.
Similar commands work for various Linux distributions.

### macOS initial setup

Install Ruby in Homebrew:

```bash
brew install ruby
```

Add Homebrew Ruby in front of system Ruby:

```bash
PATH=/usr/local/opt/ruby/bin:$PATH
```

Install bundler:

```bash
gem install bundler
```

Install gems for site:

```bash
bundle install
```

Install Netlify CLI:

```bash
brew install netlify-cli
```

### Run server

Run server using Netlify Dev:

```bash
netlify dev
```

With the server running you can access the site on
[http://localhost:8888](http://localhost:8888).

## Additional notes

### Verify pages render correctly on phone

You can run the server on your computer and then verify the pages render
correctly on a phone. There are two ways to do that:

* Access the IP address of your computer on your local network from your phone.

* Run `netlify dev --live` to create a publically accessible tunnel that can
  be accessed from anywhere over the internet.

### View future posts

Posts with future dates do not normally render. You can override the default
Jekyll invocation to add the `--future` option to see these.

```bash
netlify dev -c 'bundle exec jekyll serve --future'
```
