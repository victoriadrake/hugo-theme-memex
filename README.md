# Memex, a Hugo Theme

## Git Started

Memex is a theme for [Hugo](https://gohugo.io/), a static site generator that helps make it easy to create a static website. See the [quickstart](https://gohugo.io/getting-started/quick-start/) to create your site then follow these three steps.

### 1. Add this theme

Add this theme to your Hugo site using Hugo Modules. First, initialize a new Hugo Module in the root of your site:

```sh
cd <whatever you named your site folder>
hugo mod init github.com/<username>/<repository name>
```

For example: `hugo mod init github.com/smallweborg/smallweborg.github.io`. Replace `github.com` if your site repository is hosted elsewhere.

Add these lines to your `config.toml`:

```toml
[module]
    [[module.imports]]
        path = "github.com/victoriadrake/hugo-theme-memex"
        disable = false
```

You're done! Run `hugo server` to see the magic.

### 2. Update your `config` file

Edit the `config.toml` file to name and customize your site. Here are all the different [Hugo config parameters](https://gohugo.io/getting-started/configuration/) you can set.

### 3. Write and deploy

[Add some content](https://gohugo.io/getting-started/quick-start/#step-4-add-some-content)!

When you're ready, you can deploy automatically with services like:

- GitHub Actions to [GitHub Pages](https://pages.github.com/). Just [configure your publishing source](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).
- [Neocities](https://neocities.org/) with or drag-and-drop upload.
- Other repository hosting services, like [GitLab Pages](https://docs.gitlab.com/ee/user/project/pages/) can also serve static sites.

## IndieWeb Features

Memex supports formats and protocols that encourage independent websites! To learn more about these, the community over at [IndieWebCamp](https://indieweb.org/discuss) is a great place to ask questions.

Here are the features Memex currently supports:

- Individual posts will render [Webmentions](https://www.w3.org/TR/webmention/) with support via [Webmention.io](https://webmention.io/)
- Your posts can be automatically shared with other social media thanks to [Bridgy](https://brid.gy/) (see more about Publish (on your) Own Site, Syndicate Elsewhere [(POSSE)](https://indieweb.org/POSSE) on the IndieWebCamp wiki)
- Your feed can be parsed by RSS and feed readers thanks to [h-card](https://microformats.org/wiki/h-card), [h-feed](https://microformats.org/wiki/h-feed), and [h-entry](https://microformats.org/wiki/h-entry) [microformats2](https://microformats.org/wiki/microformats2) markup
- You can log into supported services using [IndieAuth](https://indieweb.org/IndieAuth) [`rel=me` links](https://indieweb.org/rel-me) (they're in the [head](https://github.com/victoriadrake/hugo-theme-memex/blob/master/layouts/partials/head.html) file)

## Totally Optional Cool Stuff

Memex has out-of-the-box support for these features. You can turn them on by setting parameters in your configuration file.

### Web Monetization

[Web Monetization](https://webmonetization.org/) is a proposed standard that can let you receive micropayments when visitors browse your site. You'll need to [set up a wallet](https://webmonetization.org/docs/getting-started) that supports the Interledger Protocol (ILP).

Add your wallet's payment pointer to your `config.toml`, for example:

```toml
[params]
paymentPointer = "$wallet.provider.com/myspecialid123"
```

### IndieAuth Features

Don't forget to replace `example` below!

```toml
webmentionUrl = "https://webmention.io/example/webmention"
pingbackUrl = "https://webmention.io/example/xmlrpc"
micropubUrl = "https://example.com/.netlify/functions/micropub"
microsubUrl = "https://aperture.p3k.io/microsub/example"
```

### Social Cards

Rich embeds can provide additional information about your site if you set these parameters in the config:

```toml
description = "A description of this site."
socialImage = "static/img/social.png" # site image for rich embeds

# For IndieAuth too
githubuser = "username"
twitteruser = "username" # no @ in front
mastodon = "https://mastodon.technology/@username" # full link to your instance profile
```

## Contributing

You are absolutely encouraged to contribute to this friendly open source project!

### Values

As a project, Memex has these main goals:

1. Make it easy for people to ship a fun and useful website.
2. Make it easy to participate in the small web to encourage the creation of personal static sites.
3. Demonstrate excellent open source community practices and repository maintenance practices.

Any contribution that works towards these goals is welcome. See [CONTRIBUTING.md](https://github.com/victoriadrake/hugo-theme-memex/blob/master/.github/CONTRIBUTING.md) for details.
