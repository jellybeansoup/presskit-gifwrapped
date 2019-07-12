Hello again! I know I've been quiet for a few weeks, but I'm back again with an update to fix some issues that many of you have graciously let me know about. Thanks for being patient while I worked on them, some of them required extra digging!

- Getting iCloud sync to work with the existing Library has been a challenge, and I've been finding that occasionally it'll throw up on itself and then roll around on all the good furniture. I took a pass at improving my handling of various edge-cases, which should hopefully reduce the issues and make the whole experience much more stable all around.

- In semi-related news, when turning iCloud on and/or off, the stored preference was being changed but the rest of the code wasn't getting the message (literally). The problem was that I had inadvertently caused the piece of code that notifies everyone of the change to be skipped entirely (you might think it's simple, being just a toggle switch, but it actually hides many layers of complexity… like an onion?). In any case, I've reworked that code so things are working as expected again.

- Save to GIFwrapped was having issues when trying to save items, often getting stuck and requiring the host app to be relaunched, other times not actually saving anything at all, and sometimes both! The culprit seems to have been a threading issue (because they all are at the moment, FML), but after one little tweak to the code, it's all patched up and ready to save again.

- The storage used for keeping Library-related values wasn't being accessed in a way that was entirely legit (which happens when you're working against the clock), and thus was causing more crashes than I would like. After re-thinking some of my formerly hasty decisions, I've managed to make things a lot less problematic, and thus more stable.

- Using the Retina option for Pixel Density was a little wiggy due to the image size not respecting the zoom scale when first loading up. A quick change to adjust the size has got that sorted out, and now you can look at your tiny, tiny GIFs at their beautiful tiny, tiny size.

- The API used to render user guide articles was deprecated a while ago, and I hadn't even noticed. I moved things over to the newer APIs, which is less of an improvement for all of you, and more of a quality of life thing for future-me.

- The grid view wasn't grabbing image metadata from the source of truth, and instead would end up using its own copy and thus doing some really weird stuff. I think I'd originally done this because doing lookups would be slow… so I changed it back, but also added some indexing to make sure it's still nice and quick.

- One user was experiencing crashes over and over again due to an item somehow being stored without a modification date. When GIFwrapped would try to read the item from disk again, it'd freak out… but I've calmed it down, given it some camomile tea, and it shouldn't have problems anymore.

I'm here to help if you find yourself running into problems while using GIFwrapped, so just toss an email at support@gifwrapped.co, or hit me up @gifwrapped on Twitter.

Have a great day!