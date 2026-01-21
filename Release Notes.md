G'day! Hello! Good Morning!

Welcome to 2026, ostensibly a year that is at least numerically greater than 2025. Let's start it off with a sweet little GIFwrapped update, shall we?

It's worth noting that fortunately/unfortunately, depending on how you see it, this release doesn't have "Liquid Glass" just yet. Trust me when I say I'm working on it, and I'll do my best to make it as nice as I can.

• A lot of people have noticed the missing navigation buttons on the main screen, which has been making it harder to get into the settings screen. This was a bug introduced by the latest OS release, and I had to do a little juggling to get them to show up properly.

• With Tenor pulling a Twitter and discontinuing its public API later this year, I'm on the look out for something to fill the gap. Its death would've meant that Giphy would've been the only engine supported, but then I was informed of the existence of Klipy, and so I quickly spun up support for it. You can select it as your default in the Search settings screen. You're welcome.

• Sometimes when looking at a GIF, you just want to be able to pause and appreciate each frame, and while you've been able to scrub through (as a Premium subscriber) with the playhead for a while now, I wanted to make it easier to do so from the comfort of a keyboard. As such, I've added , and . shortcuts that allow frame stepping, similar to YouTube or QuickTime.

• A few months back, I got an email asking me to add the ability to get GIFs from Yarn, and given that it was actually not too difficult to do, I went ahead and tossed in a basic handler. It's given me some ideas to potentially improve the basic web parsing too, but that'll have to wait for another day. You get what you get.

• It seems like Dropbox sneakily changed it's API again (it has been a while, to be fair), this time changing one of the endpoints used for signing in, which meant you could sign into Dropbox from GIFwrapped. I've updated that, so it's working again. Sorry to those who were quietly suffering with this one.

• While I was in the Import menu, replacing icons with SF Symbols and doing a little cleanup, I took the time to dig further into the File Sharing screen which I uplifted to SwiftUI a while ago. This time I made it use Structured Concurrency (effectively nerd talk for stopping it from causing the app to freeze) and also get thumbnails from Quick Look. With that and a couple other small niceties, the least used screen in all GIFwrapped is now also possibly the nicest. Go figure.

• GfyCat died a while ago, and it's taken me a bunch of time to finally remove it from the list of search engines. RIP GfyCat. I wanted to like you so much, but you were probably the least supported API I've ever used.

That's it, I hope you enjoy this update! If you run into any issues, don't hesitate to toss an email my way, via support@gifwrapped.app, and I'll see if I can help you out.

Until next time, don't forget to brush your teeth twice a day. Happy 2026!
