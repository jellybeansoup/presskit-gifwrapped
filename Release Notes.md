Guess who's back, back again? It's GIFwrapped, with some more bug fixes (tell a friend).

- A change to how windows are handled in iOS13 seemed to make it so that they aren't automatically held onto when presenting alerts in them, which made the image deletion prompt relieve itself of duty prematurely. I made a quick tweak to ensure that the window is kept around, and things are once again working much more like one would expect.

- When renaming GIFs, the sync engine could get stuck in a loop of attempting to update the server; it would actually work the first time, but the local metadata wasn't being updated with the change afterwards, so it'd just keep trying over and over. I added an extra line to force the metadata update for that particular piece of information, and now it's working as expected again.

- The status bar was going dark when opening the in-app settings screen, which is one of those very minor visual bugs that I just can't abide. After taking a look, I realised that I no longer need the hands-on approach to status bar management I'd previously had, so I got to delete some code to fix the issue. DANG THAT FEELS GOOD

- Speaking of incredibly minor visual things, the user guide's search bar was bothering me, in that it was showing as a _very_ faded looking version of the colour it was intended to be. I tweaked the appearance to try and make it a little better, and now I'm… well, not happy, but definitely a little less irked.

Remember: always wash behind your ears… and that if you want to let me know about any issue you're having, you can always tweet @gifwrapped or email support@gifwrapped.co with the issue. It helps make things better for everyone!