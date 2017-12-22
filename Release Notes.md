You may have thought I'd forgotten about you all, but never fear! I've been diligently working hard on under-the-hood improvements and fixes, bringing you easily the least worst version of GIFwrapped of all time!

I mean, I could be wrong, but I sincerely hope not!

- At some point, a combination of factors resulted in ridiculous levels of CPU and memory usage during the creation of thumbnails. After a month of confronting my past mistakes head on (and more than a little procrastination), things are looking much better.

- An innocuous change (aren't they all?) caused a small delay in retrieving metadata for images, both in the Library and in Search. A couple of quick adjustments restored the prior speed, which should help make a little bit of difference. Especially in larger libraries, where it mattered the most.

- The alert designed to warn of a failure to connect to Dropbox was way too eager, maybe even a little lonely and desperate? Adding a delay to the check should allow things to properly fail before everything starts freaking out… no one likes an alert that cries wolf, after all.

- The cache for Search and Photos images was storing files but then completely forgetting about them, which I can honestly relate to some of the time. Tweaking the names it used allowed everything to work as intended, mostly because it wouldn't put the files somewhere it wouldn't recognise later.

- The list of files in the iTunes File Sharing folder had a few niggly issues, mostly with the thumbnails and just how dang slow it was at filtering large lists. A few tweaks here and there has it running much, much better… maybe even too much better.

- While adjusting some stuff under the hood, I took the opportunity to add the modification date for images to the Info screen for people with the File Information upgrade. Nothing crazy, just a tiny little hint at some cool stuff that's coming.

- The initial presentation of the library when launching the app wasn't always consistent, which isn't really something that matters to anyone but me… but guess who's in charge of making this thing? Point is, I fixed it up, and one more of my little annoyances is dealt with.

- As it turns out, there were occasions when "rescue operations" run by GIFwrapped would block the UI, and everyone knows that's bad. A tweak here and a nudge there, and it should stay responsive for now.

- It doesn't happen often, but those same rescue operations weren't always reflected in the Library itself, which sometimes meant they might have missing thumbnails. Now they'll be refreshed automatically, and it'll be like nothing happened at all. Because it didn't? Or did it? I'm confused.

If you want to get in touch with me, I'm only an email or five away. Send one to support@gifwrapped.co, or even just hit me up on Twitter @gifwrapped, and I'll be happy to help you with any problems!