---
title: "How to Create a Music Bingo in Minutes"
date: 2019-09-05T15:39:37+02:00
tags: [Bingo, ]
draft: false 
---

I was recently asked to help organise a 'music bingo' for students of horseriding association
[BLOK](http://asrblok.com/english/). To be completely honest with you, I feel that bingo is
probably one of the most boring party games out there as the only 'skills' involved are paying attention
and bookkeeping.

*Music* bingo, however, puts a nice twist to the original game that makes it more
fun, exciting and skill-based. Music bingo is like regular bingo with some minor differences that
make it just so much more fun. The first difference is in the bingo cards: these consist of a grid
of cells like in regular bingo but each cell contains a song title instead of a number. Instead of drawing random
numbers from a tumbler, songs are played from a (randomized) playlist. If a song is played, it can be marked on the card and once a player has five marked cells in a row, they shout 'BINGO!' and collect their prize.

In this blog post I will describe how to organise a music bingo.  Some coding is required for now,
but I might come back to this fun topic and create some tooling for non-tech-savvy music bingo
enthusiasts. I might also delve a bit deeper into some mathematical properties of bingo (i.e.
combinatorics and probabilities of getting a bingo etc).

My preparations for a music bingo consist of the following ingredients:

* A great playlist in Spotify
* Printable bingo cards
* A list to keep track of songs played so far

I will describe how I got to these ingredients and then add some additional suggestions to make
your music bingo extra special.

# Creating the playlist
A fun evening of music bingo starts and ends with a great playlist. You can create a good music
bingo playlist by picking songs that most of your audience will know. You have to understand that
it's quite frustrating to get 'stuck' on a song you feel is impossible to guess. In the end, the
game of bingo is mostly about the element of luck, even if you are playing music bingo. As some of your audience members will surely not know some of the songs, it helps to select songs in which the title is clearly embedded in the lyrics.

Besides choosing relatively 'easy' songs, you could consider a particular theme for your music
bingo event. What constitutes a suitable theme depends strongly on your audience. Since recognizing the
songs is the biggest fun factor in music bingo, I would suggest taking well-known songs of some
bygone era. In my case, I was asked to create a music bingo night with a '90s theme. Perfect! If you are curious, you can find the list
[here](https://open.spotify.com/user/florisdenhengst/playlist/1RLqO7gwwsCBIvOT7hb8db?si=cwPzlyYtT--R7zfUKHLM8w).

Some additional hints regarding the playlist:

* Think about the length of the playlist up-front. The length of your playlist depends on two
  factors: total event time and playtime per song. I found that about 30 seconds playtime per song
  is suitable. This means that you'll have about 1 hour net playtime if you have 120 songs in your
  playlist. This is excluding time to verify bingos, introduce the game and prizes and breaks.
* make sure you deduplicate your playlist. There are online tools to do this for you, [Spotify
  Deduplicator](https://jmperezperez.com/spotify-dedup/) for example.
* you can decide to curate the order of the playlist yourself or randomize it. If you randomize
  it, I suggest storing the randomized playlist rather than playing the original playlist using 
  Spotify's shuffle option. Having a preset order makes for easy verification of bingos during the 
  event. You can randomize your spotify playlist using a tool such as [Spotify Playlist
  Randomizer](https://stevenaleong.com/tools/spotifyplaylistrandomizer).

Finally, create an export of your playlist so that you can easily generate bingo cards. Again,
many tools are available. I used [Exportify](https://github.com/watsonbox/exportify) to download
the randomized playlist.

# Printable bingo cards
After having created, randomized and exported the playlist, it's time to generate some cards.
I created a small python script to generate bingo cards in HTML. You can find the code on [Github](https://github.com/florisdenhengst/music-bingo). It's not great but it works.

In case you use my code, make sure to input the file using the following structure (tabs for
illustration purpose only):
```
playlist_order,     track_id,       track_name,     .....
             1,           32,    "Never Alone",     .....
             2,          104,     "What's Up?",     .....
```
The ``track_id`` column contains random numbers. This helps in verifying bingos during the event.

I added print-specific CSS styling to ensure that a single bingo card does not end up on two pages
in print. You can see how the bingo cards turn out
[here](http://htmlpreview.github.io/?https://raw.githubusercontent.com/florisdenhengst/music-bingo/master/cards.html).

# List all songs
During the event, many people will have a bingo at once. As you might not want to rely on your own
memory for verifying which songs have been played already, it helps to have a list available to
check off songs that have been played. You can simply create the export you have created before. I
added an extra column to keep track of songs played so far
```
playlist_order,     track_id,       track_name,     played?,    .....
             1,           32,    "Never Alone",           x,    .....
             2,          104,     "What's Up?",            ,    .....
```
Use this list in Excel or OpenOffice and you'll verify a bingo in no time. Use the auto-filter to quickly check whether the crossed of songs have actually been played.

That's it! You're all set to have a great bingo night.

# Get creative
You can get creative as well. Here are some ideas:

* Put the artist rather than song title on the card.
* If a song became well-known due to a movie, put the movie title on the card
* Put part of the lyrics on the card
* Mix it up and make cards with song titles, artist, album name, lyrics, movie titles etc.

# Things to consider
The success of the bingo night depends on a good preparation.
Here are some things to consider:

* How long are you gonna play the songs? I found that this depends per song: some are easily
  recognized while others are harder to guess or plain nice to sing along to. Overall, we played
  songs for about 30 seconds before skipping to the next song.
* Make sure you take enough time. As you need to play all songs for a while, you might not be able
  to play as many games as you would be used to per hour.
* Some songs start very slowly. Skipping ahead helps here.
* Make sure to introduce the rules upfront. Especially, think about whether the use of a
  smartphone is allowed. Players can easily cheat by using song recognition apps such as
  SoundHound.
* Allow the audience to verify a bingo together, by announcing the songs that contributed to the
  reported bingo. Do so for both proper and faulty bingos.

Finally and most importantly: don't forget to have fun :)
