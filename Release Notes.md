Despite the (somewhat hasty) fixes for Twitter importing that went out in my last release, GIFwrapped was still having issues importing GIFs from Twitter in certain cases, so I had to go back and do some additional work on it.

- The Save to GIFwrapped extension was crashing before it could parse links (like, say… Twitter links), due to the web content being loaded off of the main thread (bad developer, BAD!). I made a few changes to make sure the important calls are handled correctly, and it should be more stable now.

- I was also finding that the results being returned could be… variable, based on the position of the moon, the speed of XHR requests, and which leg I was standing on at the time. I went back and tweaked the way GIFwrapped handles knowing when a page has finished loading (it'll load initial results, but then continue to update as the various XHR requests complete). It's not perfect (the in-app experience is superior because it's not under time pressure), but this has helped ensure that as many results as possible are produced.

- Tweets marked as sensitive (typically because they're… naughty) used to work in GIFwrapped, but the link for the GIF got properly hidden in the recent Twitter website update, which made it not so worky. I made (significant) changes to how Twitter's site is parsed in an attempt to make a best effort to retrieve GIFs from any tweets, but if all else fails, the error should at least be more accurate as to what caused it to fail.

- I still get emails from users experiencing lock-ups that I cannot detect or replicate for the life of me. Each time I do, I go into the code base and look for any possible reasons that the app could get into such a state, and then do what I can to relieve it. It hasn't worked so far, but maybe the changes I made in this release will have an effect?

- Thumbnails are another source of support grief, and in this release I discovered a couple of points where the code could just… not download thumbnails. Add to that some improvements to how it handles the sheer number of downloads that can be spun up during first load, and hopefully it should be improvements all around.

If you find any issues with the app, or want to send me a much-needed morale boost, tweet @gifwrapped, or email support@gifwrapped.co, and I'll get back to you as soon as I can.
