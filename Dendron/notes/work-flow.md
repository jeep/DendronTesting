---
id: jo1gckv9rs978h7au6q29f5
title: Work Flow
desc: ''
updated: 1664740506719
created: 1664738568184
---
# Mapping how I used to work to how I will work
+ I'm moving from Org-Roam to Dendron and I had a system that I liked pretty well. Unfortunately, emacs on Windows is not working for me when I'm forced onto a Win10 system. I've been playing with emacs on Win11 using WSL and it seems great. Unfortunately, I don't have that option at the office.
+ This is kind of a mix of bullet journaling and GTD that has been adapted to digital. Which, I know, going digital is amost antithetical to those two processes which are explicitly analog systems.
## Planning
* I organize my projects in a very GTD manner
* I would call up org-agenda, which would give me a list of all the items with dates associated with them which is 1 week from now or earlier and all things with special TODO keywords. (ACTV, NEXT, TODO, WAIT)
* The format for the lines below is `<filename>: <state> <action>   :<tags>`

~~~
Day-agenda (W39):
Sunday  2 October 2022
    Home Maintenance: Winter 2022-2023 [0/4][0%]

<if I had anything overdue, it would show up here>
=================================================
INTR
  <a list of items with the INTR state, if any>

IN PROGRESS/ACTIVE
  <a list of items with the ACTV state, obviously I did this one, but didn't move it to done>
  Figure out how to work with Dendron:ACTV Install Dendron               :Project:home:Dendron

NEXT
  <a list of items with NEXT state>
  turn the game room into a gym: NEXT: Electrical          :Project
  turn the gym into a game room: NEXT: Organize shelves       :Project
  small-projects: NEXT Box wrap         :Project
  small-projects: NEXT Pick colors for army     :Project 

TODO WITHOUT PROJECT
  <as above, but for tasks not in project files>
  2022-09-14: TODO process this page (2022-09-04)
  2022-09-14: TODO set up 1:1 with Person1
  2022-09-14: TODO ....

PROJECTS
  <a list of items with the project tag, mostly these will be file names and lines in the small-projects file>

WAITING
  <a list of items with the WAIT tag>

TODO
  <a list of every item marked with a TODO tag, will include the items not in a project. This is just a place for me to scan to ensure nothing is missed>
~~~

