Back again! Had a couple of tricky bugs to figure out this time around, and took the opportunity to add some of that sweet, sweet pointer action that you can do on iPad now.

- Took a pass at the low-hanging fruit around hover gestures on iPad, mostly hitting the spots that already had arrow key support (plus a couple of extra spots where it made sense). I'm sure there's more that can be done, but it's a great start.

- A few people (more and more) have been seeing a crash on launch which I just couldn't get enough information on to properly fix. Managed to sort the information part out in the last release, which allowed me to nail down a potential cause and resolve it. I'm basically a detective now.

- Chonky GIFs are and always will be problematic for me (due to their extra-cuddly size), and most recently they were blocking the UI for a moment when loading, which became real apparent when swiping through previews. One of the heaviest parts of loading a GIF is decoding the data, which the library I use does on the main thread (where UI stuff is done), so I moved that to a background thread and it feels muuuuuuch smoother now.

Until next time. Stay safe out there!