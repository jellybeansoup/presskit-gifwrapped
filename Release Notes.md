The time has finally come to deal with iOS 14, so I've done the work to make sure that GIFwrapped properly supports it. Don't get too excited: for now, it's literally a matter of "was it showing an error? GUESS I HAVE TO SUPPORT THAT", so if you were hoping with all your heart for some kind of widget or something: prepare to be very disappointed.

While we’re on the topic of disappointment, let me unload a little more bad news on y’all: support for iOS 11 and 12 is going away in the very near future. In fact, I fully expect this to be the last release to support them, unless something major breaks.

Now… as far as this release is concerned:

- I added support for iOS 14’s limited Photos permission, so if you choose it, it should correctly show results based on what you specifically select, because that’s how the limited permission works.

- The method for pulling frames from video while converting to GIF stopped working as of iOS 14; not because it's deprecated or anything, just because that sort of nonsense happens (what is life without DRAMA). Good news is that I've had a secondary option waiting in the wings, which might even be slightly faster (but is less… battle-tested), and I've activated it so that things can keep on trucking.

- I was still seeing some crashes when image metadata was being updated, so I reworked some things to reduce the possibility for errors to occur, which should make the whole thing more stable… again. I call this method the stab-about-in-the-dark-until-you-hit-something form of debugging.

- I’ve noticed for a while—particularly after an iOS update—that downloads from iCloud could sometimes just get stuck, and no amount of resetting or force quitting would sort things out. So I did what any sane person would, and created a custom console app to run on my iPad so that I could get some insight into what was happening, and finally managed to sort it out.

- The paging feature available to Premium subscribers had a small flaw: as you paged through, GIFs wouldn't always stop animating as they went off screen, which means higher-than-expected CPU and memory use. I adjusted the way pages are loaded, only ever allowing GIFs to play when they're actually on screen, because otherwise, what's even the point?

- There I was doing some spring refactoring (as you do), when I discovered that the save/sort button wasn't being updated as one might expect, meaning that the button for saving a search (a Premium feature) likely wouldn't show up when a search went through, and if it did somehow appear, it likely wouldn't leave. I hooked it up correctly, and now it should do the thing you'd actually expect it to do.

- The fact that GIFs have a configurable number of loops (i.e. that it's not always infinite) is easy to miss, and as such, it's a bit of information that has been missing from the info screen for far too long. Since I need to pull that information out anyway (for the new and hopefully improved GIF playback), I figured it was high time I actually made it visible. No need to thank me or anything.

- I've not run into a lot of cases where images could be discovered but not downloaded… however, in cases where the server was producing HTTP errors for an image download, the response would often be entirely misinterpreted. So I wrote an error message for every HTTP status code that exists. Easy peasy lemon squeezy.

- When updating my remote configuration setup a release or two back, I managed to accidentally hardcode the wrong file as the source, which isn't exactly ideal. Wired in the right variable, and now it's like I actually know what I'm doing. WHODATHUNKIT

As always, you can send an email to support@gifwrapped.co or a tweet to @gifwrapped if you’re runing into problems, or if you’d just like to share your thoughts. My ears and heart and DMs are open to hear from you.

Until next time, remember: this too shall pass.