---
layout: post
title:  "Exposed to Modern Web Dev Pathogens"
---

# Exposed to Modern Web Dev Pathogens

This weekend, my coworker Shannon and I participated in our first hackathon, [Angular Attack 2016][aa]. Many developers spent the weekend developing apps using [Angular][angular], one of the many New Hotness view frameworks for Web development. As someone who now ostensibly gets paid to make Web sites, I should probably keep up with the hot new trends in the Web dev world, and this hackathon seemed like a great way to familiarize myself with a framework we had been considering using for work.

It's no secret that I'm a critic of modern Web development practices. It seems damn near impossible to accomplish anything fancy on the Web these days without needing to resort to a web of node.js packages that seems even too ridiculous as a caricature. The Hello World project that was inside our source repository when we entered the hackathon had [434 dependencies][deps] to install on my machine, and it wasn't even doing anything other than display Hello World yet. It seems like a house of cards teetering on the edge of collapse, and that's because [it is one][leftpad].

But modern Web development also has some really cool stuff these days. Listeners to the [podcast][limipo] probably know I'm a big fan of Facebook's [React][react] framework. It definitely isn't perfect, but it defies many assumptions people had about best practices on the Internet, tries something bold and new, and proves that perhaps it isn't so crazy after all. This kind of reimagining of Web development is sorely needed as bigger and bigger applications are developed atop of it on the client-side, and there's no real structure in place to keep development sane.

From my limited experience with Angular 2 over the weekend, it feels like a more "enterprise" take on React, with much more plumbing needing to be done explicitly by the developers. The scale of [our application][app] ([which you can vote for here][vote]) was incredibly limited, so it's hard to say for certain, but it seems like it could come in handy in massive-scale applications. The things I tend to develop outside of work are much more minimal, so I'd tend to gravitate towards something like [Riot][riot] myself, if I decide to bother with a fancy view layer at all.

One thing I ended up being pleasantly surprised with was TypeScript. Angular 2 development heavily favours use of [TypeScript][ts], Microsoft's statically typed-checked superset of JavaScript, so we decided to check it out. TypeScript integrates really well with Microsoft's own [Visual Studio Code][code] text editor, and with very little effort, you can get really helpful tooling and feedback from the TypeScript compiler. Microsoft's code autocompletion is practically unbeatable in the IDE space, and having the opportunity to use it in JavaScript while making minimal changes to the JavaScript you're used to writing is really nice. If we switched to using TypeScript at work, I think we would see immediate gains in productivity *and* less bugs, whereas I'm not convinced I could say that about Angular 2 as a whole.

Visual Studio Code has really nice tooling when combined with TypeScript, but I can't help but feel that it and other Atom-based text editors still feel too much like typing in a Web browser (because fundamentally that's what it is) and not enough like a native Mac app. Yes, it's nitpicky, but you know me.

If there's one thing I'd like to see improved, it's documentation. A lot of what exists on the internet today about Angular or about TypeScript assumes you are fully up to date on Modern Web Dev Practices, such as using npm, the [clusterfuck][common] of [different][system] JavaScript [module importing mechanisms][amd], ECMAScript 6, and the like. If you are coming straight outta ECMAScript 3 land like we did, there doesn't seem to be a central place where you can catch up on what's going on with all of this mess before jumping into modern Web frameworks and you have to piece it all together yourself.

But overall, it was a decent learning experience, and I think we know enough about it now to make an informed decision on whether or not it's the right tool for the job in future projects. That's all we really wanted out of it, so I'd call it a success.
 [leftpad]: http://blog.npmjs.org/post/141577284765/kik-left-pad-and-npm
[riot]: http://riotjs.com
[common]: http://www.commonjs.org
[system]: https://github.com/systemjs/systemjs
[amd]: http://requirejs.org/docs/whyamd.html
[limipo]: http://limitlesspossibility.net
[aa]: https://www.angularattack.com
[angular]: https://angular.io
[deps]: https://gist.github.com/Sakurina/a7fc2e1f3879c2114142c7fed3de9cfc
[react]: https://facebook.github.io/react/
[ts]: http://www.typescriptlang.org
[code]: https://code.visualstudio.com
[app]: https://polyphoniccataclysm.2016.angularattack.io
[vote]: https://www.angularattack.com/entries/3445-polyphonic-cataclysm
   
