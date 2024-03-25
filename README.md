# lh-obsidian-templates
A collection of leethobbit's templates, Canvas dashboards, or other useful things I've created for Obsidian.

## How to use
Each folder in this repository will contain a selection of files needed to re-create some part of my vault. I've spent a lot of time in Obsidian creating nice dashboards, templates, and other things, and would like to share that work!  Most of these will require some level of work to get them fully functional, but I'll try to list out all of the steps that need to be taken for each one.

## Some Highlights
- Callout blocks wrapping Dataview and Task queries - I recently changed up a lot of my queries so that they are wrapped in Callout blocks.  You may or may not like this, but I do - it has improved visibility for me on pages with lots of information.
- Dynamic linking in templates - Not sure if that is the correct term, but I use a lot of dynamic linking in my templates. For example, in [Project Template](QuickAdd%20Templates/Project%20Template.md) you'll see that the tables are automatically set up to track the file after it is named - thank you to Templater for that!

### Day Trading (Stock trading profit tracker)
Within this folder are three files:

- **Daily Template.md**: Daily Note template
- **Trading Overview.canvas**: The Canvas dashboard I use for tracking my profit and loss.
- **P&L Dashboard.md** The individual "widgets" that are on the dashboard.  

When I create a big Canvas dashboard, I like to be able to link in tables, graphs, and more - this often involves building out said features on another note and then using ![[filename#subheading]] to link that specific feature into the table.

Because of this, you'll need to go into the "P&L Dashboard" file and update the folder attribute of the graphs to point to where your daily notes are stored. You may also need to update the links in the Trading Overview Canvas itself - hopefully what I'm sharing here is enough to understand what needs done.

### QuickAdd Templates
TODO: Incorporate more use of the Buttons plugin to replace doing QuickAdd command hotkeys.

I make heavy use of the power of Templater + QuickAdd, so in this folder are some of the more interesting templates I've created that use them. Any time you see {{VALUE:something here}} that is a QuickAdd variable that will trigger a prompt if you set up a QuickAdd template macro for that template.

A few notes about things I really like:

- **Project Template.md**: This has evolved quite a bit over the years and currently does not feature too much work related stuff - back when I did use it for work, I just had more of those "if/else" blocks checking for different work tags so each project would have a relevant starting point.
- **Meeting Template.md**: This is designed to work with the Project template - the Project template has a table that searches for all Meeting notes in a specific folder, and lists the ones where their project property in those Meeting notes is equal to the name of the Project.

### Writing Templates
A few additional writing templates for creating scenes and characters.  I don't write a lot so these could be much better.

## Final Thoughts
I've been using Obsidian for a few years, which means I've definitely fallen into some habits along the way.  If you see things in this repo, and you think "Why doesn't he use X?" or "Why does he do it like Y?" - please tell me about it! I don't go out of my way to find new plugins or tricks like I used to, but I'm always interested in doing things the smartest way possible!
