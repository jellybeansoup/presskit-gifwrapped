Nothing like starting off a new year with a new update. There's more coming incredibly soon, but this prepares the way for things by resolving some bugs, and making some under-the-hood changes that are needed for upcoming features.

- I went through and made a significant number of changes to the structure of the Library sync engine to prepare for… clients other than Dropbox. This probably isn't 100% yet, but then… when is anything? Throwing incomplete stuff out there is what I'm best at!

- I've expanded the usage of the dialog prompting you to manually reconnect to Dropbox so that it handles more cases, including some where reconnection used to happen automatically. You can blame the wiggly ghosts for this minor inconvenience (their specialty).

- If downloaded configuration files were newer than the ones bundled into the release, they'd be skipped, causing features to potentially break. Not ideal, but a quick modification date comparison sure sorted that out. TAKE THAT SUCKA

- The new pre-show stuff that runs on launch was causing issues with URL schemes, because the app needed a moment to be ready to handle the URL, and iOS is super impatient. A quick addition to the code, and URLs will now be handled regardless of how long it takes to GIFwrapped to get ready. Progress!

- I wanted to remove the old upgrades from sale, but turning 'em off caused people restoring their purchases to experience crashes. Not ideal, so I dove into the code around in-app purchases and made it possible for me to properly remove 'em from sale at some super-distant point in the future. 

- The mysterious custom URL option was a little too eager, allowing invalid configuration to lead to confusion, so I took a look at things, and tweaked 'em so that there'd be even more confusion. I mean, it IS in the advanced section of the settings, what the heck are people expecting here?

- As it turns out, when using a team account for Dropbox sync, the team name was getting duplicated… but I had no idea. Who knows how long this has been a thing. Maybe since the very beginning?!?!!? GOOD WORK JELLY

- An issue with the library's contents taking just slightly too long to be loaded was causing the preferred sort order to be ignored, which isn't ideal. A couple of tweaks here and there mean the app's load time might be a tiny bit longer for larger libraries, but the tradeoff is very worth it.

- Somehow, past-Jelly didn't stop to think that, if the thumbnail has failed for a particular GIF… maybe it's a good idea to try loading it again after downloading the GIF itself? Anyway, it does that now, so you can look forward to less cells displaying errors in the grid view. Hooray!

- When getting to the end of a paged set of search results, the indicator wasn't being properly removed. This was due to the conditions only taking the final page into account when comparing the number of results against the total available, but now it's taking into account the offset, so we're all good here; just bread for the table THANKS.

- Downloads started by one sync client weren't being properly cleared out, so when connecting another, you could find yourself in a limbo where there's a bunch of downloads waiting to finish that can't. One little chat with the dead later, and we should all be able to move on to a better place.

As always, comments, complaints and support requests can be sent via email to support@gifwrapped.co, or you can drop a line to @gifwrapped on Twitter. I'm here to help!

Have a great 2019!