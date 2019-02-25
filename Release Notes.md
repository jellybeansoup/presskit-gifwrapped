I know it's been a while… at least a couple of the bugs this release hopes to address have been causing people grief for a few weeks while I did my best to get to them, so maybe now is a good time to mention that the GIFwrapped Premium subscription is what helps me be able to dedicate time to fixing bugs and building features.

Without my subscribers, I am but a code monkey out of time. This release can happen thanks to YOU.

- An oversight in the sync code was causing images to be deleted when the Library's contents was plastered over the top, causing a handful of people to lose their hard-earned collections (I'm really sorry for this, please get in touch if you haven't already). Some changes to the sync logic should ensure that this doesn't happen again, but if it does, I've put other measures in place to allow the lost items to be recovered via iTunes File Sharing.

- Under certain conditions, renaming files could cause duplicates to appear in the library unwittingly. As it turns out, it's because after the change was pushed to the server, the local copy wasn't updated, and things would go downhill from there so very quickly. A quick tweak to ensure the change was properly saved, and things should be much better now.

- When renaming an image, Dropbox would unnecessarily clear it from the cache and download it all over again… not an ideal scenario. I fixed a couple of places where the current revision wasn't being updated, which had it sorted it out pretty quickly. Maybe… too quickly?

- There was a crash in the Search tab that was slowly getting worse with each new release, and it had me entirely stumped. When it finally happened to me while I was working on a separate bug, I was able to properly investigate. This allowed me to find a potential cause, and hopefully sort it out once and for all.

- There was a minor issue blocking file recovery from happening when it was manually triggered. I resolved the issue, and made it so that opening the iTunes File Sharing option in the import menu causes recovery to be run automatically, which is actually kinda handy.

If you're having issues, want to share an idea, or just want to gush about how GIFwrapped sparks joy for you, don't hesitate to reach out! You can catch me by emailing support@gifwrapped.co, or over on Twitter: @gifwrapped. I'm here to help where I can!