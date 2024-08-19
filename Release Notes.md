I'm trying to get more, smaller releases out the door… so I'm back, and I bring with me a tiny collection of fixes and tweaks that I've put together since the last release.

- After 2024.1 got out the door, I immediately noticed that I'd get a crash on a couple devices when doing a search because a change to how I was treating search queries was causing an Equatable and Hashable mismatch. This is why you don't write custom conformances to those protocols, kids!

- When cancelling a search, one expects that one can just go on living life. However, a bug was causing GIFwrapped to crash if the results hadn't come back yet, and that just wouldn't do. I fixed the issue where the section was being released unexpectedly, made sure things got cancelled appropriately, and now one can expect life to return to normal.

- It seems like there was some issues with the way the IAP validation was being done on macOS… it's just slightly different enough of a process that I had to rewrite some bits to get everything working as expected. That said, it should work properly now, just in time for me to rip it all out and replace it with some sweet, sweet StoreKit 2 code.

- A change I made to the 'Save to GIFwrapped' extension accidentally broke importing GIFs where the source application provides a file URL, like the Photos app. Thankfully, I got a lovely email from someone who set me straight, and now it's working as it should once more.

That's it for this one! Small but meaningful. If you want to reach out, chuck an email towards support@gifwrapped.co, or hit me up at jellystyle.social/@gifwrapped if that's more your jam.

Until next time, remember: don't be a turnip.