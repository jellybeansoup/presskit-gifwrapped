Good morning! Who's ready for a GIFwrapped update?

- Work on the Library refactor continues, and this release takes care of a few additional things under the hood. Nothing interesting, really, unless you’re curious about the new features I hope to wring out of it… and then it’s actually verrrrrry interesting.

- The code that calculates the size of the thumbnail grid has been a mess for a while, with each new platform adding complexity as I tried to tailor the grid to the screen, like an idiot. With the iPhone Duo effectively being an iPad that folds in half with an iPhone duct-taped to the back, things got even more complicated, so the best thing to do was simplify the heck out of it. If you’re on an iPhone you probably won’t notice, but the grid on iPad and Mac is definitely different now.

- The iPhone Duo’s sneaky horizontal safe area played havoc with my custom sheet, despite all the work I put into it this year to get it working nicely with Liquid Glass. I had to rework its behaviour ever so slightly, and now (in the words of North of the Border) it’s not just good, it’s good enough.

- In the last release, I fixed a crash caused by items coming through iCloud sync without a URL. Unfortunately, on new devices, that fix could decide some of your GIFs were missing before iCloud had finished listing them, and remove them. Now the Library only removes a GIF from iCloud when you delete it yourself, and if it can’t account for every file, it just… looks the other way. Sync is hard.

- There were a few bugs in how URL schemes where being handled within GIFwrapped. Likely nothing anyone actually noticed (some obscure settings stuff, and a percentage encoding thing), but I took the opportunity to fix them as an excuse to pull that code out into something I can reuse elsewhere, so it’s a win for all of us. Mostly future-Jelly, who won’t appreciate it anyway. Ungrateful jerk.

That's it. Technically a smaller release than I'd originally planned for this one, but who's counting? If you are, or if you need some help with GIFwrapped, please toss an email to support@gifwrapped.co and I'll see what I can do to help.

Until next time, remember: you're a star.