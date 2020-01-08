It's a new year, a new decade, and a new GIFwrapped version! It comes complete with a new versioning system that puts less pressure on me to produce big feature releases, and should go along nicely with the subscription-based pricing that GIFwrapped has been using for a while now.

There's no better way to kick all of this off than to improve things with a number of hefty bug fixes, so without further ado, here's the list of changes in the first build for 2020!

- The copyright notice on the launch screen got a tweak. Happy new decade, everyone!

- I heard you like dark mode, so I put dark mode in your dark app, which makes those previously white alerts and share menus lovely and dark (like my soul).

- Given the switch-over to context menus in iOS 13, it seemed only fitting that GIFwrapped replace it's custom long press menu with a fancy context menu, now available both from the grid view and the preview screen. They do have some weirdness with animating the image preview, but that's a problem for future-Jelly to figure out.

- There seemed to be a number of iCloud connection issues somehow related to phone changes/upgrades, and upon further investigation I discovered that the warning wasn't being triggered to allow for automatic re-connection, so I adjusted the logic so it's displayed properly, and hopefully I won't need to stand in for it it on Twitter any more.

- Some wiggly ghosts were occasionally accusing other wiggly ghosts of disconnecting Dropbox, when it was just that iCloud had been enabled instead. Lotsa finger pointing, mostly about nothing. I added some logic to make sure things get cleaned up properly, and you shouldn't see this warning any more… unless it's actually legit.

- Somehow I hadn't activated a "read-only" mode for iCloud sync that kicks in under very specific circumstances (extensions in particular, where memory is very limited). This would cause issues with the sync potentially happening while trying to perform other tasks, so I fixed it up, and it shouldn't happen again.

- Under certain circumstances, an item in the grid view would start it's loading animation but never stop it, causing it to spin forever. This was due to the expectation that the cached file would change, which didn't always happen, so I added some backup logic, and it shouldn't get stuck in a loop stuck in a loop stuck in a loop stuck in a loop stuck in a loop any more.

- GIF conversion was occasionally bumping into memory limits when using Save to GIFwrapped, which could cause the whole thing to crash without finishing its job. I dug into the logic for how the various frames are handled after capturing them from the video, and it seems to have done the trick, reducing the load and allowing a little more headroom for super frame-heavy GIFs.

- Apparently Twitter started including text when sharing tweets from its app, which would sneak through and then fail to be handled as a URL, causing an error that wasn't necessarily valid. I added a little extra code to handle these strings separately, so the error shouldn't be popping up any more.

- In certain cases, when an image was opened, it triggered a change that caused it to be hidden from view until the next time the app is launched. Obviously errors aren't great, but neither is this behaviour, so I fixed the issue causing it, and now images with errors won't go missing. Yay?

Thanks for continuing to use GIFwrapped! If you like using it consider leaving a review on iTunes, and subscribing to GIFwrapped Premium wouldn't go astray either. You can also reach out to me on Twitter @gifwrapped, or via email at support@gifwrapped.co… I'm always working hard to improve the app, and I'd love to hear your thoughts.

Until next time!
