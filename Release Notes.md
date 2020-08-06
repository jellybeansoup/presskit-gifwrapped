Over the past few weeks, I’ve been laying out plans for GIFwrapped’s future, so a lot of this release is in anticipation of that: rebuilding parts of the code to improve them, and to allow me to bring exciting new features to GIFwrapped down the road. Lest you get the idea that I’m a big ol’ tease, however, this release also adds something exciting and new.

- Thanks to some recent refactoring of the way the main app’s universal search layer works, I was able to bundle it up and bring the feature over to the Messages app, allowing for parity between the way search works in both the main app and the Messages app. This means you can now search anywhere for a GIF to send, right from a conversation in Messages, just like you would within GIFwrapped itself. Hooray!

- The code managing GIFwrapped's rather complicated share functionality—including the menus and actions that accompany it—has existed in the same form since almost the beginning (except for when I wholesale ported it to Swift), and it was getting a bit… crusty. I buckled down, tore it to pieces, and built a new version out of the rubble… which should hopefully work about the same as before. It’s really more of a self-care thing from my perspective, but at least it should be less prone to problems as I expand its feature set going forward.

- Dragging GIFs from the main app’s grid view has been a thing for a while now, but I never did get around to implementing the functionality for the preview screen… until now. Just another thing to cross off my bucket list.

- Thanks to a handy watch dog (woof!) that I’ve been using with my beta testers (its bark is honestly worse than its bite), I was able to surface a potential cause for the lock ups people have been experiencing: resolving bookmarks used to track iCloud files from the main thread. The moral of the story here is: don’t do that.

- Tweets could occasionally be dropped from search results, particularly if they were a reply to another tweet. Fortunately, I was able to improve the quality of the results returned by tweaking how I parse replies, but I swear I will never be done fixing bugs that have cropped up thanks to Twitter's site overhaul from several weeks ago. SIGH.

- I was occasionally seeing images getting stuck in an update loop, constantly attempting to merge non-existent changes back to the metadata store. Turns out the fix was two-fold: first I fixed a bug that was causing the metadata to appear to have changed even when it hadn't (oops), and the second was a little refactor to avoid modifying the store unless it's _actually_ necessary.

- The preview screen wasn't handling errors particularly well, with one (rather useless) error that was used across the board. This is a regression that happened a while back, caused by past-Jelly ditching the old method of downloading and displaying images… and thus the lovely, custom errors that came with it. It's still not perfect (is anything?), but it's a damn sight better than what past-Jelly left us with. JERK.

- The way I was retrieving Animated Images from Photos seems to have been broken for a while now, stopping new images from showing up in the results, but it was a fairly easy thing to resolve. I just wish I’d known sooner.

- It only took me… uh… 3 years to support the fancy authentication stuff that Apple introduced back in iOS 11, but here we are. I've added it to the flow for connecting to Dropbox. That's about all I have to say about it.

Thanks for using GIFwrapped, and doubly so for reading these release notes! If you’re having any trouble, please reach out by emailing support@gifwrapped.co, or tweet @gifwrapped, and I’ll do what I can to help. If you’re feeling particularly generous, a review on the App Store is always welcome, too (but fair warning: I don’t provide support through reviews).

Until next time, remember: you are a large, majestic mountain trout.