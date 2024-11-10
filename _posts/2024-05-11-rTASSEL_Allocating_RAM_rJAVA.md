---
title: 'Navigating rTASSEL rJAVA allocation of memory issue in ubuntu'
date: 2024-05-11
permalink: /posts/2024/05/creating_your_website/
toc: True
excerpt_separator: <!--more-->
tags:
  - webpage
  - academic pages
  - github
  - git 
---

Mere humans computational problem
I was having issues configuring rJava to allocate memory. I follow the steps below to fix it. Unfortunately, these steps have to be repeated every time Rstudio is restarted, but at least it works.

Run each line in the console
```{r}
remove.packages("rJava", lib="~/R/x86_64-pc-linux-gnu-library/4.4")
Sys.setenv(JAVA_HOME='/usr/lib/jvm/java-17-openjdk-amd64')
remove.packages("rTASSEL")
install.packages("rJava")

```


```{r}
library(rJava)
.jinit(parameters="-Xmx30g")
```


Confirm that the specified memory was allocated.
```{r}
maxAllocRam <- .jcall(.jnew("java/lang/Runtime"), "J", "maxMemory") / 1e9 
message("You have ", round(maxAllocRam, 2), "GB memory available.", sep = "")
```


```{r}
if (!require("devtools")) install.packages("devtools")
devtools::install_github(
    repo = "maize-genetics/rTASSEL",
    ref = "master",
    build_vignettes = TRUE,
    dependencies = TRUE
)
```


```{r}
library(rTASSEL)
```