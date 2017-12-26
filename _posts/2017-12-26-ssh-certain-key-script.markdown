---
layout: post
title: ssh certain key script
---
use git command through certain key
	ssh-agent bash -c 'ssh-add /somewhere/yourkey; git clone git@github.com:user/project.git'
