Small update this time around, to attempt a quick turnaround on a couple of bugs that were causing people headaches. Sorry about that, y'all!

- To get the preview transition animation right, the two screens involved compare notes on where the image comes from. If paging is disabled (like because it's a premium feature, and not everyone has Premium?), the two views can have _very_ different ideas, and this caused significant problems. I helped the two calm down and talk to each other, so it should be ok… for now.

- I'd made some last minute changes to the diffing used for the bookmarks view (it was custom, and I wanted to rip it out in favour of DifferenceKit, yes I know iOS 13 has it built in, get off my back MUM), and it made it so that clearing the clipboard would mess up the updates and crash. Anyway, it's fixed now, go team!

Hope you've been washing your hands. Until next time!