Time for another GIFwrapped release, with fixes for bugs and some minor improvements. Very, very minor.

- Pretty quickly after WWDC, I started to receive messages to let me know that the app was crashing on launch for a specific subset of very eager updaters. I don't officially support future OS versions (and I'm certainly not allowed to talk about them), but what can I say? I'm a softy.

- Ever since iPadOS introduced native keyboard navigation, it's been at odds with the version I built a year or five back. This is good and bad, because while I'm definitely keen to delete code, I'm not in a position to do so juuuust yet. In the meantime, I've done what I can to improve things a touch, just to make it usable again.

- The "Get Info" option in the context menu isn't really used that often, so it should be no surprise that it got broken on iPadOS and macOS somewhere along the way to updating the preview screen. A little rearranging of the logic to have the UI state updated at the right moment, and the option works once again.

- The advanced command words (which start with a bang and allow you to use an alternate search engine for a query) weren't working correctly because, for whatever reason, they were getting left in the query being sent to the server, and it'd totally bone the results you got back. I reworked the way it's handled, and now they work again. Clockwork.

- I wanted a better solution for my logging and analytics infrastructure that would let me share most of it between a bunch of my various apps with minimal effort. To do so, I ripped most of the good stuff out of GIFwrapped and into a format I could share, then reintegrated the whole thing back in. Not a big deal for you, but a decent quality of life improvement for me.

Thanks so much for using GIFwrapped! I really hope you enjoy it, and if you don't… I guess you could probably reach out to me and let me know why? Emailing support@gifwrapped.co or tweeting @gifwrapped should get your words in front of my face, and from there I will do what I can to help.