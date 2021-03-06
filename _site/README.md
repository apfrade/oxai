# OXAI website

Welcome to the repository for the website of the Oxford Artificial Intelligence Society

```
      ___           ___           ___                 
     /\  \         |\__\         /\  \          ___   
    /::\  \        |:|  |       /::\  \        /\  \  
   /:/\:\  \       |:|  |      /:/\:\  \       \:\  \ 
  /:/  \:\  \      |:|__|__   /::\~\:\  \      /::\__\
 /:/__/ \:\__\ ____/::::\__\ /:/\:\ \:\__\  __/:/\/__/
 \:\  \ /:/  / \::::/~~/~    \/__\:\/:/  / /\/:/  /   
  \:\  /:/  /   ~~|:|~~|          \::/  /  \::/__/    
   \:\/:/  /      |:|  |          /:/  /    \:\__\    
    \::/  /       |:|  |         /:/  /      \/__/    
     \/__/         \|__|         \/__/                
```

To edit the website you need a Github account and to join as a collaborator on this repository. Then you can follow the instructions below. If you know how to do pull requests, you can also do that.

## To add/edit Partners & Sponsors

Drag and drop an image into the folder `/img/partners/` or `/img/sponsors` (then press "Commit changes on the bottom).
Then add a new record by editing the file in the `/_data` folder. It is `/_data/partners.yml` for partners and `/_data/sponsors/[gold/silver/bronze].yml` for the three tiers of sponsorships. Look for the file, and click the edit button on the top right corner, which looks like

![edit button](/img/edit_button.png)

then add the field with the format like:

```yaml
- name: Herbertsmith Freehills
  url: https://www.herbertsmithfreehills.com/
  img: /img/sponsors/hsf.png
```

where the thing in `img` should point to the image file which you dropped in the `img` folder before. The press "Commit changes". And that's it.

## To add/edit team members

Edit the file `_data/team.yml`, and add or edit a record with the format:

```yaml
- name: Guillermo Valle
  picture: /img/people/guillermo.jpg
  role: Labs Technology Officer
  email: guillermo.valle@oxai.org
  linkedin: https://www.linkedin.com/in/guillefix/
  twitter: https://twitter.com/guillefix
  facebook: https://www.facebook.com/guillermovalleperez
```

Where the only compulsory fields are `name` and `role`. If you want to change the profile picture you should drop it in `/img/people/` and then update the field `picture` above. If you don't have a `picture` field, then the picture defaults to `/img/people/anonymous`.

## How to add a post to the blog

Open folder `/_posts/`. Click on the button "Create new file" on the top right. Name your file with a name like `2018-12-5-careers_tips_communication.md`, where the first bit should be the date of the post, and the next can be anything but use underscores "\_" instead of spaces. Then the content of the file can use [Markdown](https://daringfireball.net/projects/markdown/) syntax, to do things like include links, images (which you can put in the `/img/` folder), urls, etc. Markdown should be a pretty easy language to learn, as it's designed to be very minimal. If you want though you can use a markdown editor, of which there are many online (e.g. https://stackedit.io/app), which can give you a GUI to create markdown documents. It also supports HTML if you wanna include something fancy :D

```md
---
layout: post 
title: 'Tips for Securing Careers in AI: Communication'
author: Timothy Seabrook
email: firstname.lastname@oxai.org
---

Content of the blog post here blah blah

```

where you put the content instead of the "Content of the blog post here blah blah", you replace the field `title` with the title of the post, the field `author` with the author, and `email` with their email. The content of the post can use 

## To add events
Really we'll be using this if we are going to have "event posts", but for completeness: You can manually add events by editing `/_data/events.yml` for "current/future" events, or `/_data/pastevents.yml` for past events. Both will be shown in oxai.org/events. The format is

```yaml
 - title: Test event
   datetime: 2019-08-21
   day: 21
   month: Aug
   year: 2019
   time: 8:00 PM
   desc: This is a test event
```

<!--## Updating navigation bar
You can also add/edit fields in `/_data/navigation.yml` which will update the Links on the top navigation bar of the website (note that some links are fixed. Hmm, I need to fix that.)-->
