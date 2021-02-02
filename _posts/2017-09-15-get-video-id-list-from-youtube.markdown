---
layout: post
title:  "Get video id list from youtube page"
date:   2017-09-15 09:58:13
categories: python
permalink: /archivers/get-video-id-list-from-youtube-page
---

```python
import os
import re
import urllib.request

f = urllib.request.urlopen('https://www.youtube.com/c/highwill76/videos')
contents = f.read().decode('utf-8')
urls = re.findall(r'watch\?v=([^"]+)', contents)
unique_urls = []
for url in urls:
    if url not in unique_urls:
        unique_urls.append(url)
        print(url)
```
