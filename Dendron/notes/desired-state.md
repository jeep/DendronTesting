---
id: 5whbl1or5si0kn3sul5vvpg
title: Desired State
desc: ''
updated: 1663521646586
created: 1663433606814
---

# Recommended agenda
1. Review desired state (Joe)
1. Feedback on desired state (mentor)
1. Set up and additional vaults and workspaces needed
1. Process sample notes [[daily.journal.2022.09.15]] (Joe drives, mentor navigates)
1. Set up next day (Joe drives, mentor navigates)
> 1. Migrate open tasks (might already be done when processing)
> 1. Todo setup
1. If time, maybe look at converting .org docs (C:\Users\jeepe\OneDrive\Documents\TestDendron\mostlysafe-to-share-org)

# Requirements
1. Separation of work stuff which cannot be committed externally and personal stuff which I don't want embedded in my work notes for privacy reasons
1. Able to see interactions with people (expect backlinks with a person note)
1. Easy use of project vaults to segregrate knowledge from project work
1. Daily notes captured easily and then reorganized as desired (leaving links in daily)

# Work Computer
## Work workspace 
+ Peacock to have special color to indicate "do not push to remote" and not safe for personal info
1. [[Worknotes vault | #worknotes-vault]] (why does [[#worknotes-vault]] render to the page title)
1. [[Shared Vault | #shared-vault]]
## Personal workspace
+ Peacock to have special color to indicate safe to push and safe for personal information, no work details
1. [[HomeNotes vault | #homenotes-vault]]
1. [[Shared Vault | #shared-vault]]
1. [[HomeProject vault 1 | #homeproject-vaults]] (1 - 3 of these)
1. [[HomeProject vault 2 | #homeproject-vaults]]

## Vaults
### WorkNotes vault 
+ Local git repo
+ See structure
> #### contacts - c.* (not a huge fan of c, but p is taken by projects)
>> I kinda would like to have all the contacts be in my shared vault, but see how I want to keep daily notes, too...
> #### daily
> #### intel - i.* (reference notes for work specific stuff)
> #### meetings - m.*
> #### projects - p.*
> #### todo

### Shared Vault 
+ Sync'd to github
+ Shared via OneDrive.
+ Will it be a problem if shared? Will each edit overwrite or will there be a prompt to reload or is there some nice merge?
+ Could be split into people and reference to be more correct with the naming
> #### games
> #### languages
> #### literature
> #### people (Primarily want this for the backlinks)
> #### technology
> #### science
> #### ...

### HomeNotes vault
+ Sync with github
+ Stored on OneDrive for easy sharing
+ Same questions as people vault
> #### projects - p.*
> #### daily
> #### todo
 
### HomeProject vaults
+ Likely to be 3 of them at a time
+ Mostly for things that I want to keep a separate knowledgebase for
+ Custom structure 
+ ex. Active books/stories that I'm writing

## Other questions
### Is there a drawback to making ctrl-enter use "Dendron: Go to" instead of "Dendron: Go to note"?
[Google][http://www.google.com] will let me ctrl-click, but not ctrl-enter

[[new-note]]

### What's the best way to make nested lists
1. Do I just use intented text?
    1. This is indented
1. Or I can indent with block quotes
> 1. Either way, can I make a third level different?
>> 1. Or must it be letters too?
1. I like bullets, but why are these all the same? Is there a way to make them render differently?
  * asterisk
  + plus
  - dash 
1. I feel like I'll need to come up with a format using heading since this restarts the numbers. It takes 4 spaces to keep the numbering, but hitting tab apparently has some "smarts"
    * asterisk
    + plus
    - dash 
1. This will keep numbering
> * As will the next, I assume
1. Test

### Is there a way to "dicover" missing links? Maybe a "soft backlinks" list that shows not just the actual links but a list of files that contain that word

### In tables is there an easy way to line up the pipes?
~~~
| Title1 | Title2 |
| :--- | :--- |
| This sentense is quite long but I don't want to manually line thigns up| or do I rely on the preview? | 
~~~
So it looks like this?
~~~
| Title1                               | Title2                                       |
| :---                                 | :---                                         |
| This style table is readable in text | And I don't really care about the right side | 
~~~

### Are we still limited to 6 levels of headers, since it's just MD? Or is there a workaround for that?
 
### It appears we still prevented from starting lists at an arbitrary number? I assume that is still an HTML limitation and this renders everythign to HTML?
3. Will render as 1
5. Doesn't matter the number

### How can I force hanging indents with long text?
* This is a really long line, like longer than I want to be on one line, so I will need to wrap the text at
some point, I guess here.
* This is the second item. It's also longer than I would like on a line. But I'll manually indent it this time 
  so that it lines up
*   The other options is to always use tabs.
    Which will be easier, but it's not what I'm used to

### Is there a way to make checkboxes without putting in a list?
[ ] should be a checkbox in my mind