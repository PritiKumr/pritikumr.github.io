---
layout: post
title: "Build and host your own site."
excerpt: "Websites are your identity that speak for you in the internet, setting them up can cost you much..."
categories: blog
tags: [jekyll, website, github pages, blog, static site]
author: preethi_kr
date:   2016-07-22 11:25:35 +0200
comments: true
share: true
modified: 2016-07-22T11:28:57-04:00
image:
  feature: how-to-build-website.png
---

## Build your own static site and host.

Basic command line control will be a really good start for this tutorial. We're gonna build a site and launch it. Firstly, let's do some analysis over the regular costing for building and hosting a small blogging site or personal website.

We're gonna make use of Jekyll for easily building our static site and Github Pages for hosting. 

	GitHub Pages is designed to host your personal, organization,
	 or project pages directly from a GitHub repository.

First, what's jekyll?

Jekyll is a static site generator. In simple, it gives us a ready to use website. Make slight tweaks and integrate any free themes. You are all set then. You think a walk through would be much better?

The jekyll documentation is a big help, although very confusing for someone with no technical knowledge.

* Prerequisites to run jekyll: 

	* You will need to install Ruby on your machine, because jekyll is powered by Ruby. Installing Ruby is really simple and follow this <a href="https://www.ruby-lang.org/en/documentation/installation">link</a> if your not sure how to start.

	* Also you need a package management framework for ruby to help you install the essential software packages. Follow <a href="https://rubygems.org/pages/download/">link</a> to download. 

After you follow these steps, moving around with Jekyll is pretty simple.

~~~ ruby
$ gem install jekyll
~~~

This will jekyll software package to your local machine. 

To verify if you have properly installed Jekyll in your machine, use the below command. make sure your command returns something similar to 'jekyll 3.1.6'

```ruby
$ jekyll -v
jekyll 3.1.6
```
As far as your static site generation is concerned, it is all set. Now, for web developers out there - you have two options.

1. Design your blog.
2. Download and use any free themes.

But if your really new to this, it's the latter that you got to deal with.

Jekyll has got a huge supported themes, choose your favorite and download them. Here is a quick <a href="http://jekyllthemes.org/">link</a> for fellow lazy minds. :P

This is the common directory structure of Jekyll,

	.
	├── _config.yml
	├── _drafts
	|   ├── begin-with-the-crazy-ideas.textile
	|   └── on-simplicity-in-technology.markdown
	├── _includes
	|   ├── footer.html
	|   └── header.html
	├── _layouts
	|   ├── default.html
	|   └── post.html
	├── _posts
	|   ├── 2007-10-29-why-every-programmer-should-play-nethack.textile
	|   └── 2009-04-26-barcamp-boston-4-roundup.textile
	├── _data
	|   └── members.yml
	├── _site
	├── .jekyll-metadata
	└── index.html

Any themes you download would contain similar directory pattern. This is the skeleton pattern, if you have a good understanding of jekyll you can customise the structure leaving the skeleton structure undisturbed.

### Generating your site.

You are just 3 commands away from creating your new site,

	$ jekyll new NewSite
	New jekyll site installed in /home/preethi/NewSite.

This site generates the scaffold needed for you, in simpler terms it creates the directory skeleton structure. Use the 'cd' command to move into NewSite directory and execute the following,

	$ jekyll build
	Configuration file: /home/preethi/NewSite/_config.yml
            Source: /home/preethi/NewSite
       Destination: /home/preethi/NewSite/_site
	 Incremental build: disabled. Enable with --incremental
	      Generating... 
	                    done in 1.361 seconds.
	 Auto-regeneration: disabled. Use --watch to enable.

The 'jekyll build' is the most important command that builds the destination site, the site that you've been trying to build now. Finally, fire up the server with the 'jekyll serve' command.

	$ jekyll serve
	Configuration file: /home/preethi/NewSite/_config.yml
            Source: /home/preethi/NewSite
       Destination: /home/preethi/NewSite/_site
	 Incremental build: disabled. Enable with --incremental
	      Generating... 
	                    done in 1.352 seconds.
	 Auto-regeneration: enabled for '/home/preethi/NewSite'
	Configuration file: /home/preethi/NewSite/_config.yml
	    Server address: http://127.0.0.1:4000/
	  Server running... press ctrl-c to stop.

That's it! Your server is running at port 4000. Your site is up. Add the styling that you want or use free themes. Change all site configurations in the '_config.yml' file.

All you have to do next is add your posts in the '_post' directory. Use 'jekyll build' command after every update to the site, to regenerate the destination site.

Push it to your github repository, create an orphan branch 'gh-pages' and push all settings to it. For more information on Github Pages hosting, refer to this guide.

	$ git checkout --orphan gh-pages

	# Creates our branch, without any parents (it's an orphan!)
	Switched to a new branch 'gh-pages'

	$ git commit -a -m "First pages commit"
	$ git push origin gh-pages

After your push to the gh-pages branch, your Project Pages site will be available at *http(s)://GithubUsername.github.io/ProjectName* . Note that Pages are always publicly accessible when published, even if their repository is private.

Happy building. :)
