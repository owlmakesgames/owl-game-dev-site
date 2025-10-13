---
layout: post
title: "Loki's Revenge Early Access Release Post Mortem"
date: 2025-10-13
---

![Loki's Revenge capsule art](/images/1232x706_MainCapsule.png)

It's been about 4 months since the release of [Loki's Revenge](https://store.steampowered.com/app/2936750/Lokis_Revenge/) at the time I'm writing this post. I've been meaning to write about how the launch went and publicly share my thoughts on the release of my first commercial game as OWL.

If you're unfamiliar, Loki's Revenge is a Norse survivors-like game. On the steam page, I describe it as:
>Loki’s Revenge is a survivors-like roguelite where you play as Norse gods fighting Loki’s army of monsters! Level up to gain powerful upgrades and explore hand-crafted maps to find secrets. Build the ultimate overpowered god with permanent upgrades and master each god’s signature ability.

In non-marketing words: it's a Vampire Survivors clone, but with a Norse mythology theme. 

Now before I get into the story of the game's development and my main takeaways, here's the important numbers up front:

![Screenshot of steam stats](/images/Loki_stats_10_10_25.png)

* Early Access Launch date: 06/23/25
* Launch price: $1.99, with a 10% discount
* Wishlists at launch: 972
* Copies sold on launch day: 93

Stats as of 10/10/25:

* Lifetime copies sold: 370
* Returns: 18 (4.9%)
* Net Steam Revenue: $619
* Outstanding wishlists: 1283
* Wishlist conversion rate: 12.3%
* Median playtime: 48 minutes
* Reviews: 11
* Steam sentiment rating: Positive

I'll dig into this a bit later on - but in short, pretty shitty if I wanted to do this full time! Thankfully this has been a side project and I'm fully employed by day. So for my first solo commercial game (I've worked on games professionally), it's definitely a better outcome than most. 
<br><br>

## Origin &  Development

I started working on the game in November of 2023 - this was around the time Survivors-likes had been popping off and there were several stories of solo devs seeing multi-million dollar success from small-scoped games similar to Vampire Survivors. At the time, there weren't really any Norse themed versions of the game, and I thought it was a gap in the market worth pursuing.

I had been wanting to take a proper crack at solo development, and just like most everyone who does it, I wanted it to be a full-time thing. So I deliberately was framing my thinking in terms of what was likely to sell well. I like Roguelikes/lites as a genre, and Vampire Survivors fell neatly into the box of "I could definitely do this myself" and "I think I can do it better or differently." So Loki's Revenge definitely did _not_ start out of a place of passion. I wasn't obsessively playing VS or any of the others in the new genre. I played a bit of VS and mostly thought "wow I could do that." 20 Minutes Till Dawn I liked the most and actually played several runs of. I liked Norse mythology in a pop culture sense (God of War: Ragnarok, the Marvel takes, etc.) but was never deeply invested in it and didn't actually know a lot about it. 

Regardless, I had a euphoric excitement about the concept and immediately dove into building it. I used Godot for the first time, which I absolutely fell in love with. I started with Game Maker 8 back in high school, and Godot felt like a familiar, maybe "grown-up" version of Game Maker. I've used Unity and worked on Unreal projects, but neither of them ever really clicked for me. Godot just makes sense to my brain, and it's a real joy to use. I currently plan to make all my future games in Godot (barring experiments with stuff like Pico8 or GB Studio). 

My development time largely consisted of the 1-2 hours before work (I've been fortunate enough to be able to work from home) and the occasional weekend hours. I probably spent an average of 8-10 hours a week over the 1.5 years it took me to finish the EA version of the game. It definitely varied depending on the week and what was going on in my life at the time, but I did my best to remain consistent even when I wasn't really feeling like working on it. It was genuinely difficult to maintain this - often I wanted nothing more than to just play games or watch a show or something instead of spending my morning doing extra work before my day job. However, that determination and discipline is what enabled me to actually finish the EA version of the game and launch it on Steam. 

An aside on that discipline: I've talked about part-time solo development with a number of people who are interested, have tried working with other people part-time as a team, etc. and the most common reason I find that things fall apart or people don't follow through is that they just give up too easily. They're not willing to make the sacrifice in wherever else they're spending their time in order to do this. To be clear - that's not a value judgment, I don't blame anyone for not wanting to spend hundreds or thousands of hours of their life to make something that probably won't materialize much for them. I wish I didn't feel so compelled to make games and could just play others games or something with that time! Point being - if you're reading this and want to take the plunge but haven't, just know that there's no shortcut or cheat - it's genuinely difficult work at times and you just have to stay consistent and put in the time.

Anyway, back to Loki's development: all of the code was written by me, with some of it early on being adapted from tutorials. A majority of the art is from a couple of asset packs (some stuff I made myself or edited from asset packs), all of the music is creative commons, and the sound effects are all creative commons with a couple being mixes/edits I did. I deliberately picked assets that I hadn't seen used in other games and that fit what I was going for pretty well. I ended up using shaders and effects to make everything feel more cohesive and not tip off that I was using pre-made assets.

The only asset I regret using is the tutorial code. It's a janky mess of poorly written and unoptimized code that I should've gotten rid of soon after I found it. Tutorials and the like can be useful to get an idea of how to prototype and build things when you're just starting out, but they're terrible for using as production-quality code. Unfortunately, I ended up leaving it in and now Loki has a bunch of tech debt that I really do not want to mess with because it'll require a lot of refactoring and rebuilding to keep things stable. (More on that later)

Promotional marketing activities took up a good portion of the time I spent on development - I submitted to festivals (never got into any), tried posting on Reddit and Bluesky, entered Steam NextFest, and reached out to a bunch of YouTubers & press. The most effective things ended up being NextFest, YouTubers, and Reddit Ads. At some point, I gave up on social posting and decided I was just going to focus primarily on development and rely on whatever organic attention I got at that point.

I also had a demo up for several months before releasing the game, which I think definitely helped get the reception that it got. It helped build wishlists (even just _having_ the demo, not even having people play it, helped boost wishlists. It felt more real to people.) and led to a few consistent players reporting bugs and feedback that dramatically reshaped the game probably for the better.
<br><br>

## Release, Reception, and Steam Numbers Analyzed

On release day, I took the day off of work to push the buttons and get ready for any bug fixing or community responses I needed to handle. Thankfully, no major bugs were found that required an emergency patch - just smaller stuff I was able to clean up without much pressure. 

I think only other game developers or creatives will understand this: but on launch day, I felt nothing. I thought I would feel excited, scared, nervous, or any sort of strong emotion, but instead I felt... nothing. Clicking the release buttons on Steam alone in my room left me feeling the same as I had before. Maybe it's because I didn't have a large, eager group of people waiting for  the release? Maybe it's because I just viewed it as another thing on the task list and knew I wasn't really done with the game? Maybe something is wrong with me? It was difficult to be asked by friends and family if I was excited or anything having launched the game, because what they wanted to hear was "yes it's amazing!" but what I felt was "no, it's just Monday."

Anyway, the reviews and response were generally positive from players. Not many people bought the game, but those who did seemed to enjoy their time with it. There were several people who posted YouTube videos of their playthroughs and a bunch of people on the Steam forums reporting bugs, giving feedback, and generally expressing that they enjoyed the game.

The most rewarding reception came from 2 individuals:

Firstly was from Steam user Nosteru who was a supporter from Day 1. The guy started replying to other players for me to handle feedback or explain the game! He's always been supportive and a genuinely nice dude, and it really made me happy to see him enjoying the game and interacting so much. He's made my day more times than he knows.

The other was from Steam user Falkathemage. She reported that she, her husband, and a friend had all gotten the game Day 1 and played through all of the content together at the same time. They 100%'d everything I had made and didn't seem to mind running into crash bugs. She doesn't know it, but knowing that 3 random people out in the world bought my game and enjoyed playing it together for an afternoon was the most impactful, heart-warming thing that happened on launch day.

![Screenshot of steam stats](/images/Loki_stats_10_10_25.png)

Some observations on the Steam sales numbers:
- The biggest sales day was launch day, by far
- The 2nd biggest was when I got 10 reviews and Steam bumped me in their discovery queue weeks after launch
- My refund rate and conversion rate are within normal bounds - so it seems that if people think they'll like the game, they probably do. But most people don't think they will

I've been negative about the sales figures, but I want to express that I'm genuinely thankful and amazed that so many people have bought the game. I hoped for more, but expected less, so my expectations have been exceeded. I know that your 1st game is usually the weakest performer, so this makes me hopeful that my future games will do even better, both financially and artistically. 
<br><br>

## Takeaways
I've got 3 lessons that I learned from shipping this game:

1. You need to look different from the competition
2. Content is king
3. I don't even like the game or genre
<br><br>

### You need to look different from the competition

"This isn't that different from VS" is a common point of feedback that I've gotten from players and from would-be-players. Even though there's mechanical differentiation from Vampire Survivors, people still insist that Loki is not different enough from that game to warrant their time. I think really what this comes down to is that it _looks_ similar to VS - as in, it's 2D 16-bit-ish pixel art, similar UI, and nothing dramatically different gameplay-wise. It doesn't matter that the maps aren't randomly-generated, or that there's way more polish in the player and enemies, or that there's active abilities you can use - because it _looks_ mostly like VS, players decided they don't care enough to try it.

A great example at the time of writing is Megabonk: gameplay-wise, it's just VS (I know you can jump and whatnot, but I consider that comparable to Loki's active abilities as a "one mechanical difference"). However, I think that because it's 3D, it's now a multi-million dollar seller within a month of release. I believe that if Loki was 3D or hand-drawn or something, it would've done way better. Or, I would've had to sell the experience of being a Norse god way harder - maybe through dialogue like Hades, or some other mechanics and visuals. Point being, I played it too safe and it stuck too closely to what VS looks like, so it hasn't taken off like I'd hoped.
 
Also, a point on the marketing angle that may inevitably come up in response (i.e. "did you market the game enough") -  It's partially a symptom of being solo and part-time: I really just don't feel like spending weeks of my limited time not working on the game and instead begging people to cover it. My opinion at this point after shipping Loki and studying all the cases Chris Zukowski covers on howtomarketagame.com is that a game destined to be a success won't require that begging - it'll need the most gentle of nudges and it'll snowball on its own with organic attention, OR you throw money at the problem and make it impossible to _not_ see the game while online. In other words, there was no way I was going to be able to post my way into Loki's Revenge achieving Megabonk levels of success. The reality is that it just isn't a visually or experientially appealing game to enough people to attract the level of organic attention it would need to thrive, and I'm not interested in rolling that particular boulder up the mountain.
<br><br>

### Content is king

For those that did end up buying it and enjoying it, a common point of feedback is that there just isn't a lot of stuff to do in the game. On launch day, I had several people report back within a few hours that they had 100% completed all the available content. A year and a half of my life, and it was all finished in a couple hours!

One of the things I learned from making and launching this game is that there's a contingent of people who enjoy the survivors-like genre enough that they buy up just about every one and play through them completely. They're great 2nd screen games for a lot of folks and are just enough interaction to feel like you're doing something, but not enough to require your full attention. That same type of player really likes completing everything these games have to offer and getting the full achievement list completed. Had I launched with more content, I think I may have seen more word-of-mouth success from early players becoming evangelists. 

Thankfully, players were forgiving about the amount of content because I launched into Early Access - there's an expectation that more content will be added over time. That's a bit of a double-edged sword, though: players may be more forgiving and generous with their opinion because they have an idea in their head of what the game will look like months from now. However, if it never meets their expectations, I could lose some good will with previously satisfied players.

For future games: any roguelikes or similar that I make, I know I'll need to launch with a lot more content than I think I do. There's usually like, 5 different systems interacting with each other each filled with a ton of stuff that makes these games compelling and that make people want to play them for hundreds of hours. 

As a player, I generally like short games that don't overstay their welcome - they take a few hours to say what they want to say, and then they're done. That's more of what I want to make - so in that context, this lesson is less quantity and more quality. 
<br><br>

### I don't even like the game or genre

This is probably obvious based on everything I wrote above, but truth be told, making this game taught me that I just do not like survivors-likes. I think they're kind of "slop" games - minimal interaction, relying mostly on "number go up" in the form of DPS and enemies killed, flashy slot machine-adjacent VFX to make you feel good about a level up, and otherwise just not much of substance. I think it's just inherent to the genre - based on the player profile I described above that seemed to latch onto this game, I'm highly suspicious that more meaningful interaction or a story or anything would see the same success as some of the mega hits in the genre. Ask someone who dislikes video games, and they'll tell you I just described every video game in existence - so maybe my point is invalid, and it's just that the smoke and mirrors we game developers put up to make players feel like they're accomplishing something is just too thin in this genre for me to get into it.

Earlier, I described the origins of this game purely based on the cartoonish dollar signs I had in my eyes when I saw VS and similar games doing well. That clouded my judgment and I ended up making something I didn't really care about or enjoy because I thought it would make me money - that's what I do at my day job! I spent a year and a half making a 2nd job for myself rather than making something I actually enjoyed! I think because I enjoy the process of making games, it didn't bother me much until close to shipping the initial EA version and being confronted with needing to make updates that it started to bother me.
<br><br>

## The Future

As for the future of Loki's Revenge, the need to update it with more content has caused me great anxiety. My plans early on were to gauge reception and then update it accordingly. If it had sold well, maybe I would've quit my job and gone all-in on updates. Reality is that it didn't, so I won't. I've pushed a few minor patches with some fixes and new content, but the level of tech debt is so agonizing to deal with that I truly just want to put it away forever most of the time. The source code is like an archeological dig site: you can see the layers of my growth as a developer, learning how to do things better over time. Dig in deep enough, and some of the core systems that everything else is standing on are brittle and trying to rework them will cause a domino effect I need to deal with of reworking things. It makes working on the game further really tiresome and that makes me want to work on it even less. Refactoring it wouldn't be worth the investment and the opportunity cost of working on other games. I also have had a lot of major life changes (all positive!) so it's been difficult to spend the same amount of time that I used to on working on games.

Recently, though, I had an epiphany after seeing another dev post about updating a previous game on the same day as launching a new one - I can do whatever I want! I can work on new stuff AND still update Loki from time to time. I don't want to abandon the game or disappoint players who paid for it expecting more content - I want to fulfill that promise, and part of me wants to finish what I started. I think the best compromise is to periodically work through the list of improvements and new content I've thought up until I get to a point that I'm comfortable calling it 1.0 and doing the full release on Steam. 

Simultaneously, I can work on other games and release them at whatever pace I want to. If I'm going to spend my free time making games, I want to only make things that I actually like and worry less about them needing to make enough money to live on full-time. Games are my artistic outlet and I have the luxury of being able to create whatever I want to without a publisher or boss demanding I conform it to what The Market wants or whatever. 

<br>
<br>
<br>
<br>
Thanks for reading! If you have questions or comments, feel free to email me at owl@owlgame.dev or hit me up on Bluesky.