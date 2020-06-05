---
layout: post
title: Reading Shakespeare
---
## The Problem

For the past several weeks, my friends and I have been reading Shakespeare plays on Twitch every Friday evening. It is a really low key endeavor and people drop in and out as they are available. There are often two dozen or more characters in each play to be divided among six to ten readers. Before each session, we spend about half an hour assigning roles, with a goal of preventing anyone from playing two characters who interact.

## Finding the Data

My group uses [OpenSourceShakespeare](https://www.opensourceshakespeare.org/views/plays/playmenu.php?WorkID=asyoulikeit) and my first inclination was to scrape the site to capture the information I needed. But, the format of the website does not lend itself well to easy scraping.

Luckily, the full text of all Shakespeare's plays were available through kaggle, [here.](https://www.kaggle.com/kingburrito666/shakespeare-plays)

## First Iteration

I downloaded the csv and created a pandas dataframe. The first play I am scripting for is *As You Like It*. So, I copied only those lines from *As You Like It* into a new dataframe. From there, I captured the list of all the characters in the play.  Then, I wrote a for loop to make sets[^fn-sets_explanation] of the characters in each scene. Using a default dictionary and some for loops, I made lists for each character which contained those characters with whom they did not share any scenes.

These character lists were useful in guiding assigining roles by hand at the beginning of each reading, but do not automate the process as much as I would like.

## Second Iteration

Using the dictionary of non-interacting characters I created in my first iteration of the project, I needed to figure out a way to find the unions between the lists.  For a simplified example, we'll say that there are only three scenes and four characters.  Scene 1 has Phebe and Jaques, Scene 2 Jaques and Roselind, Scene 3 Roselind and Celia.

<table>
  <thead>
    <tr>
      <th>An Actor Playing</th>
      <th>Can Also Play</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Phebe</td>
      <td>Roselind, Celia</td>
    </tr>
    <tr>
      <td>Jaques</td>
      <td>Roselind, Celia</td>
    </tr>
    <tr>
      <td>Roselind</td>
      <td>Phebe, Jaques</td>
    </tr>
    <tr>
      <td>Celia</td>
      <td>Phebe, Jaques</td>
    </tr>
  </tbody>
</table>

You'll notice that each actor could play only one of the two other characters in their "Can Also Play" list, but not both, since those characters interact.  Also, once a character has been assigned, it is no longer available to be assigned to another actor.

[^fn-sets_explanation]: Sets are lists which keep only unique items. (Click the return link to go back.)