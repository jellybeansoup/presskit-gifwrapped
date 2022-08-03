There's no shortage of things to improve within GIFwrapped, and so I've been hard at work improving things (as I'm sure you know). This release in particular has some real doozies.

- A mate of mine has been gently nudging me for months about an issue with downloading and displaying the preview for GIFs stored in iCloud, and because I'm a good friend… the problem has sat in my backlog waiting for me to spend time on it for months. The good news is that I finally did, so downloads from iCloud are now less likely to fail immediately after a cold launch, or when using the Messages app. Aren't I _such_ a good friend? DON'T ANSWER THAT

- iCloud downloads have historically also been a source of UI lockups, particularly when a bunch are happening all at once. With this in mind, since I was in there already, I decided to refactor things to be a little less of that. Feels much better… to me at least.

- Scrolling the main grid was real janky on macOS, and I never really dug into exactly why. At some point I did make some minor improvements, but nothing particularly noticeable… until I recently looked into why the memory usage was so high. Turns out both issues had the same cause: the thumbnails were e-flippin-normous. After a little tweaking of the grid scaling to reduce the overall scale, the memory usage plummeted and the grid now scrolls very nicely. You're welcome.

- I've not exactly been thrilled with the Settings screens that I built out in SwiftUI, in part because of simple stuff, like the fact that the Search History screen in Settings lost its search controller because of the way that SwiftUI embeds UIViewControllers. So when a mate of mine (not the same mate for those keeping score) showed me how to have my cake and eat it too, I was so thrilled that I just had to get it in ASAP.

- I've been noticing a regular issue where results from search engines fail to be decoded for one reason or another, which isn't ideal. I adjusted the parts that were failing to make 'em a little more robust (stupid APIs returning empty strings instead of nil), and they should be OK from here on out.

If you have a particular bug you'd like to see fixed, you'll be super pleased to know that you can tell me all about it. Either send an email to support@gifwrapped.co or tweet @gifwrapped… or even jump on r/gifwrapped and let me know what you're thinking. In the meantime, I'll just be over here continuing to make things a little better for y'all.

Until next time!