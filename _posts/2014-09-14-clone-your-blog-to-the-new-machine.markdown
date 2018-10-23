---
layout: post
title: "Clone your blog to the new machine"
date: 2014-09-14 15:28:30 -0500
comments: true
categories: coding
---
My baby air is too small, so I frequently delete wasted things, today, I delete some source... So I couldn't run rake generate anymore, so sad :(  
I looked up for recreating repo on a new machine, which is surprisingly easy.  
To recreate the local directory structure of an existing Octopress blog, follow these instructions.

Clone your blog to the new machine

First you need to clone the source branch to the local octopress folder.

	$ git clone -b source https://github.com/shadowind/shadowind.github.io.git octopress
Then clone the master branch to the _deploy subfolder.

	$ cd octopress
	$ git clone https://github.com/shadowind/shadowind.github.io.git _deploy 
Then run the rake installation to configure everything

	$ gem install bundler
	$ rbenv rehash    # If you use rbenv, rehash to be able to run the bundle command
	$ bundle install
	$ rake setup_github_pages
It will prompt you for your repository URL.

Enter the read/write url for your repository
(For example, 'git@github.com:your_username/your_username.github.com')
That’s you setup with a new local copy of your Octopress blog.
