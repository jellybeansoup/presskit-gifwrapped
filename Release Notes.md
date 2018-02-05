Didn't take very long to sort out a new swath of problems, some of which might have been hiding out for a while now. What follows is literally a list of bug fixes and performance improvements, but… you know… a pretty detailed list of 'em.

- Made an adjustment to how the cache status is determined that should reduce the load it places on the CPU. It's actually a pretty small thing, but it can make a huge difference if there's a lot going on… and let's be honest, we don't need the added pressure.

- A couple of the icons in the app got a tweak here and there, most notably the Dropbox logo in settings. It's not a big thing, and you might not even care, but I'll bet some marketing executive just got a nice, happy feeling… and doesn't even know why. That's how marketing executives work, right?

- A parsing error was causing the thumbnails of Twitter GIFs to fail so completely that it made the whole feature seem broken. While this could be construed as a metaphor for the times we live in, the fix itself was very straightforward: just a matter of tweaking the code so that the generated URL was correct.

- Sharing images to Messenger broke at some point, likely due to how they expect GIFs to be shared (story of my life). I added the ability to wrap everything up just how they like it, and more importantly, the ability to adjust the next time they decide to change things on a whim.

- Despite each one being tracked centrally, the same download could end up being started multiple times, which is bad for so many reasons (like the progress bar in the preview screen being all whack-a-doodle-doo). A couple of quick additions to the relevant code should ensure that it doesn't happen anymore.

- The preview screen was getting stuck after it was supposed to be dismissed, which meant the contents (i.e. GIFs) were being kept around (thus eating all the memory like they were delicious snacks). Made some adjustments to ensure this isn't happening anymore, and now it's just like a bought one!

- The little spinner for each of the thumbnail cells in Search and Photos wasn't kicking in, which was slightly disconcerting if it took a second before downloads kicked in. We had a chat, and everyone's on the same page now; no more blank screen of vague uncertainty.

Thanks for using the app! If you want to get in touch, you can find me pretty easily. Shoot an email to support@gifwrapped.co, or look for @gifwrapped on Twitter, and I'll be here to help with problems, consider your suggestions, and sort out any bugs you happen to find! If you'd like to help support GIFwrapped, I'd be really honoured to read any reviews you leave on the App Store. In the meantime, stay cool and don't stop believin'!
