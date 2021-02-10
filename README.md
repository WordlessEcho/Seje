# 寫嘢 - Seje
寫嘢（Se2'Je5）, A beatutiful Hexo Theme

## Install
1. Open your Hexo flodder and Execute the following command：

```bash
git clone https://github.com/eatradish/Seje.git themes/Seje
```

2. Open your hexo `_config.yml`, set `theme` value as `Seje`:

```yaml
theme: Seje
```

3. Using `hexo s` see if it works.

### If you using disqus
1. Set your disqus_shortname in your `_config.yml` of `$BLOG/themes/Seje` :
  ```yaml
  disqus_shortname: $YOUR_SHORTNAME
  ```

2. Using `hexo s` see if it works.

### Excerpt vs. Content?
Does every post on your homepage need to show a summary or a whole post? You can modify it in `_config.yml`. The default is to display a full post. You can change it to this in your `$HEXOFLODDER/themes/Seje` to display the summary.

```yaml
excerpt: true
```

### Favicon
Copy your `favicon.png` to `$BLOG/source` or `$BLOG/themes/Seje/source`

Now you can set the file name of favicon yourself, just modify the value of `favicon` in the theme` _config.yml`, and copy your file to `$BLOG/source` or `$BLOG/themes/Seje/source`

### Code Highlight
This code highlighting is implemented using [highlight.js](https://highlightjs.org/), If you want to turn on code highlighting, please add the `highlight` in `$BLOG/_config.yml`:

```yaml
highlight:
  enable: true
  hljs: true
```

### Podcast

Seje support podcast feature (thanks [shikwasa](https://github.com/jessuni/shikwasa)!), A case of using podcast on Seje:

1. install hexo-generator-podcast in your blog foldder:

```bash
yarn add hexo-generator-podcast
```

and set podcast as true on theme `_config.yml`:

```yaml
podcast: true
```

2. Set your Podcast info in your blog `_config.yml`, like this:

```yaml
podcast:
    type: rss2
    path: podcast.xml
    limit: 20
    hub:
    url: https://URL/to/static/resources
    description: 
    language: zh-CN
    copyright: "COPYRIGHT"
    owner: ITUNES-OWNER
    email: ITUNES-EMAIL
    category: CATEGORY
```

3. `hexo new "podcast-test"` and add the following example to the markdown file created:

```
---
title: podcast test
date: 2020-06-19 16:23:38
tags:
subtitle: SUBTITLE
category: podcast # must be exactly `podcast`
media: /path/to/media # placed under //URL/to/static/resources/path/to/media
image: /path/to/episode/image # same as above, but somehow itunes doesn't support episode image as it should do
length: 6989--IN_BYTES
type: audio/mpeg
duration: XX:YY:AA
author: AUTHOR
---
一个 Podcast 实例：
{% podplayer %}
```

### Bug
- Please use `git pull` regularly. Bug fixes are guaranteed.
- Issues / Pull requests are welcome
