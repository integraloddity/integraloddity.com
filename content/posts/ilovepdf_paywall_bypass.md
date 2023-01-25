---
title: "Business Logic bugs: Bypassing Ilovepdf's paywall"
date: 2021-12-08
# weight: 1
# aliases: ["/first"]
tags: ["business-logic", "bypass", "mobile", "fun"]
category: ["blog"]
author: "5hyl0ck"
showToc: false
TocOpen: false
draft: false
hidemeta: false
comments: true
description: "A tale of love, loss and unlimited pdf processing"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: true
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: false
ShowPostNavLinks: true
cover:
    image: "" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page

---

## Intro
This article details how I bypassed the paywall present in Ilovepdf’s mobile application for the amount of daily PDF processing tasks possible and explains the specific vulnerability type involved: "business logic" 


## Story Time
A couple of days ago, I was helping my mom do some clerical work with PDFs (because I’m the good child and my siblings are useless). Being stuck on an unfamiliar device with none of the apps that I’m used to, I did a quick glance of the play store and downloaded the first app that looked like it didn’t have malware in it (as the competent security professional that I am.) and I ended up with  [Ilovepdf](https://play.google.com/store/apps/details?id=com.ilovepdf.www). Its business model is freemium with functionality locked based on amount of tasks performed per day and requiring payment for performing additional tasks. 

Here is an image of the paywall: 


![paywall exemplar image](/paywall.png)


I immediately decided that, since the paywall is locked behind tasks carried out “per day”, the application might be using the system time of my device as opposed to contacting some API or server somewhere on the internet for the accurate time (this would require internet access for an application whose functionality is largely local and would reduce the application’s usability). This led to testing out whether changing my device time would impact the recorded tasks already carried out (surprise surprise, it did) In effect, I was able to use the application an unlimited amount of times without paying for additional access just by disabling automatic date and time setting on the android device and changing the day to one not used before. 


Here is a [video](/paywall.mp4) detailing the entire process.

I know this is not the most earth shattering bug, but it leads to a discussion of what is perhaps my favourite bug type: business logic bypass. 

## Explaining business logic vulnerabilities

According to [OWASP](https://owasp.org/www-community/vulnerabilities/Business_logic_vulnerability)
> ... business logic vulnerabilities are ways of using the legitimate processing flow of an application in a way that results in a negative consequence to the organization.

and according to [Portswigger](https://portswigger.net/web-security/logic-flaws)
> Business logic vulnerabilities are flaws in the design and implementation of an application that allow an attacker to elicit unintended behavior. This potentially enables attackers to manipulate legitimate functionality to achieve a malicious goal. These flaws are generally the result of failing to anticipate unusual application states that may occur and, consequently, failing to handle them safely. 

It involves fully understanding the underlying business rules behind an application's functionality and manipulating them to achieve some unforseen goals (presumably malicious) that the application cannot defend itself against. The beauty of this vulnerability type is the fact that it does not require sophisticated technical knowledge or complicated automated tools, all you need is a good eye for detail and critical thinking skills. Also, the effects of business logic flaws range from mild annoyances to full application compromise. If you want to learn about business logic bugs and other interesting web security stuff, [Portswigger Academy ](https://portswigger.net/web-security/logic-flaws) has a lot of comprehensive resources (for free !)

TLDR; if an application locks functionality behind time based parameters, it’s always a good idea to test how changing your system time affects said functionality.


Happy hacking ! 