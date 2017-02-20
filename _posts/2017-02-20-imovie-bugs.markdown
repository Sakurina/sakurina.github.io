---
layout: post
title: "Technical Difficulties"
---

As I've mentioned in the past, I've been hard at work on a video series called [Swan Song](http://swansong.ws) focused on covering every WonderSwan game released in chronological order. So far all of the seven episodes in the series have had their audio and video fully edited on the iPad Pro, but there have been some difficulties in the process, which is what I'm going to go over today.

Perhaps the most irritating of the bunch is how iMovie on iOS handles rendering transitions between clips. You may have noticed a few instances in Swan Song episodes where volume spikes up inexplicably during a video transition. It took me a while to figure out what was causing it, but I think I've gotten a better understanding of what the issue is.

iMovie for iOS doesn't re-render transitions on every minor modification made to a clip, as that would be very wasteful of computing resources, especially when on battery power. Some flag needs to be set behind the scene for iMovie to trigger a re-render, and it appears adjusting the volume on either clip in a transition doesn't set that flag.

Furthermore, you can't just select another transition type and switch back to the transition you wanted, because the app keeps track of the rendered transition in the background to avoid re-rendering something if you press the undo button.

Here are the workarounds I have found for this issue:

* **Tier 1:** If the bulk of your video involves one giant clip that you eventually plan to split into smaller ones, set the volume on the giant clip before splitting it. This ensures the implicit transitions between each clip iMovie automatically inserts when a clip is split are rendered at the correct volume. You may experience issues if you do further volume tweaking after the fact, which is where you must fallback to tier 2.
* **Tier 2:** Drag the start/end handles of the problematic clips a tiny amount to force a re-render of the transition. This is really easy and is probably the best solution if you aren't relying on precise edits. This is unlikely to be helpful if you made your frame-perfect transitions in the Precision Editor *before* balancing your audio volume.
* **Tier 3::** Set all of your transitions to No Transition. Exit the project, double-press the home button, and force quit out of iMovie. This will clear the undo buffer for the transitions you changed. Go back into iMovie, open your project, and set the transitions back to what they were before. This should force a re-render.
* **RNG-dependent wildcard:** This might work as long as your project doesn't include any clips you've sped up or slowed down for reasons that will become obvious shortly. In the gear menu in the top toolbar, there is an option called "Speed changes pitch". Triggering this option *can* cause transitions to re-render randomly, however it is unreliable. I only mention it because it is the simplest, coming in at two taps.

But at the core of it all, transitions, which are a basic building block of iMovie projects have been bugged for months, and that doesn't inspire confidence in the more advanced features like picture-in-picture. Any normal user would have noticed the issue with transitions and given up on the app then and there.

It's unfortunate. The debate surrounding the iPad's viability for work has risen up again in recent weeks due to the lamentations of neglected Mac users and the continuation of unimpressive iPad sales numbers. While I could certainly make the case that iMovie for iOS is on paper a very powerful video editor that can be used for serious work, in practice, its fundamentals are bugged and haven't been fixed for months. How many other apps in other domains are similarly very powerful applications on paper but buggy and unreliable in practice? Even though the iPad hardware or iOS isn't itself to blame for the shortcoming of these applications, how do apps like these negatively impact the reputation of the iPad as a work device?