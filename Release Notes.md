I don't know about you, but from where I'm standing, 2021 feels a bit like life is pressing the pedal to the floor. As such, it's time to make good on the, uh… threat …I made back in January: this is the last GIFwrapped release to support iOS 13. On the up side, I've spent a little time duct taping a few sore points to try and improve things before I drop it like a hot coal.

- I ran across a few ways that the iCloud sync engine was causing duplicates to be created within the library. One was caused by moved or renamed files being synced from iCloud and GIFwrapped being unable to find the file locally (meaning that GIFwrapped treated it like a new file), the other being that when moving a file the update to the data store could end up happening twice. I tightened things up, found a way to better connect local copies to their iCloud counterparts, and GIFwrapped's iCloud sync should officially be the best it ever has been.

- I took a dive into the screen for renaming and moving files in an attempt to make it a little smarter, a little easier to understand, and a little harder to get into a situation where one could actually break stuff in one's Library. This is predominantly just a UI refresh, and it's not perfect, but I'm hoping it'll help make moving and renaming stuff clearer.

- The link on the Premium screen for managing subscriptions got broken when Apple changed it a while back, and it took me way to long to notice, and way too long for me to fix once I did (and I only did because a few nice people pointed it out to me several times, while I clearly just ignored them like a jerk? I'M SORRY, NICE PEOPLE. YOU DESERVE BETTER).

- In an effort to curb the usage of App Store reviews as support requests, I've removed the link to write a review from GIFwrapped's Settings screen. You're still free to write a review—especially if you have nice things to say—but you'll have to do it the old fashioned way. Sorry!

Thanks for using GIFwrapped! I'm still over here continuing to work on improving things, so if you need to get in touch, just send an email to support@gifwrapped.co, or hit up @gifwrapped on Twitter. I'll do my best to help you out.

Until next time, remember: BLACK LIVES STILL MATTER.