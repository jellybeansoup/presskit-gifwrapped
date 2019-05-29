…and we're back! Overall, I'm putting last week's launch of GIFwrapped 2 down as a great success. There was an overall positive reaction, and I'm really thankful that you all like it.

Of course, that doesn't mean there hasn't been troubles, and with the help of a number of amazing users, I've spent the last week working hard to get things into an acceptable state so y'all can stop dealing with crashes and get back to the GIFs.

So without further ado:

- Mass-uploading GIFs to iCloud—something that was happening a lot, given that it's a new feature—was resource intensive in the most ridiculous way, because I made the mistake of not corralling it, result in GIFwrapped trying to upload everything… all at once. After putting some limits in place, it's now slower, but at least it's not going to go hard and die trying.

- If iCloud didn't manage to get all the way through uploading the Library contents (you know, because of crashes?), it'd end up starting over again, and thus any items that had managed to get uploaded would get duplicated… sometimes a lot. Dealing with the original file properly, and updating GIFwrapped's internal metadata, should ensure that this doesn't happen any more, which is honestly a relief for everyone involved.

- The iCloud on-boarding screen wasn't checking whether it was already connected if you went back and tried to continue through that screen again. That's obviously not ideal, so I added the check, and now you can zoom around the on-boarding screens with no regrets.

- It turns out that MoPub's privacy policy screen is disabled when Limit Ad Tracking is turned on (totally worth doing FWIW). I wasn't aware of this, which resulted in _my_ screen still being shown during on-boarding, and thus blocking people from getting into the app. One quick check later, and y'all should be able to get right on in now.

- After saving a GIF to the Library, the UI could find itself frozen in place, unwilling to move in fear of the monster returning. Also partly because there was a threading issue causing a deadlock, so I had a go at making a few more things asynchronous, and hopefully it should be running much smoother now.

- The Info screen's name field wasn't being updated appropriately after renaming an image, which is just straight up unsettling (and a little awkward). Turns out I hadn't updated the relevant code when introducing the new screen for renaming and moving, so I did that and BAM! Solved.

- Importing from the Inbox was being run unnecessarily. This is an old method for importing to the Library with the share extension, and it's not really used anymore, so it's somewhat pointless to run it every time. I sat Turbo on it, and now it can't get up. Cat gravity!

- When using iCloud, the Sharing Links option in Advanced settings would incorrectly reference Dropbox. This was just an oversight, but I was able to fix it up thanks to some eagle-eyed users with a thirst for adventure!

- If the drawer was open all the way, and the bookmarks view wasn't all the way at the top, trying to drag on the little handle to close the drawer just wouldn't work. A very minor tweak to the drawer's expectations of when it should stick to the top, and it's now working as expected!

- With a long enough list of folders, the name field of the "Move to Folder" screen could get in the way of the last couple items, which can be a giant pain. The list just needed a gentle nudge so it could scroll clear of the field, and now all your ZZ Top GIFs can be moved to their appropriate home.

Thanks to all of you for using GIFwrapped! As always, I'm here if you're running into problems, so just toss an email at support@gifwrapped.co, or hit me up @gifwrapped on Twitter. I'm here to help!