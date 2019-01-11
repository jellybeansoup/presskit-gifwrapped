This update is small, but powerful… it's been a busy week as I've powered through all the bugs I could get my hands on, and bringing everything back up to snuff. Thanks for being patient while I sorted it all out, you're the best!

- A small bug in the updated Dropbox engine caused sync to happen in app extensions (like the Messages app) instead of in the app itself, resulting in many users experiencing a "Waiting for Dropbox" issue. I've fixed the bad code, so it should be all good now… we can all get back to waiting for Godot instead.

- A bug report about duplication of images added to the library took me down a the rabbit hole of how downloads are handled in certain cases, and eventually lead to improving the performance of downloads overall, while also fixing the reported bug. NICE!

- Saving GIFs from the share extension could some times result in no file extension being added (the .gif part), which has all kinds of implications. Fortunately, I was alerted to this travesty… and thus the issue is hereby resolved. Thank you, and good night.

- Did a bit of a minor overhaul of how updates for the grid view are prepared, which should hopefully improve their reliability a bit. I was seeing some super rare (but annoying) crashers pop up, and honestly I just wanted to play something other than whack-a-mole for a while.

Remember, I'm here to help! Comments, complaints and support requests can be sent via email to support@gifwrapped.co, or you can hit me up @gifwrapped on Twitter.