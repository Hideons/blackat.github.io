---
layout: "single"
title: "Angular 2 Components"
date: "2016-10-22 14:58"
comments: true
categories:
  - Components
  - Angular2
tags:
  - component
  - angular2
---
Angular 2 has a new __design model__ to build applications. An application is just a _tree of components_, the root of the tree is the application itself.

{% include toc icon="gears" title="Contents" %}

## What Is A Component
_Components_ are fundamental building blocks of the application able to teach the browser a new _tag_. A component is __composable__, that is:

> a __component__ can be built up by one or more components in hierarchical fashion. An __application__ is a component made of a tree of other components.

An application can be designed through a tree of components, each component is responsible to _render_ a specific part of the page, the navigation bar for instance, and to do so it can use other components to split up the rendering work.

## Component vs. Directive
todo
