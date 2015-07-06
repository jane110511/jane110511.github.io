---
layout: post
title: Git ssh key
categories: diary
tags: job
---

change git from https to ssh

1. git remote rm origin
2. git remote add origin git@github.com:yuquan0821/demo.git
3. git push origin 

then generate a ssh key 

```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

```

and then push code if it show that you don't have permisson, 

```
Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
````

then add ssh key for git

```
ssh-add ~/.ssh/id_rsa
```

