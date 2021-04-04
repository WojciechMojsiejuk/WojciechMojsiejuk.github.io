---
layout: page
title: Promenado
description: a location-based, puzzle mobile game
img: /assets/img/promenado/promenado.png
importance: 1
---


`Promenado` is my first individual project as a game developer on which, concurrently, I have based my Bachelor's thesis "Design and implementation of a puzzle video game".

The purpose of my engineering thesis was to create a mobile, location-based puzzle game focusing on a story of a young boy and his grandmother who together walk across the city of Bialystok to solve puzzles and unlock long-forgotten memories.

The game is targeted at younger players, elderly, families and tourists.

The game offers a dozen different puzzles, challenging various players' abilities. Through those puzzles players may learn basics of Esperanto, learn about forgotten places and people who lived in Bialystok, get to know interesting facts, discover incredible paintings, music and other elements of the cultural heritage of the city.

The game can be treated as an off-the-beaten-track guide around Bialystok. It does not require nor endorse one specific way to finish the game. The pace and the chronology of visited points are up to the player.

The game was written in `C#` using the `Unity` game engine. The game uses `Yarn Spinner` dialogue system and geographic information system provided by `Mapbox SDK for Unity`.

***

UI
---

***
<div class="row">
    <div class="col-sm">
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/promenado/album.png' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm">
    </div>
</div>
<div class="caption">
    Skeuomorphic design of level selection menu (trying to imitate the old photo album).
</div>


***

Cutscenes
---------

***

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/promenado/cutscene_1.png' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/promenado/cutscene_2.png' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/promenado/cutscene_3.png' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    For cutscene purpose I have used vector graphics. 
</div>


***

Puzzles
-------

***

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/promenado/puzzle_1.png' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/promenado/puzzle_2.png' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/promenado/puzzle_3.png' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    Exemplary puzzles used in game.
</div>


***

Trailer
-------

***

Here you can watch a trailer of [my game][youtube].

[youtube]: https://youtu.be/qKgeuKdBtoE


***

Game & Requirements
-------------------

If you want to play the first released version of my game you can download it on my [itch.io site][itchio] (if there is a password, type game title in lowercase). Sadly, there is no localisation yet in this version, so all of the dialogues are in Polish 😔.

Current requirements:

* Android 7.1 or higher;
* 200 MB of free space;
* Game uses GPS in "GPS mode". This mode requires you to be in the Bialystok to fully experience the game. You can choose 
"no GPS mode" otherwise, however game is limited to puzzle-solving elements. 

[itchio]: https://hirohideyoshi.itch.io/promenado



***