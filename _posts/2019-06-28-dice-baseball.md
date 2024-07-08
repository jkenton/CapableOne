---
layout: post
title: "Dice Baseball"
date: "2019-06-28 15:27:09 -0400"

---
**TLDR;**

Gather 'round people.

Get yourself three dice (yes, the six-sided kind, Dungeon Master) and a baseball scoring sheet.

Roll the dice. Add the sum and consult the table below

---

|||||||||
|:---:|:---:|:---:|:---:|:--:|:--:|:--:|:--:|
|3 | 4| 5| 6| 7| 8| 9| 10|
|3B | BB  | 1B  | 2B  |GO |SO|FO|FO|

---

|||||||||
|:---:|:---:|:---:|:---:|:--:|:--:|:--:|:--:|
|11|12|13|14|15|16|17|18|
|GO|HR|BB|BB|GO|BB|SO|1B|

---


Enjoy!


**Serious nerds only:**

I looked at the <a href="https://www.baseball-reference.com/leagues/MLB/2018.shtml">end of season stats</a> for the entire MLB, and looked for the incidence of the following events:
Singles (1B), Doubles (2B), Triples (3B), Home Runs (HR), Striekouts (SO), Ground Outs (GO), Fly Outs (FO), and all the various ways that someone can earn 1st base without hitting (BB, HBP, IBB)

| | | ||
|:---:|:---:|:---:|:---:|
|1B|2B|3B|HR|
|.143|0.045|.0045|.03|
| | | | | |
|SO|GO|FO|BB|
|.224|.201|.251|.100|

The lowest occurrence that needs to be resolved is 3B, at about 1/200 AB.

I wanted to be able to use common household items (like dice). 2 dice only resolves down to .03 or so (1/36). Three dice gives 216 (6x6x6) options. Every numerical combination between 3-18 is possible.

Then, I looked at the probability of rolling each possible dice roll"

I know from statistics that there are only limited ways to get 3 and 18 (1x1x1 and 6x6x6, respectively), and that there are lots more different ways to get a combination in the "middle" of the range (10 & 11; each 27 ways/216)

||||
|:---:|:---:|:---:|
|P(3)| P(18)|	1/216= 0.0046	|
|P(4)|P(17)|	3/216= 0.0138|
|P(5)|P(16)|	6/216= 0.0276|
|P(6)| p(15)|	10/216= 0.0460|
|p(7)| p(14)| 15/216= 0.0694|
|p(8)| p(13)|	21/216= 0.0972|
|p(9)| p(12)|	25/216= 0.1157|
|p(10)| p(11)|	27/216= 0.125|

Now, to find a way to assign one outcome to each of the 16 possible scores 3-18. I started with the lowest incidences (3B and HBP), and the highest incidences (FO and SO) and worked my way back toward the middle.

This table is how I came to assign the dice results in the first table waaaay up above:

|||||
|:--:|:---:|:---:|:---:|
|**Action**|**MLB %** |**3d6 Pred**|**Dice**|
|1B|.143|.1526 |(p(5) + p(10)|
|2B|.045|.046 |p(6)|		
|3B|.0045|.0046| p(3)|
|HR|.030|.0276 |p(16)|
|SO|.224|.2129 |p(8) + p(9)| 	
|GO|.201| .2136|p(7) + p(13) + p(15)|
|FO|.251|.2407| p(11) + p(12)|
|BB|.085|.0832| p(14) + p(17)|
|IBB|.01|.0138| p(4)|
|HBP|.005|.0046| p(18)|
|**Totals**|.9985| .9996||

If you've got a better way to assign the dice results, let me know. Otherwise, the game is really fun to play with another person. Admittedly, there is no base stealing, and the rule about potential double plays (any GO with a runner on first) makes things a "little" unfair. Without it though, the incidence of 1B is a tiny bit higher than predicted, and the box scores and pitcher ERA become a little bit inflated.

It's a fun game, though, and a nice subsitution for Yahtzee on a rainy summer day...

ENJOY!

[Ed: This post was informed by a webpage about [Desktop Baseball](https://www.housewifeeclectic.com/tabletop-dice-baseball-game-scorecard-printable/), but that webpage calls for just two dice. As nerds know, that would only give 36 possibilities, which is not precise enough (for nerds), so I did all the work above to "improve" (from a nerd's point of view) the rules I originally found.]
