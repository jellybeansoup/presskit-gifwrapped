Oh, hi there! You got here just in time for me to tell you about the improvements in this release. Nothing big, mind you; just a little touch up here and there to help GIFwrapped be the best it can be.

- When I made changes to the various sharing activities in the last release, I messed up the monitoring of the underlying progress, causing it to occasionally crash on iOS 13. In my defence, KVO is finicky… but it does help to actually handle the observation stuff in the right place, which I'm definitely doing now. Promise!

- In an attempt to improve GIFwrapped's handling of Twitter GIFs, I jumped in and made some small modifications to help it avoid failing before the underlying page finishes loading. This means you shouldn't be seeing errors that pop up briefly, only to be replaced with content a few moments later. It also means that the "Save to GIFwrapped" extension should finally work for Twitter GIFs again. Here's hoping it sticks for a while.

- While I was poking around in the Twitter-handling code, I was able to identify a couple more potential sources of tweet content, thus improving the chances that opening a tweet URL will have a happy ending, particularly on occasions when parsing the HTML itself falls over.

- On occasion, when switching from an app where the keyboard is being displayed, GIFwrapped would open up thinking that the keyboard was visible, causing it to look weird. I got a couple of bug reports about it, so I jumped in to try and stop it from happening. Fingers crossed!

- The custom preview transition was a little janky for anyone using retina pixel density, so I jumped in and fixed it up real nice. While I was at it, I took a pass at making the in-app explanation of this option a little more clear, because I've gotten confused emails more than once, which is way too many.

- I've had the option to disable URL sharing as a hidden debug option for a while, and in my desire to work towards a cleaner settings screen, I figured I could toss it in as an actual option. WHAT COULD GO WRONG

- The settings button felt wrong being above the grid view instead of being above the sidebar on iPad, so I moved it. Yeah, you heard me. I know I promised no big changes, but I really couldn't help myself.

That's it! Just a short on this time. I'm still over here continuing to work on improving things, so if you need to get in touch, just send an email to support@gifwrapped.co, or hit up @gifwrapped on Twitter. I'll do my best to help you out.

Until next time!