This latest GIFwrapped release has been met with amazing love from everyone. Even the new GIFwrapped Premium subscription, which was pretty unexpected (if I'm being honest). There have, of course, been some issues, and this update should hopefully resolve a couple of the worst ones.

- Attempting to load more results in situations where there wasn't results to be loaded (like in the Library) was causing crashes on iOS 9/10. This is mostly due to what was likely a bug that got fixed in iOS 11, so I added some extra checks to ensure I'm supposed to even be checking for content before relying on the iOS stuff, and boom! No more crashes.

- There are occasions when the collection view's internal data gets out of sync with the real world, and I'm still not entirely sure why (there are so many contingencies to avoid exactly this sort of thing). I moved some things around to simplify the logic and gather a bit more data as to why it's happening. Here's hoping we'll see some results from that.

- There were occasional issues with the Premium screen's layout, causing it to go all wiggy (I mean ALL WIGGY). Things would overlap, or simply not refresh properly, but I tracked down the underlying problem (conflicting constraints, for those in the know). It's still not perfect, but things have smoothed out considerably.

- The illustration for the Premium screen was using too much memory for my liking… something to do with loading the images… which I'll admit were kinda unnecessarily huge. I made some adjustments, broke the whole thing up into it's components, and dropped the total memory usage by like 75%. I'm calling it a win.

- Restoring purchases wouldn't warn you if it couldn't find any to restore. This might seem trivial, but there was the potential for confusion if someone disabled their subscription, and thought restoring would get it back. Stranger things have happened.

- If you're the sort of person who likes to add a little extra bling to their home screen, you're in luck. This version adds the option of a couple of alternate icons for GIFwrapped Premium subscribers, which should help show just how much better than other people you are. Pretty sure that'll put you in league with our cat, Turbo.

Thanks again for all the support! Remember, it goes both ways… so if you need assistance, please reach out to me, either by emailing support@gifwrapped.co, or by hitting up @gifwrapped on Twitter. I'm always here to help.