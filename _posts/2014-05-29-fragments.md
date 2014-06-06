---
layout: post
comments: true
title: AnDevCon talk on Fragments
---

_I gave a talk on Android Fragments on May 29, 2014 at AnDevCon in Boston. The talk was well attended and well received. You can download the [slide deck](https://github.com/johnnylambada/andevcon-2014-jl/blob/master/slides/fragments.pdf) from the presentation if you like._

Life used to be simple. We had Activities and they were good. You could define all of your app's UI in a layout and animate it in an Activity. Then Apple brought out the iPad and Google answered with Honeycomb. Things got complex. Google realized that tablets would drive the need for developers to reuse parts of their UI, and the answer was the Fragment class. Fragments enable developers to use bits of UI along with the associated business logic in various parts of their app or even in multiple apps.

The Slide deck has a matching [github repository](https://github.com/johnnylambada/andevcon-2014-jl) that has several really useful example projects in it. The easiest way to build the examples is with Android Studio and gradle.

## [fragment-logged](https://github.com/johnnylambada/andevcon-2014-jl/tree/master/fragment-logged/src/main/java/andevcon14/FragmentLogged)

This example app uses native fragments to demonstrate several concepts:

1. Dynamic vs Static Fragments: Static fragments are created with the `<fragment>` tag in a layout. Dynamic fragments are added at run time to a `<frame>` tag.
2. Using a Bundle to store Activity state information throughout the Activity's lifecycle.
3. The interrelationship of the Activity lifecycle with the Fragment lifecycle. There is a really useful set of classes ([CallLogger](https://github.com/johnnylambada/andevcon-2014-jl/blob/master/fragment-logged/src/main/java/andevcon14/FragmentLogged/CallLogger.java), [LoggedActivity](https://github.com/johnnylambada/andevcon-2014-jl/blob/master/fragment-logged/src/main/java/andevcon14/FragmentLogged/LoggedActivity.java) and [LoggedFragment](https://github.com/johnnylambada/andevcon-2014-jl/blob/master/fragment-logged/src/main/java/andevcon14/FragmentLogged/LoggedFragment.java)) that enable you to log calls from lifecycle events without adding any code to your Activities and Fragments themselves.
4. How the Back button and configuration changes (screen rotation) affect the Activity and Fragment lifecycles.

## [fragment-comms](https://github.com/johnnylambada/andevcon-2014-jl/tree/master/fragment-comms/src/main/java/andevcon14/FragmentComms)

This example app demonstrates five styles of communicating data between Activities and Fragments.

![Fragment Communication Chart](/assets/fragment-comms-chart.jpg)

* [ActivityIntent](https://github.com/johnnylambada/andevcon-2014-jl/tree/master/fragment-comms/src/main/java/andevcon14/FragmentComms/Types/ActivityIntent) - How to communicate to a fragment through the Intent that started the Activity.
* [FactoryMethod](https://github.com/johnnylambada/andevcon-2014-jl/tree/master/fragment-comms/src/main/java/andevcon14/FragmentComms/Types/FactoryMethod) - Communicate build arguments to a Fragment in a way that will survive the Activity and Fragment lifecycles.
* [ObserverPattern](https://github.com/johnnylambada/andevcon-2014-jl/tree/master/fragment-comms/src/main/java/andevcon14/FragmentComms/Types/ObserverPattern) - Two way communication between any combination of multiple Fragments and Activities using the standard Java Observer pattern.
* [LayoutElements](https://github.com/johnnylambada/andevcon-2014-jl/tree/master/fragment-comms/src/main/java/andevcon14/FragmentComms/Types/LayoutElements) - Communicate static build arguments to a Fragment by placing them in the Layout.
* [SetArguments](https://github.com/johnnylambada/andevcon-2014-jl/tree/master/fragment-comms/src/main/java/andevcon14/FragmentComms/Types/SetArguments) - Using the setArguments call on the Fragment itself to give it arguments available to it during the entire lifecycle.
* [LocalBroadcast](https://github.com/johnnylambada/andevcon-2014-jl/tree/master/fragment-comms-support/src/main/java/andevcon14/FragmentCommsSupport/Types/LocalBroadcast) - Available only when using the Support Library, LocalBroadcast enables the Observer Pattern without the need for the participants to keep track of Observers.

## [fragment-comms-support](https://github.com/johnnylambada/andevcon-2014-jl/tree/master/fragment-comms-support/src/main/java/andevcon14/FragmentComms)

This project is just like the fragment-comms project except that it uses the support library.

## [hall-of-mirrors](https://github.com/johnnylambada/andevcon-2014-jl/tree/master/hall-of-mirrors/src/main/java/andevcon14/HallOfMirrors)

The hall-of-mirrors example demonstrates that Fragments can be nested within other Fragments.
