---
layout: post
comments: true
title: MVC Solitaire Part I
---

[Klondike solitaire](http://en.wikipedia.org/wiki/Patience_%28game%29) is a specific type of [Patience](http://en.wikipedia.org/wiki/Patience_%28game%29) card game played with a standard 52 card deck. The object is to sort all suits from Ace to King in _foundations_. It's basically the solitaire that many Americans know and love.

[MVC or Model View Controller](http://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller) is a software architectural pattern for implementing software including a user interface. It's widly used in modern software products.

My goal with this article is to explore the MVC architecture using the Klondike solitaire game. In the first iteration, I'll create a completely playable command-line version of the game in Java. The second iteration will be a cross platform Android / iOS versoin using [libGDX](http://libgdx.badlogicgames.com/). The goal is for both iterations will use the same Model and Controller, but we'll have two Views; one for the Command Line version, and one for the libGDX version. As a special bonus, the APK on Android will also host the command line version and will be playable using the Android Debugger.

## Setup

The initial setup is dead simple -- a simple Java command line app that says, you guessed it, "hello world".

http://makble.com/gradle-junit-helloworld-example
