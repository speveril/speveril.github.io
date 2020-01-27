---
title: Making Engines
layout: post
tags: gruedorf
---

Gruedorf progress:

*Technically this is stuff I've done over the last few weeks, not just the last week, but a bunch of it was done in the last week. I'm establishing a baseline here.*

- Finished up a Godot-based prototype RPG that I started a couple weeks ago. It's got...
    - standard jRPG-style movement, including proper obstruction handling
    - walk-on events and button-triggered events
    - asynchronous/re-entrant cutscenes
- Got a start on a VN/point-and-click game prototype in Godot. It's got...
    - speaker portraits
    - asynchronous cutscene handling
    - background image switching

---

## Cozy Engine

Cozy Engine is a web-technology-based game engine that I started working on in 2015. Originally, it was called Egg, but I eventually renamed it because I discovered an existing game engine using the name, and because I liked "Cozy" better anyway.

It's my latest iteration of building a general 2d game engine, which I feel like I've been doing pretty constantly, under various names, for most of my adult life. Settling on web technologies was a way to make it familiar and quick for me to work on, since I've been primarily a web developer for my entire professional career so far. Earlier attempts had been built in C++, with embedded VMs like Lua, LLVM, or V8; I believe I started at least one attempt with Monogame or XNA, and there was definitely one shot at building it as a collection of scripts in Unity. I've looked into graphics libraries in Python and Ruby, and various so on.

I keep doing it because every time I try out a game engine, I kind of hate it. "Hate" is a strong word, I suppose. I invariably run into some eccentricity in the architecture, or something in the language, or something about its performance, or whatever other thing bothers me t the time, that makes me disenchanted with sticking with it for long enough to make an entire game.

So, of course the obvious solution is to build my own.

I've released it under an open source MIT license, and it's available on github at https://github.com/speveril/cozy. I also built a page for it at https://cozyengine.com/. Its icon is a cute cat. I even built a (small) complete game with it, [SimpleQuest](https://speveril.itch.io/simplequest).

It does a few things that I still think are interesting and novel, but my interest in continuing the project is, admittedly, waning. It represents a lot of work, and it clearly works to make a video game. I'm less convinced though, now that I've done it, that it was worth my time to spend years building an engine to my specifications, rather than learning to live with engines that other people are already working on.

## Living With Someone Else's Decisions

I wasn't always this way. Back at the tender age of 14, when I was apparently much wiser, I discovered a game engine called [Verge](https://verge-rpg.com/). I didn't really know much beyond the basics of how to build a simple text-based game, but I had wanted to make them basically since I was old enough to play them. While I'd learned bits and pieces of programming up to that point (mostly various flavours of Basic, a tiny bit of C, and a little bit of [MicroMUSE](https://en.wikipedia.org/wiki/MicroMUSE) scripting), Verge let me put graphics on the screen and move them around so much more easily than anything I'd worked with before. It let you make maps with layers, and animated sprites. It was very exciting!

So exciting that I eventually learned how to use Verge quite well. I didn't manage to ship anything to anyone else until years later, but I got pretty familiar with it. By the time the third iteration of Verge (aptly named Verge3) rolled around, I was ready to actually start making things. Over time, thanks especially to some "Hours of Verge" competitions (think early game-jams), I got quite comfortable and fast while working within its constraints.

Its constraints were pretty... constraining. Its built-in language, a straightforward C derivative, had bugs, and design decisions driven by what was easiest to implement. It had hard-coded limits to the number of sprites you could use at once. It was a lot of fun, and the community was vibrant, though, and that was enough for me, at the time. I made multiple starts on a Big Game.

## Old and Picky

Eventually I "outgrew" Verge. The slow dissolution of the community (as most online communities experience, eventually) is probably what did it, honestly. It was easy to overlook the technical faults of the engine when there was a community of people to share excitement with.

The idea of Verge also, early on, sparked in me the realization that an engine can be made by anyone. I love the idea of a reusable, useful core to build lots of games on top of. This realization has been a bit of a double-edged sword, though -- I have a pathological need to build things as generically as possible now, and to approach every game in the content of an "engine". I want to make a game, but I also want to write as little as possible in a way that it is specific and unique to that game.

This led to me splitting my time between trying other game engines, and building my own. No engine that I tried ever seemed to match Verge, even though they were technically more capable. I realize now that the problem never really was the technical issues, but it was me: I'm an introvert by nature and will not usually immerse myself into the community. Even with Verge it took me quite a while to become comfortable engaging with everyone else. With other engines, I just never did, which meant they always felt incomplete.

Given all of that, it seems silly that my fallback would be to build my own engine, but here we are. I started a lot of them. The one that's gotten closest to complete (in that, I ever shipped anything with it) is Cozy. I'm realizing now, as I write this, that I think I've finally figured out why. No matter how much I tried to keep myself focused on technical issues, in the back of my mind I was thinking about how Cozy would support people working together and sharing things, and how a community could build up around it. That might have been what kept me going, the imagined future community.

## Always an Engine, Never a Game

The problem with all of this is that I don't actually especially *want* to build a game engine. I want to build games. Forcing myself to build an engine first, before a game, is just procrastinating. Without an engine that I like to hang my hat on, though, the other option is just hand-rolling things at a lower level, and I hate that idea.

So recently, during the end-of-year holidays, I decided to suck it up and take a hard look at some Actual Engines. There were a few stipulations I had...

- I have to enjoy using it
- I have to be able to hold my nose and accept the architecture
- I have to have *some* path for future portability of the games
- I can't be the only person maintaining it

In retrospect maybe I should have put "It needs to have a community around it" but I hadn't written this post at that point.

Cozy, by the way, fulfills the first two of these well, almost by definition. It absolutely falls flat on the last two. Being based on web-technology, the games work great on Windows and Mac and in a browser. Linux would be fine too, but I haven't tried it. Consoles and phones would be a garbage fire, and would probably just mean rewriting everything from scratch, losing most of the benefits of the engine that made me create it in the first place. The last point is particularly salient too -- like I said, I want to make games, not maintain engines.

## A Decision?

I tried a handful of different things, and maybe I'll write more about them in the future, but for now I've settled on [Godot](https://godotengine.org/). I've still only been working with it for a couple of weeks, but so far it's feeling pretty good. I've been building small prototypes in it, and am just about at the point where I want to build something a little more "real", something new along the lines of SimpleQuest.
