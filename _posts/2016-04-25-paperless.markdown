---
layout: post
title: "Paperless"
---

# Paperless

I hate paper that comes in the mail. Paper sucks because inevitably there are like three pieces of paper out of the mountains of mail I get every year that are important, and it can't be searched easily. So every tax season I have to sit here and sift through piles of paper while waterfalls of tears are streaming out of my face. I'm in the process of figuring out how I want to scan and organize documents so they can be easily searchable on iOS.

"Scanning" is kind of a misnomer though. I've been quite impressed with the results of document scanning apps on phones recently, which apply processing to photos taken with your phone or tablet's camera. Most power users I know have converged on using Readdle's [Scanner Pro][sp], which has a really streamlined workflow for scanning multi page documents. It allows you to capture pages either with its in-app camera that can recognize common aspect ratios for documents and automatically capture pages when it detects one on-screen, or you can use its Radar functionality to automatically scan your phone's camera roll for things that look like documents and import them into the app.

Once there, your documents will sync from one device to the other over iCloud Drive. While iCloud has a reputation for being rocky and unreliable, iCloud is really more of a brand name for multiple underlying technologies, and CloudKit and iCloud Drive, which this document sync is built on top of, has been rock solid for me so far both as a user and a developer.

Where things start falling apart is document organization and search. While Scanner Pro does have support for multi-language optical character recognition, which tags your PDFs with their text contents for easy searching, Scanner Pro itself doesn't allow you to search for anything other than file name, which seems like a massive oversight and kind of defeats the purpose of the feature entirely. While the OCR tags are definitely useful if you move the documents over to a traditional computer, it's kind of a slap in the face to people who wish to embrace iOS as their primary computing platform. Having written some PDF parsing code myself in the past, I understand PDF is a pain in the ass to deal with, but they're already doing some pretty complex stuff with PDFs in the app, and Readdle also makes an app called PDF Expert, so it shouldn't be too far out of reach for these developers.

It would also be neat to see some more automation built into the app. Mac users may be familiar with the app [Hazel][hazel], which is a general purpose utility for automated action based on files being moved in and out of folders. A pretty typical part of a Mac user's paperless workflow would be to set up their scanner to output their documents to an inbox monitored by Hazel, and then automatically move or rename the documents based on the OCR contents of the document. This way you could automatically have your utility bills be renamed accordingly if Hazel sees Hydro-Quebec in the contents of the document, for example.

There is basic support for automation in Scanner Pro where you can compose various actions together into workflows that can be invoked with a few taps when viewing a document. This would allow you to create a button to rename your utility bills, but since the OCR data is already there in the app, it would be nice if filters similar to what you can do in Hazel were built right in. That way, even if full text search is unavailable in the app, at least the file names would automatically be set to something sensible based on its contents.

What I have yet to explore is if my needs would be better met by a combination of Scanner Pro and Readdle's other app [PDF Expert][pe]. Maybe PDF Expert is better suited at document organization than Scanner Pro, which really excels at pure document input. If that's the case, maybe they should make more of an effort to market the apps as a suite, as I surely can't be the only person who's thinking this.

Of course, due to the nature of the App Store and the lack of trial versions, finding that out becomes a $13 risk. But that's an other complaint for another day.

[sp]:  https://appsto.re/ca/lva5t.i
[pe]: https://appsto.re/ca/nGcwS.i
[hazel]: http://www.noodlesoft.com/hazel.php
