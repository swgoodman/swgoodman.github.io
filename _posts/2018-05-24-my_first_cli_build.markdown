---
layout: post
title:      "My first CLI build."
date:       2018-05-24 20:10:12 -0400
permalink:  my_first_cli_build
---


![](https://upload.wikimedia.org/wikipedia/en/7/76/Pitchfork_logo.svg)

Like a toddler taking his first step, I just created a basic CLI application to help music fans more easily access the latest reviews by Pitchfork.com. My very first software application.

Upon running the application the user is greeted with:

```
--------------------------------------------------
Pitchfork.com | 'The most trusted voice in music.'
--------------------------------------------------
                       
Find the latest reviews from Pitchfork.com below:
                       
+----+----------------------------------------+
| 1. | 'Double Dream of Spring' by Deerhunter |
| 2. | 'Love Yourself Tear' by BTS            |
| 3. | 'Light of Mine' by KYLE                |
| 4. | 'Steamroom 40' by Jim ORourke          |
+----+----------------------------------------+
                       
Enter the number of an album to see more info or 'exit':
```
The user then inputs which review they would like to investigate and receives the following information:

```
--------------------------------------------
'Steamroom 40' by Jim ORourke
Genre: Experimental
--------------------------------------------
                       
Score: 8.0
                       
Review by Philip Sherburne
                       
The 40th installment of the prolific producer and composers Steamroom series is a highlight, one long, meditative piece of synth overtones, slowly rising arpeggios, and pure drift.Most of Jim ORourkes music is not made for you or me. Some of it is: the Wilco and Sonic Youth records hes played on or produced were certainly meant to have an audience. His collaborative outputscores of releases, many improvised, alongside players like Oren Ambarchi, Keiji Haino, Fenneszis part of a greater conversation encompassing both players and listeners. And his rock albums for Drag City, a loose series stretching from 1997s Bad Timing through 2015s Simple Songs: No matter what the Chicago native, long a resident of Japan, may say, those are surely meant for ears beyond his own. Theyre too meticulousand too joyousnot to be. But then there are the Steamroom releases, and those truly are a private, paging-through-his-journals affair. Not because theyre particularly unguarded or revealing its simply that he would be making those recordings whether anybody listened or not. I just have to make them, he told Bandcamp, the artist-to-fan retail platform where he hosts the series. Its like my oxygen.Named after his studio, the Steamroom series amounts to a curated archive of his daily practice. Since 2013, when the series launched, it has included reissued early work, film soundtracks, and tour-only releases, but the bulk of it comprises previously unreleased recordings made in his Tokyo workspace. ORourke spends a good chunk of his day holed up with a Serge synthesizer and a drawer full of field recordings, massaging sounds into a shape that feels right to him. Its less about composition or songwritingtheres nothing approaching a song on these albumsand more like painting or throwing pots, only with duration itself in place of pigment or clay. I like longform music that isnt necessarily about structure, he says. Its just a long period of something happening. The Steamroom releases amount to a kind sculpted air.For the most part, that means drones. Steamroom 20s Silent Night is an inky hour colored the semi-matte black of a fogged-up window on a moonless night. Steamroom 27s Long Night Part One, 47 minutes long, brandishes tight clusters of needling tones that feel like theyre trying to crowd their way into your ear canal. Not all the material is so shapeless Steamroom 29s from here to there sets playful, almost circus-like synth chords against insect chirps and shortwave chatter. Whether sinister or bucolic, what all the releases share in common is an almost total absence of discernable structure in favor of pure drift.But if the austerity of many Steamroom releases means theyre likely to appeal mainly to confirmed fans of dark ambient music, Steamroom 40 stands out, even though it clearly occupies the same continuum as its predecessors. For one thing, as drones go, it captures a brighter, airier mood, and its consonant tonal field is instantly recognizable. Plenty of this kind of music can sound largely interchangeable even to its fans, but Steamroom 40s lone, 41-minute track, Improper Release, cant easily be mistaken for anything else in the seriesor anyone elses work, either. Its gentleness is reminiscent of Kevin Drumms 2009 album Imperial Horizon, but ORourkes materials are less muted, more clear-cut. Its hard to say how he made it, but it feels like all the notes in a major scale are fading softly and perhaps randomly in and out of earshot, overlapping in such a way that creates a perpetually shifting moir of cottony harmonies.The bulk of its frequencies occupy a moderate range, smack in the center of the spectrumyou imagine a cat curled up in the middle of the keyboardand slowly cycling arpeggios gradually conduct the energy upward in waves. Theres almost no dissonance the rare off note flashes like a blade of grass showing its underside before the wind whips it around again. Its easily among the most placid, peaceful music ORourke has ever madeperhaps the only thing in Steamrooms catalog you could conceivably call pretty.But despite its outward simplicity, theres more going on here than meets the ear: frequencies cascading just out of earshot, microtones extending like a hall of mirrors. Funny things start to happen the longer you listen you may begin hearing melodies that arent there. I tend to hear echoes of New Orders Procession, which shares its key, and its palette of smeared analog synthesizers, with ORourkes piece. And if you listen loud and on good speakers, the occasional rumble of bass will feel like theres a truck idling outside your house. This is not music for laptop speakers or lossy compression. ORourke entreats his fans to download his music in the best possible quality, and like everything in the series, Steamroom 40 both wants and deserves a high-fidelity experience. Thats not just an issue of audio fetishism its almost a philosophical question. This is music that proceeds according to its own logic and its own time scale, music that offers a stern rebuke to the anthropocentrism of the old tree-falling-in-a-forest maxim. Whether or not theres anyone there to hear it is irrelevant, this music seems to say. The sound itself is self-sufficient, self-sustaining, and maybe even self-aware. It does not need us, which makes us all the luckier to have it.

                       
Type 'list' to choose another or 'exit'.
```
The app is simple, but hey, we all have to start somewhere. 

I started building it by referencing resources on Learn.co. Everything went pretty smoothly as I followed along with Avi and googled issues as they came up. But, then I hit a wall.

Scraping.

Fashioning a functioning scraper took up most of my time when creating this app. It is the reason I had to switch the basic functionality of my app. I inititally wanted to return the top albums of Pitchfork's "Best of the Year Lists", but the years' CSS  were all labeled differently and it simply was not worth my time to build individual scraping methods for each list.

So I pivoted. After I redirected my efforts to scraping the latest reviews it was smooth sailing and it felt great to finish my first project of the course. I'm looking forward to the project review with a technical coach and getting feedback on how I can make my code more efficient. 
