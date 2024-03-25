---
description: "{{VALUE:Scope of the project}}"
created: "{{DATE:gggg-MM-DD}}"
status: New
complete: ❌
project: <% tp.file.title %>
project_type: "{{VALUE:Project type?,personal,okr,work,writing}}"
owner: "[[Johnny Bananas]]"
goal: "{{VALUE: Link to Goal}}"
---
# [[02 Projects|Project]] - <% tp.file.title %>

{{VALUE:Tags? #writing #work #personal #travel #okr}} #project 

> [!todo] To-do
>```tasks
not done
path includes <% tp.file.title %>
## Notes

## Tasks

<%* if (tp.file.tags.contains("#work")) { %>
## People

<%* } else { %><%* } _%>

<%* if (tp.file.tags.contains("#writing")) { %>
## Planning
- [ ] Create Longform Project for the novel
	- [ ] Create folders for Drafts and link to Scene Template
	- [ ] Create folder for Characters and link to Character template
- [ ] Create a high level outline using [[Plot Groundwork]]
- [ ] Basic character details using [[Character Groundwork]]
- [ ] Complete several levels of [[World Building Groundwork]]
- [ ] Review tips in [[Best Advice From Authors]]

## Drafting
- [ ] Complete first draft
	- [ ] Write 2,000 words a day ⏫ 🔁 every day
	- [ ] Update Revision Tracker 🔁 every day 

## Revising
- [ ] Complete First Revision

## Editing
- [ ] Complete self-edits
	- [ ] Remove passive voice
- [ ] (Optional) Work with a critique partner and/or beta readers
- [ ] Work with a professional editor

## Budgeting
- [ ] Editor or multiple editors
- [ ] Cover designer
- [ ] Book Formatter / Software
- [ ] Book swag (Bookmarks, posters, postcards)

## Marketing
- [ ] Decide on a marketing budget
- [ ] Decide which marketing strategies you will use
	- [ ] Advance reader copies
	- [ ] Pre-order campaign
	- [ ] Giveaway
	- [ ] Cover reveal
	- [ ] Price promotion/loss leader
	- [ ] Paid advertising
- [ ] Build your marketing plan, including the strategies you will use

## Designing
- [ ] Building the book
	- [ ] Choose a title
	- [ ] Choose a subtitle
	- [ ] Choose a series title
	- [ ] Finalize tagline
	- [ ] Finalize back blurb
- [ ] Create the frontmatter
	- [ ] Title page
	- [ ] Copyright page
	- [ ] Dedication
	- [ ] Table of Contents
	- [ ] "Also By" page
	- [ ] "Call to Action" page (newsletter signup, etc)
- [ ] Create the backmatter
	- [ ] Acknowledgements
	- [ ] "About the Author" page
- [ ] Cover Art
	- [ ] Research covers in your genre

## Formatting
- [ ] Choose your formatting method (hire, software, or DIY)
- [ ] Finalize your interior styles
	- [ ] Fonts
	- [ ] Line spacing
	- [ ] Justified text
	- [ ] Page breaks
	- [ ] Page numbers
	- [ ] Chapter headers
	- [ ] Chapter beginnings (drop caps, phrase caps)
	- [ ] Images
- [ ] Format your frontmatter
- [ ] Format your backmatter
- [ ] Create your final, formatted files for each format
	- [ ] eBook
	- [ ] Paperback
	- [ ] Hardcover

## Prepare for Publishing
- [ ] Select your publishing formats
- [ ] Determine which formats you will publish in, and on which platforms
	- [ ] eBook
	- [ ] Paperback
	- [ ] Hardback
- [ ] Choose your release date
- [ ] If you decide to do pre-orders, choose a date
- [ ] Finalize the pricing for each format
- [ ] Get your ISBNs (one for each format)
- [ ] Determine your keywords
- [ ] Determine your categories

## Publishing
- [ ] Set up your accounts on your chosen publishing platforms
- [ ] Upload your book metadata, content, cover, and other required details
- [ ] Review the proof version of each format
- [ ] Approve the proof version(s)
- [ ] Submit the book for approval
- [ ] Congrats!  You're a published author!

<%* } else { %><%* } _%>

<%* if (tp.file.tags.contains("#travel")) { %>

> [!warning] Expenses
> ```dataview
TABLE
project AS "Project",
amount AS "Amount",
submitted AS "Submitted?"
FROM "00 Meta/02 Action/06 Expenses"
WHERE project = "<% tp.file.title %>"
SORT file.name DESC

<%* } else { %><%* } _%>

## Meetings

> [!abstract] Meetings
> ```dataview
TABLE
project AS "Project",
duration AS "Duration",
summary AS "Summary"
FROM "00 Meta/02 Action/05 Meetings"
WHERE project = "<% tp.file.title %>"
SORT file.name DESC

