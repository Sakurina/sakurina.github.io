---
layout: post
title: "Hashtag Dynamism in Swift"
---

# Hashtag Dynamism in Swift

Buckle up, kids. (I am going to try to keep this accessible to a non-developer audience, so if you've seen me snark about dynamism in Swift in the past, this might clue you into what I was going on about.)

The iOS and Mac developer community has been arguing for almost the entire year about Swift, the programming language Apple debuted at WWDC two years ago, and the direction it's headed in. The development process for Swift is arguably "un-Apple-like", with them doing [development in the open][open] (not [unprecedented][webkit], but uncommon) and letting the language get [shaped by the community][proposals]. But one thing the community is pushing hard, which Apple isn't really budging on, is that the direction Swift is headed is opposite to what made long-time Mac and iOS developers fall in love with developing on the platform, trading away Objective-C's flexibility at runtime (or "dynamism") for a more static code base that can be optimized for better performance, analyzed more thoroughly for bugs, and potential security benefits.

Here's an oversimplified explanation that will be sufficient for understanding the rest of the post: an application must be compiled before you can run it. A "static" program is one that is read only while it is running. Everything that can happen in that app must exist in its code before compilation in order for that possibility to exist when you run the app. A "dynamic" program is one that is *read and write* while it is running, and the program has the ability to modify its own structure and behavior as it runs. You can create a brand new function out of thin air in a dynamic program while it is running, and then if the program crashes in that function, the crash log will point you to a function that doesn’t even exist in the original code. (This may very well be one of the reasons Swift is backing away from that idea.)

As someone who built the first five years of my software development career off the back of the Objective-C runtime building [tweaks for jailbroken iPhones][icono] which are not easily replicated in a Swift world, you probably expect me to fall in the pro-dynamism camp, but my position is much more nuanced than that.
Objective-C was an incredibly elegant solution to the challenge of developing desktop-class applications in the late 80s and 90s, but time has moved on since then, and developers have grown to expect more from their developer tools, especially those flocking to Apple's platforms from other ecosystems to capitalize on the popularity of iOS. Apple has been trying to add modern features to Objective-C and its developer tools over the last decade, but many of the ones they introduced feel like they were merely patched onto an aging language, and they are still limited by all of the different ways things can change at runtime.

**Objective-C is fantastic as a tinkerer's language.** Objective-C hands you a massive toolbox with which you can architect applications and frameworks in really creative and clever ways, but implicit in that handoff is the trust that you'll do the right thing.

That's all fine and dandy but:

* Apple's products are increasingly completely sealed devices with little to no upgradeability once the device is shipped out from the factory to you.  It doesn't seem absurd to me that they would want to take the same approach with their software and shut out tinkerers. (In fact, a recently approved and [very controversial][vc] [Swift evolution proposal][sp] was about making classes (reusable components) provided by Apple or other developers "sealed" by default, therefore making them impossible to modify or expand upon unless explicitly stated in the code, whereas Objective-C classes are a complete free-for-all.)
* The app review policies reek of distrust towards their third-party developers, and looking at what's on the App Store, I'm not really surprised why. Any time Apple introduces a feature, there will immediately be people looking for ways to abuse it, even [at companies that should know better][twitter]. It doesn't seem absurd to me that they have given up on trusting developers to do the right thing, and are moving onto enforcement. 

While I don't necessarily agree with all of this, it's not clear to me why anybody in the developer community was surprised that this is the direction Swift is headed towards.

Don't get me wrong, I absolutely love Objective-C because I am a tinkerer at heart, and Objective-C affords me the freedom to do as I please with my code (or if I'm feeling naughty, the code of others). But when I'm *not* tinkering and I'm just trying to do my job, as much as it kills me to admit it, *the modern conveniences I gain from using Swift outweigh any kind of use I've gotten for runtime dynamism in Objective-C in that context*.

Since this debate has been going on for many months, the point has been made many times that a lot of Apple's own frameworks were written using Objective-C features that have no direct analog in the Swift world, and that a completely different (and perhaps less elegant) approach would be required to make those same frameworks work in a purely Swift world. Developers of large-scale applications may run into similar issues with their own code, so this is very much a "your mileage may vary" kind of thing. I'm fully aware of all these issues because I pay a nauseating amount of attention to the debate; my point with this post is not to close the case on dynamism in Swift, but rather to expose a wider range of people to the kinds of debates the development community partakes in and make my position public once and for all.

I refuse to comment on the other hot topic of debate in the Apple community: [the bread at Subway][subway].

[open]: https://github.com/apple/swift
[webkit]: http://www.webkit.org
[proposals]: https://apple.github.io/swift-evolution/
[icono]: http://r-ch.net/iconoclasm.html
[twitter]: https://support.twitter.com/articles/20172069
[sp]: https://github.com/apple/swift-evolution/blob/master/proposals/0117-non-public-subclassable-by-default.md
[vc]: http://mjtsai.com/blog/2016/07/17/swift-classes-to-be-non-publicly-subclassable-by-default/
[subway]: http://atp.fm/episodes/169
