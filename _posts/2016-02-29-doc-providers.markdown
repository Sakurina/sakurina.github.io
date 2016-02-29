---
layout: post
title:  "Document Providers"
---


# Document Providers

Document providers are a feature that was introduced alongside iCloud Drive in iOS 8, which allows vendors of cloud storage services to integrate their services into the system file picker. It's one of the rare places in iOS where a service was introduced alongside a feature that gives third-parties feature parity with the aforementioned service. But I feel like they're underused.

For example, one of the main appeals of something like iCloud Photo Library is that now your entire history of photos in the cloud is accessible from any third-party application using the system photo picker. Alternative services aren't as appealing because then it adds an additional step to using those photos in other apps: you need to switch over to your cloud photo service app first and export it to your phone's photo library which behaves as a separate entity.

There is a kind of workaround to this issue, and that would be for something like Google Photos to implement a document provider with a custom UI that displays your cloud photo library in a pleasing and useful way. There's one catch though: the document provider API is different from the photo library API, and any apps wanting to support this workaround would need to add a "import photos/video from document provider" button that only accepts image files and movies.

You could also see the same thing with music. You can't make a music player right now for iOS that has its songs available for use in third-party apps unless it's just a front-end to the music library built into the phone, which requires you to either sync with iTunes, purchase songs from the iTunes Store, or sync via iTunes Match. This means you can't use songs from third-party music players in videos you make in iMovie, or as samples in GarageBand, or DJ with them in Traktor or djay. If third-party music players made their music available as document providers, then they would be available in some manner to third-party apps, and it would be easier to move away from the rapidly rotting iTunes syncing process.

As Apple's first-party offerings become worse and worse, it is tempting to wish for the possibility to replace all of them with better third-party offerings, but doing so with document providers, while possible today, probably isn't the best of ideas. Document providers are a great power user feature, but Apple has shied away from exposing a traditional file system to users in iOS because most computer users just suck at understanding it. Suddenly making it more commonplace for users to deal with traditional files and hierarchical file systems and file types would be a huge blow to the simplicity that makes iOS great and accessible.

It's 2016. It seems kind of barbaric that if I want to buy a song from Bandcamp and sync it to my phone so I can use it in a DJ app, I need to go download the album on my computer and then fight with iTunes to get it to sync. Please Apple, give me a way to add arbitrary media files to my system-level music and video libraries on iOS. Either that or Make iTunes Great Again™. I beg you.
