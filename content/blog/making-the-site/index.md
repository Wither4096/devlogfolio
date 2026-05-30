---
date: 2026-05-29T16:42:57+03:00
title: "Making the Site"
description: "how meta"
tags: ["devlog","guide"]
summary: "building this thing and hosting it"
---
I thought a good first post for a website would be explaining *how* it was built, and *why*, for the why?

### Because I wanted to.

## Stack

I tried to keep it as simple as possible, I hate working with the frontend and design aspects, and having a static HTML site seemed to be the easiest.

As you might have seen, the website uses [Hugo](https://gohugo.io) and [PaperMod](https://github.com/adityatelange/hugo-PaperMod/)

### and that's it

just a bit of theming here and there, and you're ready to publish.

Hugo fits surprisingly well here since it works on basically any OS, generates extremely tiny websites, and working with it feels just like editing conf files.

Other options I tried were [Astro](https://astro.build/) and building it using raw HTML, CSS, and JavaScript.

Quickly after starting to work with Astro I decided not to use it because of its dependency on Node.js and npm, then quickly scrapping the raw coding idea after realising I was not built for that.

### BUT WHY NOT \<TRENDY_STACK>? ARE YOU STUPID?!

Yes, and

### I'm lazy.

Maintaining a static website is not much more than creating markdown documents, and making minor edits to CSS stylesheets, and pressing Enter on 

```shell
git push
```
Nice and simple.

For my interests it was not worth the hassle of learning an entire new `language` + `framework` + `database` + `whatever` to deploy a site with a **crisp three** visitors per time unit.

## Hosting

There are genuine levels to this, **no I'm serious.**

- Simplest would be using [GitHub Pages](https://docs.github.com/en/pages), it's easy, [**FREE!**](https://www.youtube.com/watch?v=Bgqk6t9Be1Q), and automatically publishes the site after pushing changes to your repo, making it a set and forget solution, 99% of the time, 100% of the time.

- A step above without breaking the bank, would be using [Cloudflare Pages](https://pages.cloudflare.com/) with a cheap domain name, not only does Cloudflare offer CDN benefits, more limits for free, and other useful features.

- Want more control? Host on a VPS, this might be a better option for some users who might want to host game servers or privacy focused frontends for websites, letting you use the same machine for all services.

- The Final Step, host your own homelab server running a custom Linux From Scratch distro behind 7 proxies.

As for this site, I chose the second option since I already had the domain name from previous endeavors.

## Then how do I build it?

Everything is basically *Just Add Water!* with PaperMod, the only things done differently were the custom [Catppuccin](https://catppuccin.com/) inspired colour scheme.

Simply install Hugo using your preferred method, create a new project using YAML format, to easily reference PaperMod's documentation:

```shell
hugo new site your-site-name --format yaml
```

CD into it, clone a theme, again, PaperMod:

```shell
git submodule add --depth=1 https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
```

Configure your `hugo.yaml` to use the theme:

```yaml
theme: ["PaperMod"]
```

And now we start customising.

I used the provided [sample](https://github.com/adityatelange/hugo-PaperMod/wiki/Installation#sample-hugoyml) YAML configuration file, tweaking it, mostly removing features I didn't need.

After finishing that, we can start changing the theme by creating a CSS override file in the `assets/css/extended` directory:

- `catppuccin.css`

Creating custom post templates in `archetypes/`:

- `blog.md`
- `project.md`

Designing a favicon/logo and adding it to `static/`:

- `favicon/favicon-dark.png`
- `favicon/favicon-dark-16.png`
- `favicon/favicon-dark-32.png`

Creating the first post:

```shell
hugo new content/blog/hello-world/index.md
```

And finally publishing to Cloudflare Pages, basically reaching the point where the workflow is:

```bash
git add .
git commit -m "post: these pretzels suck"
git push
```

## Ok, How much does this cost then?

### About ~~tree fiddy~~ US$12.72 **per year**

The only costs are the domain registration fees for my chosen method, of course you can go cheaper with domains, completely free if you want to use the default Cloudflare or GitHub provided url, or utter financial ruin by hosting your own server equipment, Pick your poison.

## And that's it!

A simple, static, fast website built in under a day that didn't take too much effort to make. 

~~you can leave now.~~