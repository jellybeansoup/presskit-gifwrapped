Hello, everyone!

Work continues on the Liquid Glass design, but Tenor’s API is going away at the end of the month, and so it is sadly time to remove the engine.

Since it was the default engine, this means updating that too, so Klipy has officially become the default. It does feel quite empty in that list, though, so I might need to figure out some new alternatives down the line.

Plus a couple of bonus fixes:

• For whatever reason, the section headers in the About screen were a bit screwy, and one would randomly show at the bottom of the screen. A couple of people pointed it out recently, and it was an easy peasy thing to fix, so I jumped in and just did it.

• The icon selection screen has been a little bit eager during scrolling for a while, if you happened to drag while touching an icon, it’d end up selecting that icon. Turns out the trick was to fix the gesture handling so it’d link up when being added to the window, and not just the parent view. Who knew?

And that's literally it. This update is all about quality, and definitely not quantity. Or maybe a good time, not a long time. Whatever the case, if you need support, toss an email towards support@gifwrapped.co and I'll do my dangedest to sort things out.

Until next time, remember: it's always OK to be who you are.
