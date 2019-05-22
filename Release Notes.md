If you've been paying attention, you'll know that I've been working on a huge update for a long time now. For the past few years (yep… YEARS), I've been working away at taking GIFwrapped towards a brand new version, and finally… IT'S HERE.

You have no idea how amazing it feels to say that!

- Say goodbye to tabs, and hello to a sweet universal search that makes finding the right GIF that much easier. Bookmarks and categories now apply across the board, and make it that much easier to find the GIF you want. It might not change your life or anything, but it's still a massive improvement.

- The preview screen also got some much needed love. It might not look like much right now, but it has a few goodies hidden away (and some that I'm still working on). Be sure to check out its much improved ability to rename images in your Library… and organise them into folders! 

- It's been a long time coming, but it's finally here: the Library can now sync with iCloud. If you've been using Dropbox, you'll need to switch over manually (you'll also need to move your files over manually, as GIFwrapped won't do it for you). If you've never used sync before, you should find it to be a huge improvement.

- In the post-iTunes age, it's more and more painful to try to access recovered files from iTunes (though still totally possible, just saying). As such, I've gone ahead and enabled access via the "On My Device" section of Files.app, which provides yet another avenue for accessing the "iTunes File Sharing" folder… and thus importing to your Library.

- If you've ever felt a bit naked with the clipboard contents hanging out in the Search tab for all to see, you can now clear it out with a quick swipe. If only things were always that easy to get rid of.

- The caching layer has gotten more and more complex over the last year or so, as I attempted to improve its overall speed. As part of doing so, I managed to introduce a pretty significant race condition that was causing a crash on launch. Spent some time rebuilding the problematic parts, so it should be pretty solid now… and just as quick.

- I spent a little time improving the code that parses Twitter URLs for their juicy GIF content, which has made the results produced by it so much more useful. Instead of just sharing the original post's details, things like the file name and sharing URL are actually representative of the tweet they're actually part of. Should it always have been this way? Probably yes.

- Using Save to GIFwrapped on tweets was fraught with issues: the list of GIFs returned wasn't as good as it could be, and then sometimes it'd save a GIF reply to the video you'd attempted to save (which isn't supported). Some adjustments to how URLs are handled means that you shouldn't end up inadvertently saving the wrong GIF any more.

- Sorting your Library by name occasionally differed from what you might expect, because it didn't use natural number sorting, so it'd end up with 1, 10, 11, 2, etc. A quick change to use the same sorting you'd get in Finder made short work of that. I like it when a bug fix takes one line of code.

- The icon selector for Premium subscribers was causing some issues, so I embarked on a whirlwind attempt at rebuilding it from scratch, simplifying a few elements as I went. Because that makes sense.

- In an effort to feel less gross when collecting data about crashes and general issues throughout GIFwrapped, I'm trying out a different crash reporting service called Sentry. Right now it's running side-by-side with Fabric/Crashlytics, but if everything goes well, I'll look at ditching that altogether, which would be amazing.

As always, if you have any problems, want to suggest an idea, or are just keen to let me know how much you enjoy GIFwrapped, you can reach out to me by emailing support@gifwrapped.co, or hit up @gifwrapped on Twitter. In the meantime, I hope you enjoy this new version of GIFwrapped, I think it's truly my best release yet.