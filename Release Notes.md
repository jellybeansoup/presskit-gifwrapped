Hi there, and welcome back to another episode of "GIFwrapped Bug Fixes and Performance Improvements: Have Things Been Fixed? Have They Fixed The Things I Specifically Have Issues With??? Let's Find Out!" with your host… me!

Last time, we fixed a bunch of issues and made performance improvements, but I know what you're wondering. You're thinking, "Have more things been fixed? Have they fixed the things I specifically have issues with?"

Well… let's find out!

- Fixing one issue in the preview screen uncovered a crasher (though not soon enough for me to ship), caused by an observer sticking around after the image metadata it was watching was gone. It might sound complicated, but it was just a matter of enforcing an order to events, so now the screen can be dismissed just fine.

- Added an extra layer to the Dropbox warning system to suppress the alert when the app isn't actually in the foreground. I think this might have finally stopped it from showing up unnecessarily, it's kinda hard to tell. Keep an eye on it, and if it even so much as twitches… beat the dang thing with a stick.

- Updated the text for an alert that I added several versions back, but had never actually wrote proper copy for. I'm not super sure it'll even get shown at any point (it's a pretty obscure problem), but the fact that I've finally fixed it should alleviate those stress dreams I know y'all were having.

- There was apparently some kind of outlined consume happening within the code, causing crashes left, right and centre. If you have no idea what an "outlined consume" is, that's OK. Neither do I! I really just kinda stabbed around in the dark until I felt like I hit something. Which means there's either no more bug, or a really angry, partially-stabbed bear hanging out in here. PLEASE LET IT BE THE FIRST ONE

- If the library had to remove all its items—which doesn't happen often—the instructions given to the UI could end up being wrong, causing it to get out of sync with the actual data and everything would go slowly downhill from there. I solved it though, so it's pretty much a non-issue now ¯\_(ツ)_/¯

- On occasion, an image might not have a thumbnail available, and if the planets align on the night of the solstice, when a full moon is visible from the well of Ashur… it could cause the thumbnail not to load at all. I've added a fallback so it goes for the actual download just in case, and the world is safe once more.

- If dimensions for an image weren't available (like if it hadn't been downloaded yet), the value it used to determine the size of the preview would be capital-B banana pants, and the app would crash as a result. This shouldn't be a problem anymore, as it now checks for invalid values/fruit-like pants and just sticks with the default when necessary.

- OH GOD… DID YOU HEAR BEAR-LIKE GROWLING JUST NOW

- The clipboard bookmark in the Search tab could quite easily find itself with a value that didn't match the label if multiple attempts at using the clipboard occurred. Somehow, it took me a while for me to actually see this in action, but everything's been sorted out, and should work as expected now.

- When using the save options found in the info panel, the app could bypass any check to ensure that it as valid, and end up crashing because things were all weird. I tracked down the underlying error and sorted it out, so no more of that crazy behaviour.

If you're having problems with anything, I'm more than happy to take your emails and tweets and do things with them! Mostly this means replying with helpful guidance, but occasionally might involve eating said emails and tweets for nourishment. Either way, follow @GIFwrapped on Twitter, or send an email off to support@gifwrapped.co, and I'll be here… hungry and waiting.

Mostly hungry.
