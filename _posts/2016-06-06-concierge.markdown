---
layout: post
title:  "Apple Maps and Concierge"
---

# Apple Maps and Concierge

Ex-Apple Maps cartography designer Justin O'Beirne has put up [the first part in a long comparative review of Apple Maps and Google Maps][job] (which I wouldn't recommend opening if you're on mobile data as the page is huge), and that got me back into the app to examine my area again.

Apple Maps is unfortunately a punchline by default, and many people scoff when I say that I haven't really used Google Maps since it was removed in iOS 6. But it turns out that for the way I use map apps and for the areas I tend to be in, Apple Maps is more than capable of doing the job… in fact, a year ago I was working on an Apple Watch app based on Apple Maps to scratch my own itch called *Concierge*.

When I'm planning to go on a trip, I'll often build up a large Foursquare list with a list of places I want to check out. I find Foursquare's Explore view indispensable when it comes to finding out about good restaurants and places to hang out in cities I'm not familiar with, so that is often where I'll start, adding locations to the list as I go along. That is about the extent to which I plan my trips ahead of time.

Once I'm actually on the trip, I tend to rely on a map view of that list to group things I want to see by area. During my first trip to Japan, I'd often try to segment my day into two or three "areas", such as Jinbocho in the morning, Nakano in the afternoon, and Roppongi at night, trying to hit as many of the locations on my list in that segment of the day. I'd often create a "day list" for the locations of the day that I would check into throughout the day as a means of keeping track of what I had and hadn't done.

*Concierge* was meant to be a viewport into this workflow from my wrist. The app would automatically pull down the Foursquare list you'd set for the day, and show you the next venue on launch, with buttons to get directions in the transportation method of your choice or to check in to the venue. The full list would be a swipe away so you could jump ahead if you wanted to do things out of order for some reason.

This was going to integrate with Apple Maps, because at the time, there were no mechanisms for cross-app interaction on watchOS. Even if there had been a Google Maps app on the watch, there would be no way to invoke it from my app. Apple Maps is notoriously bad at point-of-interest search, and I feel like it is the primary reason people think it's a bad mapping service. There's a Subway two street corners away from my home, but searching for Subway in Apple Maps sends me all the way out to Taiwan. But because all of your POIs were found on Foursquare to begin with, you have the address or lat/long coordinates of the end locations already on hand, and Apple Maps is significantly better at handling those, so it was actually viable in this case.

What ultimately ended up happening with the app is far less exciting. I was trying to kill two birds with one stone and using this app as an excuse to learn both how to develop for watchOS *and* how to write Swift at the same time. But because Apple is so secretive, Swift and watchOS were being developed in parallel, unknowing of what the other was doing. Because of this, I had run into a bug where the interoperability between Swift and existing Objective-C frameworks like WatchKit made it impossible for me to handle an error that would always be thrown whenever you launched the app for the first time *or* updated it from the App Store. Needless to say, that and a handful of other annoyances in WatchKit really pissed me off, and I haven't really touched the app since. If anyone would like to run with the idea though, be my guest.

[job]: http://www.justinobeirne.com/essay/cartography-comparison

