A developer’s job is never done, and I’ve been working hard to tackle as many of the issues I come across as I can, so I hope this release helps ease any problems you might be running into!

- I gave the App Icon screen in GIFwrapped’s settings a little overhaul, and made some of the less exciting icons free for everyone to use. What can I say? I’m a giver.

- I discovered that one of my recent bug fixes introduced a small issue that caused some values to be ignored when comparing entries before updating the library's metadata store. This is mostly fine, as any of these values would, in practice, be accompanied by others that would've been caught, but a bug is a bug is a bug, so I fixed it.

- While reworking the sharing menu in the last release, I messed up some logic causing the menu's actions to be loaded up _after_ checking to see which ones had been loaded. This had the side-effect of making the share button in the preview screen fail to show the shortcut list first—which isn't how I intended it—so I fixed that.

- I also did some additional refactoring of the way that share sheets (the standard iOS ones) are presented in order to enable a future feature which hasn't been switched on yet (because it isn't ready). When sharing via the standard means, you shouldn't really notice much of anything, but trust me… it’s different.

- The preview image couldn't initiate a drag on the iPhone. It's absolute nonsense, I know (where are you going to drag it to?!), but that future feature might make use of it somehow, so I enabled it anyway.

- I noticed that there was a fun, new crash related to the new way image metadata is updated, caused by the old copy not being removed from the store correctly before inserting the new copy. I added a fallback solution for this case (which is slower, but won't fail), and now it shouldn't be causing any more trouble.

- The remote configuration setup I use to manage the minutia of certain features (like how GIFs are shared to different apps) wasn't reloading correctly when I updated the server-side file. It's not really a big deal, as the file gets bundled when shipping updates, but it's always nice when things, you know... actually work.

- I was seeing an occasional crash caused by the presentation of a new-ish error alert in the Messages app. Basically it was because it being presented from a background thread, and dammit past-Jelly, you know you're not supposed to pull that nonsense.

- I continue to get a lot of reports of Twitter-related issues—particularly ones where the content is considered sensitive, but the user doesn't realise it—so in an effort to reduce the number of false negatives (I'm only one guy, and not at all responsible for Twitter's life choices), I've added the ability to preview the Tweet in a browser right from the error message.

- Dug into the Twitter parsing once again (groan), only to discover that a super weird bug in the library I use to pull apart HTML was bugging out on me. I'm not sure _why_, and I'm terrified to pull apart Twitter's HTML by hand to figure it out (please no), but I did manage to figure out a working solution, so now we're just gonna back up slowly. Real slowly.

- I also discovered a bug that was causing some tweets to be wrongfully ignored due to a casing issue: basically, it was comparing @GIFwrapped vs. @gifwrapped and deciding that they weren't the same. That's clearly not the case, so I tweaked things to do a better job, and the results should be much improved.

Thanks for using GIFwrapped: you’re a champion, probably! If you’re running into any problems with the app, please reach out by emailing support@gifwrapped.co, or tweet @gifwrapped. 

Until next time!
