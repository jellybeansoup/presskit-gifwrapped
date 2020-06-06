There’s nothing like a string of unrelated events that take what was intended to be a smallish release focused on resolving a handful of bugs, and just blowing it out into a huge release with a bunch of additional features and enhancements.

Now if you’ll excuse me, I need to collapse.
 
- Some of you may have heard about a ginormous data-sucking monster buying Giphy, a.k.a. the search engine that powers GIFwrapped's search. In response, I feel a significant need to drop them like a hot coal, so I started by adding Gfycat and Tenor as alternatives, and then straight-up switched the default to Tenor (which is owned by Google… so only slightly better). For what it’s worth, you can still access the others: just include the bang !gfycat or !giphy with your search, and GIFwrapped'll use the respective engine for your search.

- Ad networks suck for various reasons, but ads have always been a part of GIFwrapped's strategy, so I decided to swap out the big, skeezy ad network for some home-rolled code. There’s still a lot of work that’ll happen with these behind the scenes, but my aim is to have a variety of ads that honor your privacy and supports independent creators.
 
- As if I needed more to do, Twitter went and updated their website in such a way that it broke my ability to parse tweets in search of their sweet GIFs. Anyway, solving this was two-fold: websites are now loaded using a hidden WKWebView so that any javascript can run as desired, and then my tweet parser should now also handle the updated markup.

- I've had a decent number of emails and tweets telling me that the app would lock up during saving, deleting, or practically any situation where the library contents are being modified. This is a really tricky issue to solve, especially when I can't replicate it on my end, but I took a dive into my threading and locking code to try and alleviate any potential pain points I could find. Fingers crossed, I guess?

- When using Dropbox, library changes weren't properly getting pushed to the server unless an image was accessed or modified, which is sorta weird, and not entirely desirable. It should now make an attempt when sync is first started up, just in case.

- In other Dropbox news, the library wouldn't get cleared out properly when disconnecting, likely due to some incredibly minor change that happened months ago and flew under the radar. Love it or hate it, this is the intended behaviour, so I went in and fixed it up. Please throw your tomatoes one at a time.

- Fun fact: the main UI actually has two separate search bars that are kept in sync. One lives in the "drawer", and the other is popped into and out of the navigation bar as needed on iPad. Problem is, they could get into scraps over whose job it was to perform a search, causing a crash. Here's hoping they play nice going forward.

- Malformed paths were still a thing that I was seeing errors for, and it turns out that, while implementing my "fix", I fell for the same ambiguity that caused the issue in the first place. Good news is that I was able to fix it properly this time, and I also took a moment to clear up the ambiguous code, to avoid this sort of nonsense happening again.

- The preview transition where the image grows out of the grid view was a little… wobbly, and showing a few cracks here and there. So I took a closer look, and fixed a few small details that add up to a much smoother transition that uses significantly less memory. You're welcome.

- Thumbnails got a a little lovin' as I delved in and refactored the system that manages their creation and storage to make it easier for me to follow, and thus work better. I also made it a nice coffee, so it should hopefully be less likely to jam up or drop images now.

If you come across any issues with the app, I’m here to help… or at least listen, and then disappear while I head off to try and resolve them. Tweet @gifwrapped, or email support@gifwrapped.co, and I'll get back to you as soon as I can.
