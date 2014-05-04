---
layout: post
title: "Guardian II Attempt II"
date: 2014-02-27 17:17:31 +1300
comments: true
categories: guardian
---

A while back I abandoned Guardian II as I was unable to give it the gameplay I wanted.

Then, playing Guardian (I) again, I realised that the gameplay I tried to give it was not what I _really_ wanted.

What I wanted was a fun hack-and-slash platformer where the player controls one unit in a battle between two armies.  
What I tried to make was an RTS where the player has to fight _AND_ control their army. Not that fun.

**The relevant post can be found [here](http://heroesgravedevelopment.tumblr.com/post/62474167067) on my old blog.**

Even though I said I wasn't working on it anymore, shortly afterwards I completely
[rewrote the engine](http://heroesgravedevelopment.tumblr.com/post/66428716420)
and [worked on the spritesheet](http://heroesgravedevelopment.tumblr.com/post/65855743674).

Things in the codebase are very clean at the moment, and although I'm not expecting them to stay that way,
this is at least the 5th iteration of the engine, and that means I've had plenty of opportunity to get everything how I want it.

The pathfinding, and AI in general has had a massive improvement, and there's more to come.

In specific, I'm thinking of introducing a flag system for controlling units and the general flow of the game. More details below.

**Here's a general overview**

- You start off with one base.
    - The base has an initial spawn flag.
- To control units, you pick up a command flag and they will follow you.
    - The command flag can be placed on the ground, and then nearby units will hang around that flag.
    - If you are killed, the flag is dropped.
        - A brave enough unit can pick it up and continue.
    - If the flag is somehow destroyed by the enemy, nearby units panic (unless there is another flag nearby)
- To capture more bases, take a command flag to the spawn flag, tear down the spawn flag, and put up your one.
    - The base can then be used as a spawn point and if it is the final one for a level, allows you to advance.
- If your last spawn flag on a level is lost, you lose the level and must return to the nearest flag on the previous level.
    - If you lose your last flag on the last level, you lose the game.
- Units have randomly generated courage and aggression stats.
    - These two combined determine most of their AI.
        - Things like whether they attack, counter-attack, fight, flee, panic etc.
    - A unit must have high enough courage to pick up the command flag.
- Hopefully lots of different campaigns.

Anyway, I have lots of work to do.  
I'll blog more as things start coming together.

---
**HeroesGrave**