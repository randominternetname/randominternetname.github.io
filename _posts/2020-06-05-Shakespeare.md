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

These character lists were useful in guiding assigning roles by hand at the beginning of each reading, but do not automate the process as much as I would like.

## Second Iteration

Using the dictionary of non-interacting characters I created in my first iteration of the project, I needed to figure out a way to find the intersections between the lists.  For a simplified example, we'll say that there are only three scenes and four characters.  Scene 1 has Phebe and Jaques, Scene 2 Jaques and Roselind, Scene 3 Roselind and Celia.

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

You'll notice that each actor could play only one of the two other characters in their "Can Also Play" list, but not both, since those characters interact.  Also, once a character has been assigned, it is no longer available to be assigned to another actor.  In the above table, Phebe can play Roselind, but cannot play Jacques from Phebe's list.  

I created an empty list for the first character in my dictionary and appended the intersection of that character's list and the character list of the first character they can play:

>If Matt can play Bob, Mary, Helen, and Jane \n
and Bob can play Helen and Jane \n
and Helen can play Bob, Joe, Jasper, and Jane \n
then Matt can play Bob, Helen, and Jane (without talking to themselves at any point).

To loop through the next available character, Mary, first I needed to remove all of the previously assigned characters from the working copy of the full player list and the working copy of the dictionary of the character's lists of characters (as well as any key/value pairs with empty values.

In this iteration, I coded it really inefficiently and made it way too labor intensive.  As-is, the code requires that I run through each character one by one to determine the length of their lists to avoid index errors.  Since dictionaries do not maintain a static order, it also only works once.  This is even less than ideal because I found a flaw on the second to last character, which, forgetting about how dictionaries work, I attempted to fix and rerun part of what I had written.  Thus, ruining everything I had done up to that point, just in time for meeting up with my friends to assign roles.

##  Third (Final?!?) Iteration - In Progress

Rather than copying and pasting the list intersection code for each level of each character's lists interactions, I need to create a function which will loop through until it hits the end of the available characters.  I should be able to adapt the current code to also loop through and create all the actor's lists in one fell swoop.  Once I have this written up, it will be useable across all of the plays.

### Tools
* pandas
* re
* numpy
* pickle
* defaultdict from collections



[^fn-sets_explanation]: Sets are lists which keep only unique items.