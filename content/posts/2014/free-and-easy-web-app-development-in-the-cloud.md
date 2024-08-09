---
title: 'Free and Easy Web App Development in the Cloud'
date: Fri, 17 Oct 2014 12:41:21 +0000
draft: false
tags: ['Uncategorised']
---

[Cloud9](https://c9.io/) is a cloud-based interactive development environment (IDE) with some killer features. Amongst these is the possibility of creating and hosting a WordPress blog completely free. The blog runs in a Ubuntu instance on [Docker](https://www.docker.com) and you have complete access to the WordPress’s PHP files using the very capable browser-based IDE. No need for virtual hosting, FTP, or any of that arcane stuff. The IDE provides terminal access to the Docker instance over ssh through the browser and there’s a MySQL database, Git support and built-in support for [Bitbucket](https://bitbucket.org) and [GitHub](https://github.com). Because it runs in a Docker instance, once your blog grows to need more services or more space, you can \[presumably\] export the docker file and import it into another cloud service. You can also use the WordPress export tools or git to export your blog to another hosting service.

Even better, the partnership with Bitbucket, which offers free unlimited private git repositories for anyone who signs up with an academic email address, makes Cloud9 a potential _killer app_ for institutions which teach coding. No tools to install, just a modern web browser and an internet connection.

Cloud9 comes with Docker images that can get you started quickly with many different web app frameworks. Django, Ruby on Rails, PHP, Drupal, Node and Angular.js are listed in the _create workspace_ feature. And provided your app is open source, there is no limit to how many workspaces you can have. The pricing policy is similar to GitHub’s in that respect.

My thanks to Michael Hartl who is using the Cloud9 infrastructure for the 3rd edition of the [Ruby on Rails Tutorial](https://www.railstutorial.org/) for the impetus to try Cloud9 out. I’m looking forward to getting my Group Design students signed up and building their micromouse blogs on it!