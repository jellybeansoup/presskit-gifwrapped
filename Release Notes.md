The quest to stabilise v2 continues with a bunch of additional tweaks and changes to alleviate various crashes, failures to launch, and straight up freezing. I know these problems have continued to affect many of you, even after I patched a number of problems, so thank you all for being patient while I worked on sorting these new ones out.

- The iCloud on-boarding was being unnecessarily displayed if the Library's metadata hadn't been loaded in time to determine if it was necessary. To resolve this, I've forced it to wait for the metadata to be ready, and otherwise added a flag so if you see it once, you'll never see it again.

- Opening images from Files.app was a little weird under certain circumstances. I made a small change that should ensure we correctly handle any downloading that needs to happen in the background, so the app doesn't get stage fright and freeze up before displaying the image.

- When searching (by actually hitting the Search key), the queries were often being run twice: once to grab the result prior to displaying them, and then again, upon actually displaying them. This was caused by the status of the first query being cleared out when dropping the items into the UI, so stopping that from happening quickly sorted things out.

- Search wasn't always showing useful errors… like if GIFwrapped doesn't have permission to access Photos, or if there's no internet. This didn't make sense to me, so I tracked down the underlying problems and fixed them, resulting in an overall much improved search experience for all!

- The Library's messages about having no results were at best unnecessary, and at worst confusing as all get out. I've stopped it from displaying when there's more important content (like actual results), and tweaked the copy to better indicate how one uses the new universal search bar.

- While working on other issues, I stumbled upon a small piece of code that could potentially cause big lockups, due to reading files from the main thread (definitely a no-no). Under the best possible circumstances, it should only ever have caused a little stuttering when scrolling, but that sort of thing has a tendency to balloon out… so I fixed it.

As always, I do try to be available if you run into problems while using GIFwrapped, so just toss an email at support@gifwrapped.co, or hit me up @gifwrapped on Twitter. I'm here to help!