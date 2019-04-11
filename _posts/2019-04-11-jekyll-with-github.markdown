---
layout: post
title:  "Jekyll with Github"
date:   2019-04-11 15:51:00 +0800
author: klin0816
comments: true
categories: jekyll github tutorial
---
### Installation
Install jekyll on [localhost](http://localhost) and test running
! the blog name should be [username.github.io]
```shell
    # installation on Mac
    # install jekyll modules
    $ sudo gem install bundler jekyll
    
    # start project
    # might ask sudo password to install
    $ jekyll new [username.github.io]
    
    # run project
    $ cd [username.github.io]
	# for build first time only
	$ bundle exec jekyll serve
	# for other time run server
	$ jekyll serve
    # browser open 127.0.0.1:4000 to check 
```

### Github
Open a **clean** github repo without any initialize including README.md
```shell
    # connect jekyll to github repo
    $ git init
    $ git add .
    $ git commit -m '[commit-message]'
    $ git add remote origin [remote-repo-URL]
    $ git push -u origin master
    
    # Enter [username.github.io] to see your website
    # Maybe need couple minutes to wait your website available
```

TIPS: commit everytime to check the change is too annoying, run your website *localhost* seems better. Just commit once after you complete one of your post.
TIPS2: the server is watching server, so you can run your server up and feel free to change your blog contain, server will rerender automatically after saving.

If you are as lazy as me, and used to use `yarn` or `npm` in web-development, you can use the setting below like me.
```shell
	$ yarn init
	...
	...

	# package.json
	...
	"scripts": {
		"build": "bundle exec jekyll serve",
		"start": "jekyll serve",
	},
	...

	# run server
	$ yarn start
```

### New Post
There is a rules for jekyll post, the post naming rules is `[data-title.markdown]` as example `[2019-01-01-hello-world.markdown]`.
In the post, there is also a template for post
```
---
layout: post
title:  "Hello World"
date:   2019-01-01 12:00:00 +0800
author: [author]
comments: [true/false]
categories: [catagory1 catagory2 catagory3 ...]
---
```
I created a template for new post and named `template` in `_posts`, so i just need to copy the template and can create a new post in a fast speed.

### Blog Setting

