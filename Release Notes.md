I know! Just when you were thinking "Geez, that guy who makes GIFwrapped must be taking one hell of a nap," I appear out of nowhere and bring you an update. It's just what I do.

- The big news with this update is that I finally got fed up with my insanely fragile Twitter integration, so instead of doing the normal thing and fixing it, I tore the entire Search infrastructure that I built and re-did the whole thing from scratch… and this time I didn't just use a paperclip and a wad of gum. Much better. YOU'RE WELCOME.

- I was also scrolling through the simulator the other day, with a bunch of thumbnails downloading from my Dropbox library… when I stumbled headlong into a UI lockup. I took a beat, dug into it a bit, and discovered that past-Jelly chose to make every access of the connected sync client one where it has to iterate through a list and verify that the client is connected, which is… bad. Good news: it's not that way any more.

- At some point, the About screen's illustration started getting weirdly inset from the screen edges, so in a fit of mild annoyance, I ripped out the SwiftUI-powered List in favour  of a proper compositional layout in UIKit. Future-Jelly will probably regret this move, but he can go jump in a lake… at least this one looks and works as intended.

Thanks for using GIFwrapped! If you'd like to reach out and tell me secrets (only good ones please), you can do so by emailing support@gifwrapped.co.

Until next time… eat your vegetables. Unless you're a carnivore.