---
layout: post
comments: true
title: AnDevCon talk on Android Studio
---

I gave a talk on Android Studio on May 28, 2014 at AnDevCon in Boston. The talk was well attended and well received. You can download the [slide deck](https://github.com/johnnylambada/andevcon-2014-jl/blob/master/slides/android-studio.pdf) from the presentation if you like.

This post reemphasizes my main point during the talk.

## The best reason to switch to Android Studio today is Gradle integration.

Even though it's still considered Alpha software (as of 6/5/2014), the Android Gradle plugin is ready for prime time, and is much better than the current Android Ant plugin. Gradle builds are somewhat faster than Ant builds, and there are a lot more features. The best reason to use Gradle with Android Studio is the you only have to worry about one build. Normally you have to get your command line build working if you want continuous integration, and your IDE build is separate. It's not difficult to maintain both on simple projects, but on complex projects it can be tedious. Adding a new library can easily break everyone's IDE build, so there is a tendency to leave things alone once a project gets to a certain size.

Because Android Studio uses your Gradle project to build, once you have the Gradle build working, you also have an Android Studio project set up. All the developer has to do is import the top level `build.gradle` file and away he goes.

