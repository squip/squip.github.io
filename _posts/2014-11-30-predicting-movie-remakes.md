---
layout: post
comments: true
title: Predicting Box Office Success of Movie Remakes
---


Currently there are [over 15 original films](http://www.imdb.com/list/ls052091214/?start=1&view=detail&sort=release_date_us:desc&defaults=1&scb=0.48789280536584556) slated to be remade and released in the box office next year.  The current list for appoved cinema remakes over the next 5 years is 108 titles long. Despite the fact that remade movies appear to frequently underperform at the box office, movie studios are showing no sign of slowing down their frequency of producing remade films. Why would this be?  

Producing a film, like any other business, requires up-front capital and in an ideal scenario the investors want to make healthy returns on their investments with as little risk as possible. Movie remakes are simply considered less risky in the industry. The original movies they are based off of generally had been box office successes in their first incarnations, and already carry built-in public familiarity in their titles. Hence the assumption is that the original financial success of the original film can ultmiately act as a proxy for the relative success of the remake. But how accurate is this assumption, in practice?  

I decided to test the hypothesis by building a model that would attempt to use the box office success of an original film to accurately predict the box office success of its remake.  

## Obtaining the data

The first step in building my predictive model was to gather all the historical data I could on movie remakes.  As it turns out, Wikipedia has [an entry] dedicated entirely to listing and linking to (presumably) every movie remake produced, along with links to the original films.  I used the Beautiful Soup python library to scrape the contents of each individual movie url, extracting the budget and box office gross for each film. Since the time range of this list spanned nearly 100 years, and it was not uncommon for films to be remade decades after the release of the original, I needed to adjust all box office gross numbers for inflation, converting all earnings to be recorded in terms of US dollars in 2014. 


