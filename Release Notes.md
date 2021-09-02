Over the past few months, I’ve been zoning in on GIFwrapped for macOS; slowly getting it ready for release, and making it as good as it possibly can be. Because it shares a large portion of its codebase with the iOS version, however, there’s a whole pile of small improvements to the iOS app that I’ve made over the past few months.

Like seriously, this release of GIFwrapped almost feels like a whole new app. Almost.

- GIFwrapped’s in-app settings have been getting a bit crusty of late, as apart from the occasional addition or removal, they haven’t had any love… and it was quite honestly a big ol’ mess. I’ve attempted to rectify this by taking everything and shuffling it around into more appropriate spaces, rebuilding the whole mess from the ground up, and basically just treating it like it’s important. Funny how that makes things a lot better.

- A few of the list style screens got a small overhaul; like the GIF info panel and the list of files in the File Sharing folder. This effort seems to have made it all feel a little nicer, but that could just be my confirmation bias talking. Either way, it finally allowed me to rip out one of the oldest pieces of code in GIFwrapped: so long StaticTables, and thanks for all the fish.

- It’s only been 18 months or so since that game about relocating to an island and paying into an untrustworthy raccoon’s pyramid scheme came out, so what better time to introduce an icon inspired by the most obvious counterpart from the game? In true fashion, you’ll have to spend a few bells on getting Premium to enjoy this icon.

- The interactive swipe gesture for dismissing the preview screen could cause the screen to snap to the first GIF in its collection anytime one got cold feet and tried to cancel out; a particularly annoying bug for those Premium subscribers who have paging enabled. It’s fixed now, so let’s just chalk this up to more of those classic past-Jelly misadventures.

- The GIF renaming screen’s bottom bar didn’t connect to the bottom of the screen, which looked a little weird on iPhones with safe area insets. This was due to a straight-up amateur move involving an unruly layout constraint, and has now been taken care of.

- Despite my best efforts, issues causing GIFwrapped to freeze up can be incredibly tricky to track down; partly because GIFwrapped is so complex, and partly because I’m barely competent at the best of times. Nevertheless, I spent a bunch of time deciphering a handful of potential causes, tracking them down, and finally making good on clearing out what I could find and understand.

- Every now and then I discover that all the objects that make up the preview screen aren’t being released properly when you exit, which causes them to stockpile in the background. This can get costly pretty quickly, and it’s not generally something you want. Anyway, it happened again, so I figured it out and resolved it… for now.

- I went digging into the code for the cells within the main grid view and discovered a treasure trove of little bugs and behavioural oddities. After spending some time looking through it and tweaking things, I think I got it working just a little bit more nicely. MINOR IMPROVEMENTS FTW

Thanks again for using GIFwrapped. I’m hard at work making things better and getting a macOS release ready to go, but if you need to get in touch, toss an email to support@gifwrapped.co, or reach out to @gifwrapped on Twitter. I’ll do what I can to help.

Until next time, kids.