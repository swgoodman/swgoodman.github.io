---
layout: post
title:      "In The Wav - Rails + JS"
date:       2018-10-23 04:09:59 +0000
permalink:  in_the_wav_-_rails_js
---




A few months ago I recieved a frustrating notification while using Spotify. I clicked "Save" on the Up Soundtrack (a great coding ambience), hoping to add it to my music library. The album was not saved and I received the below alert:

![](https://i.postimg.cc/s2txQNHG/Screen-Shot-2018-10-22-at-6-15-21-PM.png)


Mind you, I was not trying to download the album. I was trying to catalog, essentially, a link to the album in my Spotify "Albums" list. After some research I am not the first to run into the limit and Spotify has stated it is simply not affecting enough users to warrant their team fixing it right now.

This ceiling is incredibly frustrating for me because my favorite way to listen to music is to flip through my collection of albums, see the album art, think back on the memories associated with each, and land on what is fitting my mood. After reaching the limit I could no longer add to my collection and I was honestly saddened by it. 

So, instead of taking the time to split my collection into Apple Music or resort back to MP3s, I decided to use the new skills I've gained over the past 5 months and build myself a solution. 

So I built "In the Wav" using Rails and Javascript. ITW is a single-page web app built on Rails, but largely relying on Javascript to handle user interactions and display data. In addition, the app incorporates the Spotify API for user authorization and Album search. To use it, a user signs in with their Spotify Account and is greeted with a single page split into the three sections. The  left is the "Search" area, where users can search albums in the Spotify database by entering album titles and artists. When the user is ready to "Save" an album, they simply click "Add" and, through JS and AJAX, the album appears in their "Albums" section. From here, the user can decide to click "Listen", which opens the album in Spotify's in-browser player, or click "More info" and see the cover along with a few other facts about the album. All data is being presented and interacted with through Javascript and Ajax, while Active Record and Rails handles the instatiation and preservation of the data. 

This was a blast to build, because I had so much to gain from a working end product. I am very excited to have it working and to be able to "Save" albums to my heart's content. In the coming weeks I plan to make it look better and deploy it for others to use. 




