This update has been a long time coming. Aside from general life things, I've been hard at work improving many of the underpinnings of the app, some of which might be noticeable now, some not so much. Suffice to say that this work will continue, but hopefully a little more iteratively from here on out.

- The time has come to disable Twitter support. It's not something I do lightly, but it has been a long time coming. As of this release, Twitter/X URLs will throw up a special error and won't even attempt to fetch or parse the relevant tweet… or whatever it's called now. If you're curious, there's more detail on my reasoning available in the User Guide.

- Someone pointed out that the selected search engine isn't respected in the Messages app, so I spent a little too long rewriting a little too much code to solve that problem. Now the vast majority of preferences are stored in a way that will enable future use within extensions, and I can cross a small bug off the todo list. Definitely worth months of delay.

- As it turns out, each time a new window was opened on macOS and iPadOS (yes… you can have multiple windows!), GIFwrapped would re-run a bunch of operations that only really need to be run at first launch. This is problematic in a couple of ways, so I rearranged a few things to make things only run as many times as actually needed… which is to say "once".

- Swiping between pages and even sometimes opening a GIF was resulting in some crazy behaviour, and it would transition to the wrong image, sometimes even showing the right one and then replacing that with the wrong one. Turns out it was a system I use to pull updates to the image metadata to views which was crossing the streams and showing whatever came most recently. Not anymore though. Just one GIF at a time, thank you very much.

- There was also some strange behaviour with resizing the preview screen, both on macOS and iPadOS. It's a numbers thing, with the complicated scrolling and scaling logic all playing a little wiggly when not exactly right. I've made some adjustments, and it seems to work much better now, which is a relief. This also helped solve some issues with tall portrait images not playing well with the scrolling behaviour of the info panel on iPhones.

- I wanted to show the current state of the info screen in the navigation button, which turned out to be a deeper hole than I intended. Nevertheless, I succeeded in my mission, and you may all behold the fruits of my labour! First it's filled… then it's not… then it is again. MAGIC!

- While I was doing some concurrency work in the Save to GIFwrapped extension, I stumbled across the fact that the individual GIF pages on gifs.cackhanded.net weren't saving properly, which is the fault of the underlying parser not supporting it. I dived in, made a super minor addition, and now it works exactly as expected.

There's so much more going on under the hood of this release, but some of that is for another time. In the meantime, please enjoy this release, and as always… thank you for using GIFwrapped. If you need to get in touch, you can find me by emailing support@gifwrapped.co, or you can reach out to jellystyle.social/@gifwrapped.

Until next time, remember to tell someone you care about how much they mean to you.