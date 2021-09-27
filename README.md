# Flumen

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/D1D35CFF1)

A newsfeed and aggregator for the digital humanities by [Codex Felis](https://www.codexfelis.dev)

## Contributing

### Add a feed

TL;DR Here's an [example pull request](https://github.com/codexfelis/flumen/pull/2) which adds a new feed

- find the URL of the feed you want to add (see below for tips)
- fork this repo (see the [GitHub documentation](https://docs.github.com/en/github/collaborating-with-pull-requests) if you need more help with this)
- add a line to the `osmosfeed.yaml` file that looks the same as the other lines which have feed URLs in, in alphabetically sorted order
- run `npm i` then `npm run build` to make sure everything is valid, the site builds and ideally you get some new items for that feed. The build shows you how many new and cached items are found for each feed, which looks like

```sh
...
[discover-cache] Pre-build cache restored: https://codexfelis.github.io/flumen/cache.json
[enrich] 0.67s |  11 cached |   0 new | https://eadh.org/feed
[enrich] 0.70s |  10 cached |   0 new | https://openmethods.dariah.eu/feed/
[enrich] 1.03s |   2 cached |   0 new | https://judaicadh.github.io/feed.xml # ^ existing feeds
[enrich] 1.64s |   0 cached |  10 new | https://dhcommons.hypotheses.org/feed # <- new feed with new items
...
[main] Finished build in 6.75 seconds # <- successful build
```

- commit this change and push to your fork, then make a pull request to this repository

### Request a feature

If you know things about code, have a look at the [osmosfeed-examples](https://github.com/osmoscraft/osmosfeed-example) repository and try to figure out if what you want is vaguely possible within the constraints of the framework we are using. In any case, [open an issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/creating-an-issue#creating-an-issue-from-a-repository) on this repository and we will look into it. Feel free to also add the feature yourself and send us a pull request if you know how, but please raise the issue first, in case we are already working on the same thing

## FAQ?

### What even is RSS?

An RSS, or Really Simple Syndication, feed is a text file representing the content on a website, that automatically updates when new content is added. RSS feeds are universally supported in web standards and allow applications and users to follow updates from a website's content.

### How do I find an RSS feed for a site?

- look for the RSS logo: <a href="https://icons8.com/icon/13841/rss">RSS icon by Icons8</a>

<img src="https://img.icons8.com/color/48/000000/rss.png"/>

- change the URL - add `/feed` or `/rss` or `/rss.xml` and hope you get something that looks like XML or your browser offers to download
- Look in the source code - view the HTML source of the page then search for `rss`

### Can I make an RSS feed for my own website?

Sure! Most website frameworks or builders will make this easy to do - you might even have one and not have noticed yet. Get in touch with us at [hi@codexfelis.dev](mailto:hi@codexfelis.dev) if you need help, and of course send us a pull request to add your website here too!

### Tell me more about this site

This site is generated using [osmos::feed](https://github.com/osmoscraft/osmosfeed) from [osmos::craft](https://osmoscraft.org/)

- [How does it work?](https://github.com/osmoscraft/osmosfeed#osmosfeed)
- [Lastest documentation](https://github.com/osmoscraft/osmosfeed)
- [Deploy your own feed aggregator](https://github.com/osmoscraft/osmosfeed-template/generate)
