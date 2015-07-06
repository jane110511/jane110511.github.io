---
layout: post
title: New Job
categories: diary
tags: job
---

change git from https to ssh

1. git remote rm origin
2. git remote add origin git@github.com:yuquan0821/demo.git
3. git push origin 

then generate a ssh key and add ssh key 

```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
ssh-add ~/.ssh/id_rsa
```

and then push code use git shell, for windows command it show that you don't have permisson, 
```
Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

````
i can only work under git shell.

