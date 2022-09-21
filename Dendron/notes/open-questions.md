---
id: 4pnkm3k35yiexe0248selrw
title: Open Questions
desc: ''
updated: 1663735374782
created: 1663734658506
---


## Other questions
### Is there a drawback to making ctrl-enter use "Dendron: Go to" instead of "Dendron: Go to note"?
[Google](http://www.google.com) will let me "Dendron-go to", but not ctrl-enter- which is "Dendron: Go to note"

[[new-note]]

### Does email address link work?
<jeepeterson@yahoo.com>
nope... normal preview it works, dendron preview it doesn't

### What's the best way to make nested lists
1. Do I just use intented text?
    1. This is indented
1. Or I can indent with block quotes
> 1. Either way, can I make a third level different?
>> 1. Or must it be letters too?
1. I like bullets, but why are these all the same? Is there a way to make them render differently? If so, I could use those to make my lists.
  ~~~
  * asterisk
  + plus
  - dash 
  ~~~
1. I feel like I'll need to come up with a format using heading since this restarts the numbers. It takes 4 spaces to keep the numbering, but hitting tab apparently has some "smarts."
    * asterisk
    + plus
    - dash 
1. This will keep numbering
> * As will the next, I assume
1. Test

### Is there a way to "discover" missing links? Ideally a "soft backlinks" list that shows not just the actual links but a list of files that contain that word or phase (I got used to that with org roam)
For example, here is how org-roam handles it: https://www.alexeyshmalko.com/_next/static/resources/0054e849f5934a1513dd/20210718141902-screenshot.png

### Are we still limited to 6 levels of headers, since it's just MD? Or is there a workaround for that?
 
### It appears we still prevented from starting lists at an arbitrary number? I assume that is still an HTML limitation and this renders everythign to HTML?
Derek opened an issue.
~~~
3. Will render as 1
5. Doesn't matter the number
~~~
3. Will render as 1
5. Doesn't matter the number

### Is there a way to make checkboxes without putting in a list?
[ ] should be a checkbox in my mind
AR: create feature request for this.