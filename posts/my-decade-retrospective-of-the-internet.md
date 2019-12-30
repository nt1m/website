---
title: My decade retrospective of the internet
description: A nostalgic look back at everything that happened on the internet in the last 10 years through the eyes my childhood.
date: 2020-01-01
tags:
  - internet
  - childhood
  - retrospective
layout: post.njk
---

Five years ago, I was applying for university and had to write [a personal statement](https://www.ucas.com/undergraduate/applying-university/how-write-ucas-undergraduate-personal-statement) to distinguish myself from other candidates. What led me to write this blog post was the following section:


> At the age of nine, I used to make startpages using Microsoft Word so my mother could easily access her links. A year later, I looked for better ones online, and found one on deviantART that I downloaded. I got curious about how it worked, so I explored the HTML code and got thrown into the amazing world of web development and web design! That deviantART online community has been a great place of exchange where I got to collaborate and interact with different computer enthusiasts, coders and digital artists, on various projects. […]

— An overly enthusiastic 15 year-old me applying for university

It’s almost 2020 — the end of a decade — I’m about to be 20 and I’ve (hopefully) grown a lot in the past 10 years. Looking back, I now see how much the internet changed at the same time. My childhood was mostly centered around the internet, sometimes feeling like it was my only raison d’être: I probably had more online friends than real life ones. Anyway, I thought it’d be interesting to provide my retrospective of the internet through the things I’ve achieved and the people I’ve met. This post has a big nostalgic vibe to it, but I’m particularly proud of what the last decade has been for me.

# The web stack
<figure class="float-right">
<img src="../uploads/my-decade-retrospective-of-the-internet/metrostart.png" alt="MetroStart, one of my first startpages"/>
<figcaption>MetroStart, one of my first startpages</figcaption>
</figure>

The personal statement quote first mentions start pages made using Microsoft Word. Start pages are web pages with quick links that you set as your homepage. While Microsoft Word might sound like a surprising choice for developing web pages, the bar for website authoring was quite high at the time. The software I found was either commercial (e.g. [Adobe Dreamweaver](https://en.wikipedia.org/wiki/Adobe_Dreamweaver)) or difficult to use. Coding was out of my league at the time. Online website creators like [Webs](https://www.webs.com/) or [Netvibes](https://www.netvibes.com/) — while easy to use — did not provide enough flexibility in terms of the content you could add but I would recommend those to my mom to build her own site.
Luckily, Microsoft Word had a web mode that allowed you to export a document as an HTML file, which made making a website as easy and flexible as making a Word document.

When I joined [deviantART](https://www.deviantart.com/) in 2011 to find and post startpages, I looked at the code others had written and realized Microsoft Word was generating a lot of junk. This led me to start learning coding along with a few folks I had met on deviantART. Taskin Forkan ([daKoder](https://www.deviantart.com/dakoder/)) was one of them, he was around the same age and originated from the New York Area. We had developed an online dashboard together — that had evolved into an online desktop — named [Altaica](http://altaica.altervista.org). Conceiving, developing and designing Altaica together was an amazing learning experience. We both learnt [jQuery](https://jquery.com/)/[jQuery UI](https://jqueryui.com/) while I actively opposed using the [Bootstrap framework](https://getbootstrap.com/) since it was a lot of unnecessary code. Both of these frameworks were the state of the art as they made web APIs much easier to leverage. jQuery has since died off as newer DOM and JS APIs were introduced to fill the gap (Github wrote a great post on how they [removed jQuery from their front-end](https://github.blog/2018-09-06-removing-jquery-from-github-frontend/)).

Another technology we attempted to add to our online desktop was logging in to save user data on the cloud and make it more useful to users. This required server-side development, which we both had a small understanding of. We attempted to add a login system using PHP — popular at the time — but the stack evolved so quickly with newer technologies coming around that we never actually got around to learning it. Nowadays, the server-side stack has gotten even easier with adding a login system being as simple as following a [15 minute AWS Amplify tutorial](https://learn.acloud.guru/course/coding-for-cloud-101/dashboard). Hosting would be provided for free by [Altervista](https://en.altervista.org/) — a site simobortolo on deviantART showed me — and deploying those websites would be done with FTP. Those tasks are today done with automatic solutions like [Heroku](https://www.heroku.com/).


<figure class="float-right">
<img src="../uploads/my-decade-retrospective-of-the-internet/20-year-old-commit-message.jpg" alt="Added the ability to drag splitters. If any build problems call me at: 650 224-0620"/>
<figcaption>20-year old commit message from the Mozilla source code</figcaption>
</figure>


Contributing to the Firefox front-end has also been a very enriching experience, as I got to learn how a large codebase like Firefox’s deals with 20-year old technologies while still being able to evolve everyday. I learnt to use [React](https://reactjs.org/), a framework made by Facebook in 2013 that Firefox DevTools had started using instead of the [legacy XUL](https://developer.mozilla.org/docs/Archive/Mozilla/XUL). React aimed to solve single page application design with [Vue.js framework](https://vuejs.org/) being its main competitor. I had also contributed to the [XBL replacement work](https://bgrins.github.io/xbl-analysis/) in Firefox that [finished last October](https://briangrinstead.com/blog/firefox-webcomponents/). This was done with the [web components spec](https://developer.mozilla.org/docs/Web/Web_Components) — making the need for frameworks questionable — especially when compatibility with older browsers isn’t an issue. If there’s something to take away from frameworks on the web, is that they come and go, with web standards never dying off.

In 2010, I saw the rise of HiDPI and Retina screens. My first patches for Mozilla were about adding HiDPI support in Firefox, by adding a second higher resolution PNG along with a media query. The inconvenient need for a pair of files for every graphic popularized [SVG](https://developer.mozilla.org/docs/Web/SVG) — with Google’s [Material Icons website](https://material.io/resources/icons/) being one of the first big icons library, inspiring me to create the original version of the [Photon Icons website](https://design.firefox.com/icons/viewer/#), called Firefox SVG Icons at the time.

The web stack has very much evolved in the security space as well. I remember having links in my Microsoft Word start pages that would launch desktop apps directly when clicked (this is an odd use of a web page, but my mom wanted to have everything centralized in one place). This is no longer possible today without explicit user consent for security reasons. The Firefox codebase also started blocking `innerHTML` to prevent XSS attacks, which proved useful since my younger self accidentally [introduced](https://bugzilla.mozilla.org/show_bug.cgi?id=1029371) and [fixed](https://bugzilla.mozilla.org/show_bug.cgi?id=CVE-2017-7798) such a vulnerability. More recently, [CSP](https://developer.mozilla.org/docs/Web/HTTP/CSP) was enforced in all Firefox internal pages for more strict security.

Finally, I saw web tooling get tremendously better. The DOM inspector, Firebug and Chrome DevTools were the only tools available a decade ago. Today, we now have more beginner friendly tools I wish I had at the time, like the [inactive CSS feature](https://www.youtube.com/watch?v=O3DAm82vIvU) or more visual tools like the [animation inspector](https://developer.mozilla.org/en-US/docs/Tools/Page_Inspector/How_to/Work_with_animations). During my first internship, I also got to work on [Janitor](https://janitor.technology/), which makes use of cloud technology to make hacking on large projects easier.

The web stack has evolved so significantly in the last decade and I don’t know if I would have noticed that if I hadn’t started customizing start pages.

# The rise and fall of software customization

When I joined deviantART in 2011, I originally found [this start page](https://www.deviantart.com/flatmo1/art/EIGHT-start-page-UPDATE-212847573) which was [one out of many](https://www.deviantart.com/popular-all-time/?section=&global=1&q=start+page). I eventually started posting my own under the username ntim007. While the account is now disabled, some content is [available on web archive](http://web.archive.org/web/20120312053400/ntim007.deviantart.com/). deviantART had a growing community of digital art involving software customization: from [icon sets](https://www.deviantart.com/dakirby309/art/Metro-UI-Icon-Set-725-Icons-280724102), [skin packs](https://www.deviantart.com/peterrollar/gallery/), [userstyles](https://www.deviantart.com/link6155/art/MD-for-Allo-Web-699481294), [wallpapers](https://www.deviantart.com/dakoder/art/MinFlat-Dark-Material-Design-Wallpaper-3-4K-523306773) to [redesign concepts](https://www.deviantart.com/link6155/art/Concept-Modern-Beige-683147792). This inspired me to post my own work inspired by the current design trends over the years, from Metro UI, Apple translucent designs to Material Design. I never thought I’d meet someone who posted this type of digital art in real life, but I surprisingly did meet [this Canadian](https://www.deviantart.com/sepen77/) just last year during my exchange.

Firefox also had a large customization ecosystem, it supported add-ons, userstyles and complete themes. My first XUL overlay add-on — then converted to Jetpack — was a simple button that leveraged the now defunct YouRepeat service. Customization was time consuming but it was very satisfying once you were done. Three years ago, my Firefox setup looked like this:

<div class="flex">
  <img src="../uploads/my-decade-retrospective-of-the-internet/custom-firefox-1.jpg" class="grow">
  <img src="../uploads/my-decade-retrospective-of-the-internet/custom-firefox-2.png" class="grow">
</div>


Point being, there was a big culture of software customization at the time. Some even made some revenue from their themes like for the [Deep Dark themes](http://stefrosselli.com/en/themes). However, this culture slowly died off, along with the customization community on deviantART and Google+. Firefox legacy extensions and themes both became obsolete with Firefox 57, a move that enabled removing legacy code (XUL/XPCOM). Despite that, there are still some subreddits remaining like [r/Unixporn](http://reddit.com/r/Unixporn), [r/FirefoxCSS](http://reddit.com/r/firefoxcss) or [r/androidthemes](https://www.reddit.com/r/androidthemes/) (Thank you Omkar for showing me that last one!), but those are a regular time investment due to needing to keep up with the more frequent software updates.

# Web browsers

When I was eight, I was already passionate about web browsers: I would compulsively read Wikipedia articles about them and download every single one on the family’s computer, including older ones like Netscape. At that time, Google Chrome was just released with a simple and sleek design that ditched the menu bar and introduced tabs on the top. Opera pioneered innovations like tabbed browsing, the speed dial or tab stacking. Firefox used add-ons to innovate: the first web developer tools came from [Firebug](https://getfirebug.com/) and cross-device bookmark sync came from [Delicious](https://en.wikipedia.org/wiki/Delicious_(website)). IE did not innovate and relied on a monopoly that Google Chrome took over 10 years later.

When you saw how browsers like Chrome or Opera innovated, Firefox had to change their innovation model to not rely on its extension ecosystem, since most users wouldn’t install extensions. In 2011, Firefox 4 started going in this direction with the transition to faster releases. The Mozilla UX team started doing regular design experiments, with the short-lived UX channel setup for it. I’d be a big fan of their work, especially designs made by Stephen Horlander and Alex Limi, to a point I’d copy CSS values from interactive mockups into my own projects. Add-on wise, most common use cases were analyzed and retained into the product. Bookmark syncing and web developer tools became built-in features. Built-in light and dark themes were introduced to fill the gap for custom themes. Since I was quite passionate about theming, I worked on the WebExtension theme API by adding what I needed for my add-on [VivaldiFox](https://github.com/nt1m/vivaldi-fox). I even wrote [blog](https://hacks.mozilla.org/2017/12/using-the-new-theming-api-in-firefox/) [posts](https://hacks.mozilla.org/2018/01/a-rule-based-framework-to-create-dynamic-themes/) and gave a [talk](https://www.meetup.com/Firefox-France-User-Group/events/248069582/) about it. Eventually, in 2017, Firefox Quantum successfully ditched this extension system, with innovation going towards privacy and security features.

With resources being constrained and innovation shifting elsewhere, most desktop browsers now feature the same overall layout as 10 years ago. However, there are a few concept browsers challenging this. I worked with the developer of [DocLayer](https://standaert.net/doclayer/), a minimalist document editor that connected with Dropbox, to provide what he needed in [my CSS framework](https://github.com/nt1m/material-framework). He’s a very creative developer who later made [Min Browser](https://minbrowser.github.io/min/), built on top of [Electron](https://electronjs.org/), featuring a minimalist one-liner design and a task-based multitasking UI. One other concept browser I really liked was [Opera Neon](https://www.opera.com/computer/neon)‘s attempt to re-imagine desktop web browsing and optimize it for today’s needs. In the mobile space, the [Firefox Preview browser](https://play.google.com/store/apps/details?id=org.mozilla.fenix), built from the ground up, tries to rethink mobile browsing, notably with its innovative UI and its collections feature.

This change in innovation models was partially a result of the rapid release model that Chrome had first adopted in the browser market and is a general transformation seen in the software industry in the past decade.

# Faster software development

In 2012, the first collaborative project I had ever done was [Online Windows 8](http://onlinewindows8.altervista.org), created with Taskin Forkan ([daKoder](https://www.deviantart.com/dakoder)), Anthony Nguyen ([link6155](https://www.deviantart.com/link6155)) and Sean Loper ([GrimmDev](https://www.deviantart.com/grimmdev/)). It’s not the project I’m the most proud of today, but I got to learn how to collaborate through Dropbox as we noticed we were losing time sending each other ZIP files (we didn’t know about Git yet). Yet, despite the low quality of the project, it had received thousands of downloads on deviantART. Tech youtubers even [created videos to promote the project](https://www.youtube.com/watch?list=PLdn7yGD-OqWQj_h_2YBoSGxpDDPKEX_QN&v=TwMG3OgJ1vc). I had wondered why for quite a while, and then I recalled seeing comments complaining that this wasn’t actually a usable version of Windows 8. Many folks who downloaded the project were probably looking for online free cracked versions of Windows 8:

<figure>
<img src="../uploads/my-decade-retrospective-of-the-internet/online-windows-8-email.png" alt="Hello windows8team i need to download windows 8 html please"/>
<figcaption>The need was there ;)</figcaption>
</figure>

This got me thinking about whether something like this would actually be successful today. Windows upgrades used to be paid for consumers a decade ago, until Windows 10 was released in 2015, when all updates from Windows 7/8 were delivered for free. Windows 10 was the very last major version of Windows, with all subsequent updates being much smaller and delivered very frequently “as a service”. This was a positive move as it would prevent businesses from being stuck on very old versions of Windows and allowed everyone to benefit from regular innovation.

Faster update cycles might now be obvious today, but it is quite radical how they’ve changed in the last decade. It’s crazy to think that a decade ago, Firefox released a new version only every year and now do every 4-6 weeks today.

# Product diversity on the internet

One thing that characterized this decade is the loss of product diversity on the internet, which led to the domination of the web by large companies. Exactly 9 years ago, I built my own search engine called [SmartSearch](http://smartsearch.altervista.org). The idea was largely copied from [Maxthon Multi Search](http://s.maxthon.com/): both sites allowed you to easily compare results from different search engines. While the idea by itself wasn’t super useful, my 10 year old mind somehow had an obsession in knowing all the search engines that existed out there, which is how I discovered Maxthon Multi Search. The Chinese web browser originally provided their feature [as a separate website](http://s.maxthon.com/) similarly to SmartSearch and later built-in the feature into Maxthon 3.

<img alt="Maxthon multi search in Maxthon 3" src="../uploads/my-decade-retrospective-of-the-internet/multi-search.png" class="float-right" style="max-width: 40%">


Maxthon’s [main pitch for the multi search](https://www.youtube.com/watch?v=5e2_njWFAKM) feature was being able to compare results across engines which may be useful to compare prices between different shopping search engines like Amazon or ebay. This feature is no longer present in the latest version of the web browser. This may show two things, the slow monopolization of search engines (Google for search, Amazon for shopping) but also Google’s aggregated information display reducing the need of browsing the sites themselves. While this does provide a lot of convenience, it does also seem scary for the health of the internet.

However, while developing SmartSearch, I was able to leverage open data from [DuckDuckGo’s instant answers API](https://duckduckgo.com/api) from which I made [a small library](https://github.com/nt1m/InfoCards.js). It provides Google-style knowledge card data when searching for terms. Seeing alternatives to Google openly sharing their results gives me hope for the health of the internet. DuckDuckGo’s results are in fact provided by Bing just like Ecosia’s results are, which is a great initiative from Microsoft.

<figure>
<img src="../uploads/my-decade-retrospective-of-the-internet/duckduckgo-smartsearch.png" alt="Integration of DDG’s instant answers API in SmartSearch"/>
<figcaption>Integration of DDG’s instant answers API in SmartSearch</figcaption>
</figure>

<figure class="float-right">
<img src="../uploads/my-decade-retrospective-of-the-internet/mozilla-paris-office.jpg" alt="The gorgeous former Mozilla Paris office"/>
<figcaption>The former Mozilla Paris office</figcaption>
</figure>

Another story relating to product diversity was the rise and fall of Firefox OS six years ago. It was Mozilla’s attempt at making a strong mobile competitor to Android and iOS. The idea was pretty neat: the web was the platform and apps were websites. Since Mozilla was doing a large company-wide push on Firefox OS at the time, I got invited by [Paul Rouget](https://github.com/paulrouget) to the Mozilla Paris office, from which I brought home a [Firefox OS Flame](https://developer.mozilla.org/en-US/docs/Archive/B2G_OS/Phone_guide/Flame) device to help report bugs. I remember using it as my daily driver where I’d flash the latest beta builds to try them out.

Mozilla also made a push by attracting developers who could expand their app ecosystem to be competitive enough. I contributed by developing an [unofficial app for Vine](https://twitter.com/andypiper/status/515133411242307585) on Firefox OS, ported from Altaica. I also attended an app workshop at the Mozilla Paris office, where the creator of [2048](https://dolske.net/hacks/browser2048/), Gabriele Cirulli, came and gave a presentation on Firefox OS apps. My current phone is a Sony Xperia Z3C, which was part of the many hardware partnerships Mozilla had made.
Despite this push, Firefox OS was discontinued and I even saw an employee throw a Firefox OS Flame into the donation box during an office clean up in Mountain View. Big companies took advantage of the integration to their large ecosystem of services to dominate the mobile market. Android benefited from Google service integration while iOS benefited from iTunes. I saw more and more news sites (e.g. The Independent, Valeurs Actuelles, etc.) use [AMP links](https://amp.dev/) by default, a mostly proprietary technology for which Google made the push by [ranking those websites higher up in their search results](https://searchengineland.com/will-amp-improve-rankings-set-amp-test-289869).

Due to this large ecosystem [FAANG](https://en.wikipedia.org/wiki/Facebook,_Apple,_Amazon,_Netflix_and_Google) already benefit from, making independent products like [Qwant](https://www.qwant.com/) is attempting is not enough by itself as a pitch. Innovation or reaching audiences that FAANG don’t dominate is the key to competing today. A successful startup based on Firefox OS’ legacy is [KaiOS](https://www.kaiostech.com/), a mobile OS for flip phones. It targets emerging markets like India where it managed to reach the second place ahead of iOS and behind Android. Despite Google and Apple being in this field, the financial market has seen successful startups like [Transferwise](https://transferwise.com) (which I’ve used in the past year to travel), differentiating itself by providing fee-less international transfers, or [Monzo](https://monzo.com/), providing an innovative way of displaying your spending. Seeing these competitors shows hope for the future health of the internet.

# Online communities

What remains diverse on the web today are the people in online communities like [deviantART](https://deviantart.com) or the now defunct Google+.

Google+ was a failed attempt to compete with Facebook: “communities“ were similar to Facebook “pages“, while “circles” were similar to “friends”. It wasn’t mainstream, but many digital artists would post art on there since Google had a better image than Facebook in the tech sphere. This is where I got to know [Carlos Jeurissen](https://carlos.jeurissen.co/), the developer of the award-winning browser extension [Black Menu For Google](https://apps.jeurissen.co/black-menu-for-google) and a great human I had the chance of meeting in real life last year. He is a very experienced developer, to a point that while trying to solve a problem for his extension, he found a security bug in the Google APIs and got invited to a security meetup. He currently passionately lives off from freelance and extension work.

Over the last decade, with the rise of online platforms, creating content online like YouTube videos (e.g. [Ryan Higa](https://www.youtube.com/user/nigahiga) who I started watching in 2010) or code have become things you can independently live off from. For others, it has become a hobby, like for [Taskin Forkan](https://www.deviantart.com/dakoder), who is studying “Neuroscience & Psychology” at the Johns Hopkins University and aims to become a doctor:

> Nowadays the stuff I do in regards to coding is running websites for my university or stuff in my psychology lab where we use basic web design and java and matlab for various experiments. […] It’s so weird that for me all that stuff is still a hobby because that’s how I prefer it, yet somehow it still helps me out while working in unrelated fields.

Through [Meetup](https://www.meetup.com) or [Mozilla events](https://wiki.mozilla.org/All_Hands), I’ve met people in real life with the same interests and many interesting profiles, which has largely shaped who I am today.

<figure class="float-right">
<img src="../uploads/my-decade-retrospective-of-the-internet/brexit-ad.png" alt="There are fewer than 20 days to prepare for Brexit"/>
<figcaption>Brexit advertisement in Bristol from October 2019, which still hasn’t happened</figcaption>
</figure>

Despite the good things online communities have brought, the UK got into this Brexit mess and Trump got elected, partially due to internet fake news or bots that led to indirect election meddling targeting older generations, widening the pre-existing generational gap. Hopefully, the future will see more legislation correcting this, like [Twitter’s recent move to ban political ads](https://twitter.com/jack/status/1189634360472829952).


# Takeaways

You’ve made it to the end! Evolution is not necessarily impressive when you passively lived alongside it. To me, seeing the internet evolve over the last decade has been an amazing learning and human adventure. This is just the tip of the iceberg and I’m sure others have seen things change in their own ways. I’m really looking forward to see what the next decade has to bring and I hope that the internet can evolve to be healthier and more diversified.

Big thanks to [Justin Dolske](http://dolske.wordpress.com), [Taskin Forkan](https://www.deviantart.com/dakoder), [Omkar Konaraddi](https://konaraddi.com/), [Stephen Zhao](https://www.zhaostephen.com/), [Carlos Jeurissen](https://carlos.jeurissen.co/), [Dennis Jackson](https://github.com/galadran), [Faizaan Sakib](https://github.com/fznsakib), [Ainsley Rutterford](https://github.com/ainsleyrutterford) and [Oussama Ben Guirat](https://ousben.github.io/) for providing their great input.
