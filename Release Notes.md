Well, hello there. It's been a while! I, uh… *checks notes* …have a release for you? It's a good one, I promise.

- The preview screen has seen a number of improvements and rewrites in this release, like the introduction of a new inspector for the info view on iPadOS, subtle accessibility tweaks, and the death of a solid number of very minor bugs. It's been a big task, pulling apart the absolute nonsense that existed before and weaving it back into something infinitely more stable and maintainable, but if you're keen to know what I've been doing for six months… it's avoiding this.

- It's no secret that I've been wanting to find a solid alternative to Firebase, and while it's not easy to find something that is financially feasible, the upcoming GIFwrapped for macOS release forced my hand, because Firebase Analytics doesn't work on Mac Catalyst. As such, this update replaces Firebase with Bugsnag for capturing crashes, and TelemetryDeck for analytics.

- GIFwrapped has had a custom search bar implementation for the search card (on iPhone and split screen iPad) for a long while, but I needed to replace it with the system version for… REASONS. Which I did. It's also not eye-burning white any more, so there's that.

- For a long while, the main grid view of GIFs has been missing the tiny, single pixel high separator between each of its rows. This always bothered me, but clearly not enough to be able to add it as an issue in my bug tracker. UNTIL NOW MUAHAHAHAHA

- I'm attempting to right some wrongs that I made years ago with GIFwrapped's library storage by actually using a database (don't @ me)… but it's a big, long process. Step one: improve the data structures so they can be properly replicated in a database, which I've started to do by using Codable structures instead of the serialised, wild-west dictionaries of the past. Yee haw!

- On occasion, the library could get stuck in a loop where reading from the on-disk store would cause it to write to disk, which would trigger a read from disk, and so forth. This could also very occasionally mean that actual changes got lost in the process, so I found a really rudimentary way to stop reads from directly triggering writes that I'm pretty sure future-Jelly will truly hate. At least it works. Bad for him, good for you!

- It was recently brought to my attention that Dropbox wasn't staying connected between launches, and to my dismay, I discovered the reason was because Dropbox switched to short-lived tokens back in… September 2021. Oops. I dug in and rewrote my authentication layer to deal with that, then updated GIFwrapped to be able to refresh the token as needed. That should be enough to allow me to forget all about this for another couple of years.

- The search card was behaving a little oddly after holding a GIF for a preview when the search bar was focused. If you then cancelled out of the preview, it'd reset the keyboard, but the drawer would end up with an extra offset. It's because there's multiple notifications being fired, so I throttled that business to just react to the important one (the most recent).

Thanks for using GIFwrapped! If you need to reach out, you can pop an email off to support@gifwrapped.co or hit me up via @gifwrapped on Twitter. I'm here to help, or at least to listen to what you have to say.

Until next time, remember to be kind to yourself (and to those around you).