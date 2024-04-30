---
layout: post
title: Using renv for Reproducible Environments in R
date: '2024-04-30'
categories: Protocols
tags: [Coding]
---

## Using renv for Reproducible Environments in R

I am starting a new Github Repository for my Chapter Three analysis, and wanted to initate this repository with a version-controlled, reproducible R environment. I am using the tutorial found [here](https://rstudio.github.io/renv/articles/renv.html).

![renv.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/protocols/renv.png?raw=true)

First, I made a new github repository. Inside this repository, I created a new Rproject through Rstudio, located at "Path/To/Repo/reponame.Rproj".

Then, in Rstudio, I ran the following code to install the package renv

```
install.packages("renv") #install the package on the new computer
```

Then, within the Rproject and in the Repository folder, I ran the following code to initialize the renv reproducible environment for this repository.

```
renv::activate() #
renv::init() #initialize the renv directory, lockfile (renv.lock), and .Rprofile files
```

Then, I pushed all changes to gituhb and theoretically this is now a working reproducible environment such that any packages I use in this code and the versions of those packages can be used by anyone pulling from the github repo.

As I continue to write code and work on the project, I will follow the guidance below:

"As you continue to work on your project, you will install and upgrade packages, either using install.packages() and update.packages or renv::install() and renv::update(). After you’ve confirmed your code works as expected, use renv::snapshot() to record the packages and their sources in the lockfile."

- To install packages: install.packages() or renv::install()
- To update packages: update.packages() or renv::update()
- To record changes in code to the renv environment/lockfile: **renv::snapshot()**
- And regularly push changes in the code and renv files to github

To run the code in my project on another computer using the renv environment, run the following lines of code

"Now when one of your collaborators opens this project, renv will automatically bootstrap itself, downloading and installing the appropriate version of renv. It will also ask them if they want to download and install all the packages it needs by running renv::restore()."

```
install.packages("renv") #install the package on the new computer (may not be necessary if renv bootstraps itself as expected)
renv::restore() #reinstall all the package versions in the renv lockfile
```