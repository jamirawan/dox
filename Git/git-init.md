---
layout: default
title: Git init
parent: Git
nav_order: 1
has_children: fals
has_toc: true

---


# Git Init
{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

Inititating git workflow either for a new project or existing


## Adding existing project to collaborate (Github)

1. Create a new repository on Github, I'll call my repository `nasigoreng`
2. Navigate to the working directory with command line and initialise Git:
```bash
git init -b main
```
3. Add the files in the local repostiory, this will stage them for the first commit:
```bash
git add .
```
4. Then commit them
```bash
git commit -m "Initial commit"
```
5. Copy the URL of the repository you set on step 1. For example `git@github.com:jamirawan/nasigoreng.git`
6. Then go back to the terminal add git remote on the folder you just committed:
```bash
git remote add origin git@github.com:jamirawan/nasigoreng.git

# then check the remote:
```bash
git remote -v

```

and it should be:
```bash
origin	https://github.com/jamirawan/nasigoreng.git (fetch)
origin	https://github.com/jamirawan/nasigoreng.git (push)
```

7. Push your commits to the upstream origin then your branch:
```bash
git push -u origin main
```


## When you created a repository on Github, it comes with instruction below

**Quick setup — if you’ve done this kind of thing before**
Get started by creating a new file or uploading an existing file. We recommend every repository include a README, LICENSE, and .gitignore. 


**…or create a new repository on the command line**
```bash
echo "# iirawan" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:iirawan/iirawan.git
git push -u origin main
```
**…or push an existing repository from the command line**
```bash
git remote add origin git@github.com:iirawan/iirawan.git
git branch -M main
git push -u origin main
```
**…or import code from another repository**

You can initialize this repository with code from a Subversion, Mercurial, or TFS project.
`Import code`
