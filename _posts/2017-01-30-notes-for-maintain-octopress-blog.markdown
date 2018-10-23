---
layout: post
title: "Notes for maintain Octopress Blog"
date: 2017-01-30 11:14:56 -0700
comments: true
categories: 
---
I haven't touched this blog for 2 years, memories fade quickly. 
Although this is wierd, the website link is <https://shadowind.github.io/index.html>, for some reason, I can't access it right now. It keeps redirecting me to my previous domain "www.sumi.im". This is very annoying since I didn't continue to purchase this domain. 

Update: CNAME is a file to store the domain, I deleted this file. commit and rake deploy again. Then use google incoginite window, it finally able to not redirecting me the that expired domain


### Create new blog:

```sh
rake new_post["title"]
# Creates new post on source/_posts/2017-01-30-notes-for-maintain-octopress-blog.markdown
```

### Generate & Preview
```sh
rake generate   # Generates posts and pages into the public directory
rake watch      # Watches source/ and sass/ for changes and regenerates
rake preview    # Watches, and mounts a webserver at http://localhost:4000
```

### Upload to github
```sh
$ git add .
$ git commit -m 'message'
$ git push origin source
```

### deploy again
```sh 
$ rake deploy
```

### Change theme

I found it very easy to change theme, there are bunch of 3rd party themes, for example I used this one:
<https://kaworu.github.io/octostrap3/>. 

Paste image in post
I used this website <http://imgur.com/>