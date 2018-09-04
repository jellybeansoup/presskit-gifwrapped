I know it's been a little while since the last update, and while things are pretty stable (as far as I'm aware, anyway), I wanted to drop a sweet bug-fix update on y'all. Because why not, really. It has a couple of bonus bits that I figure you might appreciate as well. Enjoy!

- If you've ever wanted to grab your entire library and send it off somewhere, you're in luck. I've added an option in the Storage settings to export all cached images from the Library as a zip file, which pops up a little share sheet to do whatever you want. Couldn't be simpler.

- In an effort to improve its overall consistency, I've moved stuff to do with migration and cleaning up so it happens prior to loading up the UI. All going well, you won't see much of it right now, but I'm gonna be making use of this when the next major version drops, so… stay tuned?

- I tweaked the the Search tab's clipboard button so spaces are trimmed and multi-line items are ignored. You can still paste the old way if you care a whole lot, but this should make the button a whole lot more useful overall.

- There was a race condition in play where multiple updates to the grid view happening at once could cause a crash, because the underlying information would end up out of sync with the UI for a brief moment. I made some minor changes to how this mechanism works, so there shouldn't be any more of that going on.

- If you tried opening the alternate icon selector on iPad when GIFwrapped was in a tiny column, it'd get a bit confused and end up missing a couple of icons (or worse, laying them out all broken-like). After digging into how the layout is computed and updating it in a few places, it should be all good going forward.

- People flipping the "Keep images on device" switch on may have been vaguely confused by the fact that it would download a batch of images, but then just kinda give up. This was due to a really stupid logic bug which stopped things from being notified when a prior download had finished, which I sorted out the instant I stopped face-palming.

- Screens on iOS 10 and lower were missing the insets needed to align content with the bottom of the navigation bar, which made it impossible to properly access things that got stuck underneath. Thanks to a user's email and some code to properly calculate the insets, things are finally working properly again.

- As it turns out, migration just straight up wasn't happening from a couple of different old versions, so I went in and fixed things so it'd work properly. Not because anyone is even going to be upgrading from those versions at this point, but just because I like to have my bases covered.

- Editing a GIF from the Library remotely wasn't causing the cached copy to be discarded and re-downloaded, which meant it'd end up out of date. There was actually a couple of things that were causing this behaviour, so I sorted 'em both out, and now everything should work as expected.

- At some point, I managed to disable the preview screen's rotation functionality… and had no idea because apparently I don't use the feature that much. Either way, it's all sorted now. Rotate away!

- An oversight in the code for detecting downloads in the Save to GIFwrapped extension could result in being able to download images multiple times, which isn't super ideal. A couple of tweaks here and there, and it should be pretty solid now. If only things were always that easy, amirite?

- At some point, the way the Photos tab updates its content got messed up, causing crazy looping refresh cycles, duplication within the UI, and making a right mess of things. It happens sometimes… but not any more! As a certain demi-god would say… YOU'RE WELCOME.

If you're having trouble, or would like to make a suggestion, you can reach out to me via support@gifwrapped.co, or hit up @gifwrapped on Twitter. I'm here to help… or possibly asleep… but mostly the help thing, I swear!