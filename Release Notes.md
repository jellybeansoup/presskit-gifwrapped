Oh, hi there! It feels like it’s been a while. Has it been a while? I may have gotten a little caught up with all the wild new things I’m able to do by dropping support for iOS 11 and 12, but I think we’ve all made it through in one piece. Except that one person over there who appears to be… uh, three pieces? Awkward.

- As of this release, support for iOS 11 and 12 has been dropped, and the plan is to move to iOS 14 only in a few months time. This is a necessary move for GIFwrapped to keep improving and expanding into the future, as it means that I can utilise more system features and… don't have to keep old, busted code around. Who's ready for some new hotness?

- I wanted to try out a new bookmarks sidebar for the (eventually) upcoming macOS app, and found myself liking the concept enough that I figured I'd leave it in for iPads running iOS 14 as well. It also gave me the opportunity to upgrade the bookmarks system under-the-hood, so it means improvements for everyone (even on iOS 13)! You get improvements, and YOU get improvements! Hooray!

- The GIF preview screen also got an overhaul, with everything from improvements to the (Premium) paging feature, to GIF display itself. As a bonus, Premium subscribers now get a scrub bar that allows direct manipulation of the GIF playback… it’s almost like being able to control TIME ITSELF! Almost.

- iOS 14 brought with it warnings letting you know when the clipboard is accessed. In GIFwrapped, they were constantly being triggered by the presence of a couple of buttons used to make pasting from the clipboard a bunch easier, but I was able to refactor them to allow them to detect when they were necessary without actually touching the clipboard contents, so no more warnings… unless you enable the clipboard preview in settings.

- If one wanted to get GIFs from a Tumblr blog, one totally could… but it wasn't exactly the best experience.  You'd be limited to posts on the first page, and you'd often end up with duplicates caused by different sizes of images being embedded in the page. So I wrote a proper engine to handle Tumblr blogs. Just pop in the URL, and off you go.

- I swapped out the underlying library used to create zip files within GIFwrapped (for a handful of uninteresting reasons). It’s not a perfect improvement, as the new code is slower than the old code, but everything is working smoothly, and the plans I have for this stuff can now be implemented, so I'm calling it a win.

- Downloading GIFs from Twitter was sometimes blocked by an error indicating that the image was empty, i.e. no pixels. Under the hood, variable frame rates were causing the actual number of frames to be different to what I was calculating, and iOS didn't like that. By going through the frames ahead of time, I'm now able to both get the correct number of frames and also calculate the correct duration for each, so the video converts as expected.

- As it turns out, if a search engine somehow returned duplicate results (i.e. the same GIF, but more than once), GIFwrapped would break down sobbing and crying on the floor, not knowing what to do. I let it know that it's OK to just ditch any duplicates, so this shouldn't happen any more.

- Ever since I introduced forever-dark-like-my-soul mode to make popups and modals fit better with GIFwrapped's colour scheme, the little text field for naming new folders had black text on a very dark grey background. I fixed it, but let's all just pretend it was like that for, uh… stealth reasons, OK?

Thanks for using GIFwrapped! If you discover any bugs (the software kind), and would like to see them sorted (again, the software kind… I’m not killing spiders for you), toss an email to support@gifwrapped.co, or tweet @gifwrapped. I’m listening, and I’ll do my best to help where I can.

Until next time, remember: you are valid, and you are loved.