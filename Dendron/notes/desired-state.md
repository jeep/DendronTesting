---
id: 5whbl1or5si0kn3sul5vvpg
title: Desired State
desc: ''
updated: 1664156351661
created: 1663433606814
---

# Requirements
1. Separation of work stuff which cannot be committed externally and personal stuff which I don't want embedded in my work notes for privacy reasons
1. Able to see interactions with people (expect backlinks with a person note)
1. Easy use of project vaults to segregrate knowledge from project work
1. Daily notes captured easily and then reorganized as desired (leaving links in daily)
1. Before I can migrate the following must be resolved or have a workaround:
    * https://github.com/dendronhq/dendron/issues/3548
    * https://github.com/dendronhq/dendron/issues/3546
    * https://github.com/dendronhq/dendron/issues/3547
    * (possibly) https://github.com/dendronhq/dendron/issues/3549

# Work Computer
1. [[Work workspace|dendron://Dendron/desired-state#work-workspace]]
1. [[Personal workspace|dendron://Dendron/desired-state#personal-workspace]]
# Home Computer
1. [[Personal workspace|dendron://Dendron/desired-state#personal-workspace]]
# Workspaces

## Work workspace 

* Peacock to have special color to indicate "do not push to remote" and not safe for personal info - probably a dark maroon
1. [[Worknotes vault | #worknotes-vault]] - Workspace root
1. [[Reference Vault|desired-state#reference-vault]] - remote vault 
1. [[People Vault | #people-vault]] - remote vault

## Personal workspace

* Peacock to have special color to indicate safe to push and safe for personal information, no work details - probably a dark green
* Bare native workspace
1. [[HomeNotes vault | #homenotes-vault]] - remote vault
1. [[Reference Vault|desired-state#reference-vault]] - remote vault
1. [[People Vault | #people-vault]] - remote vault
1. [[HomeProject vault 1 | #homeproject-vaults]] (1 - 3 of these) - remote vault

## Vaults

### WorkNotes vault 
 `Local git repo`

* daily
    - journal - What else do people put in daily? Should I just eliminate "journal" or or possibly "daily?"
        * `<date>`
* `company_name` - reference notes for work specific stuff, I thought about just reference, but I want a clear separation from the common reference vault. 
* meetings - m.*
    - `<meeting name>`
        + ARs - for tracked action items
        + Charter  - for meetings I run
            ~~~
            Statement of purpose
            What constitutes quorum (required attendees, etc)
            Standing agenda
            Sunset criteria
            ~~~

        + Horizon Agenda - for meetings I run
        + `<date>` - for minutes or notes
            

* projects - p.*
    - small - 1-5 task projects that don't warrante their own file
    - `<project name>`
        - Todos
        - `<reference material>`

    - archive.*
* todo

### Reference Vault 

 `Sync'd to github`

 `migrate org notes to this structure`

* technology
    - software 
      + `<language>`
      + `<topic>`
      + `<program>`
    - hardware
      + `<component>`
        + `<proxy link to datasheetA`
        + `<proxy link to adafruit learning topic for Adafruit products>
    - `<topic>`
* games
    - `<game name>`
        - `<proxy note to rules>`
        - `<proxy note to FAQ>`
        - `<proxy note to BGG entry>`
* literature
    - `<title>`
* martial-arts
    - kenpo
    - escrima
    - kobudo
    - `<concept>`
* probably other types of notes I have...

### People Vault 

 `Sync'd to github`

 `primarily used for backlinks`

    - `<firstname.lastname>
 

### HomeNotes vault

* Sync with github
* projects - p.*
    + small
    + `<project name>`
        - `<subproject, if needed>`
* daily
    - journal
        - `<date>`
* todo
 

### HomeProject vaults

* Likely to be 3 of them at a time
* Mostly for things that I want to keep a separate knowledgebase for
* ex. Active books/stories that I'm writing


[[open-questions]]
