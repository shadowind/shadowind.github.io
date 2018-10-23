---
layout: post
title: "Custom Domain with Octopress and Github"
date: 2014-09-15 08:36:20 -0500
comments: true
categories: 
---
Setting up your Custom Domain with Octopress and Github

If you’re cool using the Github subdomain then feel free to stick with it. However if you’d like to point a custom domain at your blog then here’s how to go about it.

Create a new file in the source folder named CNAME. Add your domain name to this file. In my case the only contents of my CNAME are robdodson.me. If you’re trying to use nested domains or subdomains you may need to refer back to the Octopress documentation.
```
echo 'your-domain.com' >> source/CNAME
# OR
echo 'www.your-domain.com' >> source/CNAME
```
Now lets go through the familiar steps for deploying…

```
bundle exec rake generate
bundle exec rake deploy

git add .
git commit -am 'Create a CNAME record for my custom domain'
git push origin source
```

If you visit your repo you should see the CNAME record in the root of the master branch now (Octopress has copied it over for us as part of the generate task).

Next you’ll need to update the DNS for your domain. Head over to your domain registrar and fire up their DNS manager. For a top level domain like robdodson.me we need to create an A record which points to the address for Github Pages: 204.232.175.78. Save that change and now…we wait… Unfortunately, DNS can take several hours to update. If all goes according to plan then in a few hours “your_name.github.com” should resolve to “your_custom_domain.com”.

A few quick gotchas…

If you’re using Dreamhost then you may need to set the hosting preferences for the domain to DNS only. See this thread for more explanation.

If adding www to the beginning of your domain seems to break things then make sure that your domain registrar has a CNAME record for www which points to your A record. I’m not a DNS expert but I think this is the proper way to set that up.

Make sure you spelled your domain name correctly in the CNAME record that you pushed to Github. I spent almost an hour wondering why robodson.me wasn’t resolving :\

If all else fails checkout the docs from Github Pages and [Octopress]('http://octopress.org/docs/deploying/github/') on setting up a custom domain.