* I would then go into any projects that I didn't see next actions for and set the next action (sometimes I was stuck and didn't want to get bogged down, so I'd put something like NEXT Review this project)
* With Dendron, I believe I lose the ability to handle dated things, but I didn't really use that except for recurring things anyway.
* The auto consolidation of tasks will likely be with TODO Tree. But there is a lot more research I need to do with this. This should be the very next thing I look at
* I then look at my calendar for upcoming meetings and create todo items if there is any preparation I need to do that I haven't already logged (which is almost never) and set anything I've been slacking but need to get done to NEXT
* I'll create "events" in my log for things that I know are coming up. In Dendron, I'll be using `- o` since I set up the syntax highlighting for that. 
## Capture
+ Capture is where I'm mostly inspired by BuJo
+ I capture all my notes linearly rapid log style in a single note for the day unless there is something special like a conference. In which case, I'll capture conference notes in a separate note and just link to it in my daily. I usually process those as a whole
+ Every morning, I open a new daily log file
+ It comes pregenerated with `- [ ] Process this note` With dendron, I can either do that (but I think it needs to be "TODO") or add a tag "needs processing"
+ The first thing that goes into the daily are events for the day, but other than the process task and these it will be completely empty. (When an event happens I pull it from the top to the current location and put notes under it.)
+ I then process the previous day's log- usually there are only 1-2 items left. And complete the task. (This automatically copies the task as completed to today's daily, which I don't really care about)
+ If I am working on a project, I'll sometimes take notes directly in that project file, but usually I don't bother. I take them in the daily and then move them. It's really only if I am doing heavy design work that I'll use the separate project note.
+ If I move a task to any completed state, a copy of that item will automatically be put at the bottom of my daily log
+ At the end of the day I try to process my notes so that the morning processing of the log is just moving a couple things around
+ Capturing in Org was pretty easy as I just needed to use stars to give an outline structure to the captures. 
+ Figuring out how I want to do it with md will likely be immediately after TODO Tree
+ For now, I'm just doing unordered lists which can go up to 6 levels of hierarchy. I started out trying to use headings and it kind of sucked. I cycle through using * + - in that order twice to help me see structure when not using the preview
## Processing captured stuff
+ Ideally, this would be a "daily reflection" but usually I don't actually "reflect" on the day and sometimes I process notes other than my daily log
+ I go bullet by bullet through my log (or the file being processed) and based on the type of item it is, process it like so:
### EVENT
+ Something that happened. I just leave these in the log, but if it might happen again, I create a slip for it so I see dates in the backlinks.
+ With "candidate backlinks" being experimental and not great, I need to be more diligent about creating notes for each of these, I think.
+ When I create a note for an event, I look at the unreferenced backlinks and usually turn them into hard links to gain the performance benefit
### TASK (includes waiting)
+ Some action I need to take (variously called ARs, NAs, and TODOs)
+ These automatically get displayed on my agenda page
+ If this is project related, I'll move it to the relevant project page and change it to MIGR in the daily page (i.e. migrated, so it won't show up in my agenda view)
+ This is the one area I'm most concerned that Dendron will fall over for me. I'm hoping that TODO Tree handles this for me.
+ Current thought is that I'll set up TODO Tree similar to how I have Org set up though I don't think it handles the checkbox sequence
```elisp
  (setq org-todo-keywords
        '((sequence "TODO(t)" "NEXT(n)" "ACTV(a)" "|" "DONE(d!)")
          (sequence "INTR(x)" "HOLD(h@/!)" "WAIT(w@/!)" "MIGR(m)" "|" "CNCL(c!)")
          (sequence "PROJ(p)" "INCU(i)" "|" "ARCH(z)")
          (sequence "[ ](T)" "[-](S)" "[?](W)" "|" "[X](D)")
         )
```
### LOG Content
+ Just a record that I did a thing or had a thought. 
+ When I file things from my journal, I expect the link to remain in my daily log. In org-roam any time I moved an item to the DONE state a copy of the item would be put in my daily page. I found that extremely handy when I was doing weekly/monthly reviews.
+ I don't think that the auto copy when something moves to done will work, so I might need to adapt to moving TODO items to the day I expect to work on them and then migrating them as I did when using paper bujo.
### Idle Thought
+ Some thought that I need to mull over.
+ Occasionally, I'll create a separate note for it. I used to rely on the "unreferenced links" in org-roam to find these. 
+ These generally don't fit some nice hierarchy because they are just idle thoughts. I may need to just create a hierarchy for "thoughts" and use that to file these. Or is that what "scratch" is for?
### Reference material 
+ Information that I'll possibly refer to in the future. These will get filed based on their category. I used to create category "spreads" where I collected refrences to something. In Dendron, I will file these in the correct tree and, if necessary, link to it from other trees where it's related or possible use tags. That should replace the need to keep what I used to call "topic spreads"
+ I will likely struggle with the hierarchy. Some things don't nicely fit. Or fit in multiple places. That's one thing about zettelkastin, it eliminates that burden
+ I'll likely fall into a habit of putting things in misc. I hope that I can just file things and "discover" the hierarchy that works for me
+ I may need to get used to occasionally processing misc
### Meeting notes 
+ Contain my personal notes on a meeting I attend. Tend to be informal. Can contain any of the above types of items which I pull out and link.
+ Will pull these out to meet.meeting-name.iso-week leaving a (note reference)[https://wiki.dendron.so/notes/f1af56bb-db27-47ae-8406-61a98de6c78c/]
### Meeting minutes 
+ These contain notes from a meeting I run. List all decisions made, action required by anyone, attendees, invitees, etc. If there is an easy way, I wouldn't mind attaching the attendance files that MS Teams generates.
+ I expect meetings to have the structure: (pretty sure I wrote this already)
    + meeting-name
        - ARs
        - Charter
            ~~~
            Purpose
            Quorum requirements
            Standing Agenda Items
            Sunset Criteria
            ~~~
        - Horizon Agenda
        - iso-week (for notes for that day)
## Reflections
+ The daily processing is a type of reflection, but this is talking about a larger scale. Weekly, Quarterly, and long term
### Weekly Reflection
+ I'm bad at weekly reflections but want to get better at doing them
+ Review the week to see what I've done and what still needs to be done. Look at the calendar
+ Write down thoughts on the week, what went well, what would I like to do better, what small thing can I change to improve. Did I accomplish what I had hoped to in the previous week? What do I want to accomplish in the next week?
+ Review non-project tasks- do any need to move to CNCL?
+ Review WAIT items- do I need to do anything to free it up?
### Quarterly Reflection
+ Review weekly reflections, if they exist
+ Score my work OKRs
+ Reflect on progress towards my personal goals
+ Write down thoughts on the quarter, what went well, what would I like to do better, what would I like to change to get better? 
+ Write down work OKRs
+ Write down personal goals
+ Review projects - do any need to be eliminated (move back to INCU or ARCH?) Do any need actions promoted to NEXT? 
+ Have all the new projects that have come up been groomed properly? If no, groom or create tasks to groom
### Annual Reflection
+ Review quarterly reflections
+ Think about my life in general. Have my goals changed? Review financials.