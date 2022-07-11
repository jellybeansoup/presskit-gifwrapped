I'm back, and it's been a hectic week… at least in part because I've been cobbling together fixes for the highest priority issues to come out of the latest release. In all honesty, this is why big releases that take a long time are dangerous: stuff slips through the cracks. If you got caught up in the nonsense, then please know: I'm truly sorry.

- In moving the library state over to using Codable structures, I forgot to account for dates as being a type of thing that needed to be decoded. I know, right? This obviously came back to bite me when a bunch of people who use Dropbox or iCloud sync updated to find their local library empty, which was simply because the data couldn't be read from disk correctly. Not… ideal.

- Dropbox's short-lived tokens are the gift that keeps on giving. The token update did help to ease a lot of issues—because the token could actually refresh—but there were still some calls that would occur after expiration, so they'd error out until the refresh occurred. I've now made it so that the token is pre-emptively refreshed for all Dropbox API calls, so there'll be significantly less of that nonsense.

- A small difference in padding between vertically and horizontally stacked labels in the GIF Info panel was causing constant layout updates and—in some cases—causing the app to completely lock up when opening a GIF's preview. Once I tracked it down, it wasn't hard to resolve: just make certain calculations use the intended value rather than the current one. Very obvious… in retrospect.

- I'm never against introducing a small engine to GIFwrapped, especially when a website's creator uses and enjoys the app. So this release adds a bonus: rudimentary support for parsing the pages of @cackhanded's prolific GIF website, https://gif.cackhanded.net. Plug in a URL (or use the share extension) and you're off. Thank me later (or more aptly, thank Mark Norman Francis, whose collection is… extensive).

Thanks for using GIFwrapped! If you need assistance, are still hitting bugs, or just want to share the love, please feel free to reach out to me via @gifwrapped on Twitter, or support@gifwrapped.co if you prefer all things email. I'm here to help where I can, or at least take notes so I can make my updates better.

Until next time, remember: a GIF is worth a thousand JPEGs.