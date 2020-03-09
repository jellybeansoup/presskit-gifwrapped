Continued tracking down and tackling bugs over the last few weeks, and finally figured out the solution to some stuff that was stopping me from shipping a great new feature… so if you thought I'd gone quiet, you couldn't be more wrong!

- Finally got around to putting the finishing touches on a new premium feature that has long been requested: the ability to page through images on the preview screen. Needs an active GIFwrapped Premium subscription to use, but it's pretty great for throwing caution (and data limits) to the wind, and flipping through a bunch of search results.

- Migrated my analytics stuff from Fabric to Firebase, as the former is going away soon, and I'd been putting off doing the transfer. The privacy policy got an update to match the changes, but in reality nothing has _really_ changed: Google owns both and/or our very souls.

- The logs captured while running GIFwrapped really only get captured when the app crashes, which makes them vaguely useless for like 90% of issues that people run into. For ages, I put off switching to using a third-party logging framework (CocoaLumberjack, for those who care), and then it ended up taking like an hour to implement, so it seems that all that fear was for nothing.

- Something changed with Dropbox downloads recently, and it caused PNGs and JPEGs to go all screwy. The issue appears to have been a mix-up in how the download's file type is determined, so I made some tweaks to resolve things, and it should work properly again. Phew!

- In order to reduce the duplication of cached images for iCloud, it has its own special caching layer that utilises iCloud’s storage directly. This is awesome, but had the side-effect that the Storage screen wouldn't report the amount of space used by on-disk files, which is less awesome. I adjusted the behaviour for how this works, so now the numbers should be accurate across the board.

- The ordering of results from Photos didn't really make much sense, which I've somehow been noticing more and more. Turns out it was due to some oversights in the order I specified when fetching photos, so after a quick tweak to sort by the date an image was "created" (and not just "modified"), things are looking much more logical.

- If I'm honest, the text field used for renaming GIFs needed a clearer way to finish editing than just hitting the return key, so I added a "Done" button that lets you cancel without having to resort to tossing the device out a window and buying a new one.

- The logic around detecting (and avoiding) duplicate file names while renaming was just straight up broken, which could allow for duplicates to be introduced into one's library. One does not want this, so one fixed it.

- When using iCloud, the info screen often wouldn't display the full spread of details about a GIF. Obviously, this isn't cool—especially since many are considered a premium feature—so I introduced fallback sources for 'em, ensuring that fields have multiple chances of loading up their particular piece of information.

- Apparently when switching over to context menus, past-Jelly didn't bother to make the subsequent share sheets show up from the right location, which is fine on iPhone, but it looks a little weird on iPad. I jumped in and did past-Jelly's job for him (again), so they should be presenting from the right location now.

Thanks to everyone who has been letting me know about bugs and problems, sometimes I fail as far as replying to the email/tweet/what-have-you, but I'm always listening. If you'd like to reach out (I'll help where I can), you can tweet @gifwrapped or email support@gifwrapped.co, and you'll have my ear.

Until next time, remember to wash your hands regularly!