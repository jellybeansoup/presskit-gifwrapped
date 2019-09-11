Here come another set of bug fixes and… uh… performance improvements, ready to make life a little easier when wielding your favourite GIFs.

- For the last few releases, some users have been seeing a crash on launch that I just couldn't figure out. It turns out the cause was that some libraries contained images with duplicate identifiers (something that GIFwrapped uses to manage an image on-device). This isn't supposed to happen, but apparently it had, so I put some measures in place to allow the duplicates to be gracefully ignored, and no more crashes!

- A seemingly minor (but ham-fisted) change in a recent release meant that a number of users were seeing a problem where their Library would seem empty, but really it was just taking its sweet time to load things up. I reverted the change and made a different attempt at fixing the issue that I'd originally been trying to resolve, and the behaviour should once again be back to normal.

- I had also heard rumours about libraries appearing empty for an entirely different reason, and it turns out that on rare occasions, GIFwrapped would identify the type of a GIF to be some private Apple nonsense instead of the standard affair. Because GIFwrapped doesn't declare support for the former (I didn't know it existed), it "helpfully" filtered those items out of the Library, so I made a change to link the two types, and that should resolve this episode of the case of the missing GIFs!

- When an error was being displayed, the preview screen could act a little funky: if you opened the info panel, the message wouldn't get out of the way like it should. It looked weird, so I fixed it.

- When launching in split view on iPad—if using a version of iOS that we're not going to mention—there was a crash that would occur due to a method call that happens much earlier than it's supposed to. I added some checks for when things haven't finished loading up, and we can forget about this one for now.

- I had to pull out Sentry, an alternative crash-reporting system I'd been trialing in the last few releases (since the launch of 2.0), due to its cost being untenable. This doesn't mark the end of my attempts to move away from Crashlytics in the long term, but it's the best solution for the moment.

Thanks for using GIFwrapped, and taking the time to check the release notes! Please don't hesitate to throw an email towards support@gifwrapped.co with comments and problems, or hit up @gifwrapped on Twitter.