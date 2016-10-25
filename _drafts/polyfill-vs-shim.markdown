---
layout: "single"
title: "Polyfill vs. Shim"
date: "2016-10-24 07:11"
comments: true
categories:
  - JavaScript
tags:
  - polyfill
  - shim
---
With the new ES6 specification, people talk more and more about polyfill and shim, sometimes as the term are interchangeable but, are they the same thing?

{% include toc icon="gears" title="Contents" %}

## Polyfills and shims
There are many definitions and interpretation about what is Polyfill and shim. Agree that both are libraries there are some differences between them.

{% capture notice-text %}
  - has a new API;
  - is strictly tailored for an _old environment_;
  - is a _graceful degradation_.
{% endcapture %}
<div class="notice--info">
  <h4>Shim:</h4>
  {{ notice-text | markdownify }}
</div>

#### Polyfill
  - [is a shim for a browser API](http://www.2ality.com/2011/12/shim-vs-polyfill.html);
  - is related to browsers;
  - [replicates an API using JavaScript (or Flash or whatever) if the browser doesn't have it natively](https://remysharp.com/2010/10/08/what-is-a-polyfill);
  - is something that [you could drop in and it would silently work](https://remysharp.com/2010/10/08/what-is-a-polyfill);
  - is not related only to old browsers, even latest browsers need a polyfill too.

## Polyfill, back to 2010
The term _polyfill_ comes from a [2010 blog post](https://remysharp.com/2010/10/08/what-is-a-polyfill) by [Remy Sharp](https://twitter.com/search?q=%40rem&src=typd) where Remy Sharp was looking for a new term or word:

> I wanted a word that meant "replicate an API using JavaScript (or Flash or whatever) if the browser doesn't have it natively.
...
> I wanted something you could drop in and it would silently work.

The term _shim_ doesn't work for him because:

> I knew what I was after wasn't progressive enhancement because the baseline that I was working to required JavaScript and the latest technology. So that existing term didn't work for me.

So Remy gives the following definitions:

> A __polyfill__, or polyfiller, is a piece of code (or plugin) that provides the technology that you, the developer, expect the browser to provide natively. Flattening the API landscape if you will.

> Poly meaning it could be solved using any number of techniques - it wasn't limited to just being done using JavaScript, and fill would fill the hole in the browser where the technology needed to be. It also didn't imply "old browser" (because we need to polyfill new browser too).

> __Shim__, to me, meant a piece of code that you could add that would fix some functionality, but it would most often have __it's own API__.

## Other definitions

> I like classify __polyfilling__ as a form of Regressive Enhancement
>
> <cite>[Alex Sexton](https://twitter.com/SlexAxton/status/25600963629)</cite>

> A __shim__ that mimics a future API providing fallback functionality to older browsers.
>
> <cite>[Paul Irish](http://paulirish.com/)</cite>

> A __polyfill__ is code that detects if a certain "expected" API __is missing__ and manually implements it. E.g.   
> `if (!Function.prototype.bind) { Function.prototype.bind = ...; }`
>
> A __shim__ is code that intercepts existing API calls and implements different behavior.
>
> The idea here is to normalize certain APIs across different environments. So, if two browsers implement the same API differently, you could intercept the API calls in one of those browsers and make its behavior align with the other browser. Or, if a browser has a bug in one of its APIs, you could again intercept calls to that API, and then circumvent the bug.
>
> <cite>[Sime Vidas](http://stackoverflow.com/questions/6599815/what-is-the-difference-between-a-shim-and-a-polyfill/17331540#17331540)</cite>

> A __shim__ is a library that brings a new API to an older environment, using only the means of that environment.
>
> A __polyfill__ is a shim for a browser API. It typically checks if a browser supports an API. If it doesn’t, the polyfill installs its own implementation. That allows you to use the API in either case.
>
> <cite>[Axel Rauschmayer](http://www.2ality.com/2011/12/shim-vs-polyfill.html)</cite>

## Polyfills and shims libraries
[Paul Irish](http://paulirish.com/) provides a [list of HTML5 cross browser polyfills and shims](https://github.com/Modernizr/Modernizr/wiki/HTML5-Cross-browser-Polyfills).
