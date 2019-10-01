---
layout: post
title:  "My Linux essentials"
date:   2019-09-29 22:45:02 +0200
categories: Linux OS Ubuntu-18.04.3-LTS setup essentials
---

### For two years I'm running Linux as my main OS and I haven't looked back since. These are the resources I need for my everyday Linux experience.

Before I made the transition to Linux approximately two years ago, I was running Windows 10 as my main OS. And guess what, I was completely fed-up with it. The constant updates had taken up all the space on my SSD. It got to the point that I had no space left to install the newest ones. My laptop was slowly dying, getting slower day by day and the worst thing about it: there was seemingly nothing I could do. So many times had I uninstalled and deleted stuff to have just enough space for the new updates and it had already dawned on me that this strategy will not work forever. I was right. It was about time to think about an alternative.

Up to that point I had heard of Linux before a few times, but essentially I was a complete Linux noob. I remembered that my older brother had been running a version of Ubuntu on his old desktop-computer quite a while back. He told me about concepts like "open source", different "Linux distributions" and "the terminal", but it was too much for me to grasp at the time. It was now time for me to make sense of all these buzzwords.

In the past two years I've already come quite a long way exploring the Linux-universe, however, there still remains a lot to be explored. After having tried different Linux distributions, including (obviously) [Ubuntu](https://ubuntu.com/download/desktop), Ubuntu-based [Mint](https://linuxmint.com/) and Arch-based [Manjaro](https://manjaro.org/), I have settled for Ubuntu 18.04.3 LTS on my Lenovo ThinkPad E490. At the moment I'm very happy with my setup. This happiness in not only based on Linux as an OS or Ubuntu as a specific distribution, but the high customizability in combination with the open source community which results in endless possibilities.

In this post I will list and comment on the (Linux) resources I personally can't live without. Primarily I do this for me, so that I have a place to collect and look up information in the case of setting up a new laptop/desktop-computer someday in the future. It's also a way of giving credit to the people who have created the software, which is all open source. Should anybody who reads this find some of it helpful or interesting, that's also a plus!

***
## The Mojave-dark GTK 3 theme

I'm generally a big fan of the [GNOME](https://www.gnome.org/) desktop environment (DE). However, I'm also a huge fan of the macOS/OS X design. Luckily, Ubuntu allows you to customize the design of the GNOME DE using [GONOME Tweaks](https://launchpad.net/gnome-tweaks). As I'm not the only person out there who likes the aesthetics of OS X but is not willing - nor able - to afford a mac, the internet host a vast amount of GTK 3 themes which are based on the OS X design. I'm currently using the '_Mojave-dark_' GTK 3 theme. You can find it in [this Github repo](https://github.com/vinceliuice/Mojave-gtk-theme) or on [www.gnome-look.org](https://www.gnome-look.org/), a website that hosts a huge collection of GTK 3 themes and more.

## 'pass' - Unix password manager

[pass](https://www.passwordstore.org/) is an easy-to-use PGP-encrypted command line password manager. I really like it's simplicity and the fact that it's extremely easy - yet very secure - to transfer a complete collection of passwords between devices. It takes some time getting used to, but I absolutely prefer pass over any of its GUI alternatives. I use pass every single day and by now it would be very hard for me to live without it.

## PDFjam

As a student you regularly have to print out all kinds of documents, mostly PDFs. To save some money - and of course paper - I usually like to combine 2 pages of the pdf-document on a single printed A4 page. Of course it's relatively easy to open the document and to specify everything in the respective print settings. However, [PDFjam](https://warwick.ac.uk/fac/sci/statistics/staff/academic-research/firth/software/pdfjam) makes it even easier to perform the described changes. More specifically, PDFjam allows you to do it in one line on your terminal. All you have to do is navigate to the directory which contains the document, open a terminal and type `pdfjam --nup 2x1 --landscape <name-of-document>`. A new document with the specified changes will be created in the same directory. You can also add `--suffix <your-name-extension>` to make it easier to differentiate between the old and the new document.
https://ankiweb.net/shared/info/295889520
## FoxitReader

[FoxitReader](https://www.foxitsoftware.com/pdf-reader/) is my simply my favorite PDF-reader.

## Zotero

[Zotero](https://www.zotero.org/) is a free and open source reference manager. I came across zotero when I was searching for a free and Linux-compatible reference manager to write my bachelor's thesis. I have used zotero ever since to manage my references for papers ect.

## Anki

[Anki](https://apps.ankiweb.net/) is a free and open source software that allows you to create, store and use digital flash cards on your computer or phone. If you're a student, you're probably already familiar with Anki. What initially kept me from using Anki regularly and consistently was the fact, that it can be quite a hassle to create all the individual flash cards without losing your focus while reading and making notes. Whenever I decided to create flash cards after the process of reading/making notes, I was often too lazy. At the moment I'm reading a lot about programming, maths and machine learning, which is why I have started to primarily use [jupyter notebooks](https://jupyter.org/) to take notes. In my jupyter notebooks I often convert cells to [Markdown](https://www.markdownguide.org/getting-started) to quickly summarize texts. The Anki add-on ['Auto Markdown'](https://ankiweb.net/shared/info/1030875226) allows you to write your Anki flash cards in Markdown. Because I create  a lot of my summaries in Markdown anyway, this add-on allows me to simply copy and paste into Anki to quickly create flash cards based on my summaries. In addition, I use the [Mini Format Pack](https://ankiweb.net/shared/info/295889520) add-o)n, which allows you to add a lot of additional features to your flash cards, such as: inserting blocks of code, text highlighting, creating ordered and unordered lists and more. With these two add-ons I'm able to create nice and handy flash cards without lots of extra work.

## fusuma

A I mentioned before, I'm a big fan of the aesthetics of macOS/OS X. This also includes the support of multi-touch gestures which allow you switch between tasks and/or workspaces. By default, Ubuntu allows you to switch between tasks and workspaces by combination of key presses, but not by multi-touch gestures. Luckily, [fusuma](https://github.com/iberianpig/fusuma) exists to allow you exactly this. Many thanks to [Kohei Yamada](https://github.com/iberianpig) for making it possible!

## Anaconda distribution

I use the [Anaconda distribution](https://www.anaconda.com/distribution/) for obvious reasons.

## Bash

After now roughly two years of using Linux, I have replaced a lot of the work that I would usually do via a GUI by using the command line/terminal. Ubuntu (like a lot of the other Linux distros and Unix systems) comes with [bash](https://www.gnu.org/software/bash/) as the standard shell. I highly appreciate the vast functionality of bash and I keep on exploring new ways of using it. One of my favorite resources to learn and look up the basic commands is [this article](https://dev.to/awwsmm/101-bash-commands-and-tips-for-beginners-to-experts-30je?utm_source=additional_box&utm_medium=internal&utm_campaign=regular&booster_org=) on [dev.to](https://dev.to/) by [Andrew William Watson](https://awwsmm.github.io/). Thank you Andrew for the great work!
