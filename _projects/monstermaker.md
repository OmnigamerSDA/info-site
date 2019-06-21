---
title: Monster Maker
subtitle: Custom Monsters for the Masses
layout: page
order: 5
icon: fa-compact-disc
---
<span class="image right"><img src="{{ 'assets/images/monstermaker.png' | relative_url }}" alt="" /></span>Early Monster Rancher games had a unique method of monster generation. To spawn a new monster, players were tasked with loading an unrelated CD into the PlayStation, and the game would use some of the information on the disc to create a monster. With hundreds of available monster types, it was quite a thrill to hunt around for any and every CD in the house just to see what monster turned up from it. Moreover, the monster's stats were also tied to the CD, so there were certainly "better" CDs than others.

Jump ahead to more recent years and [MetaSigma](https://twitch.tv/metasigma) was doing speedruns of Monster Rancher. Other players had put in a significant amount of effort trying to identify the particular CD data used to create the monsters, but there was still so much about the process that wasn't clearly understood. This seemed like a decent challenge, so I set about reverse engineering the rest of the process, and discovered the monster subtype and stat generation processes. With this information, it became possible to theorize all the possible monster builds, which substantially helped speedrun planning. The catch, however, was that you still needed a disc that could produce the theoretical monster.

And that's where the rest of this project came in. MonsterMaker is a simple program that contains all of the information I gathered from reverse engineering by letting you preview what monster would come from particular disc information. In addition, it actually can create a disc image with that information! Just burn the resulting image and pop it into the PlayStation, and you'll get the monster you previewed.

This program only works for Monster Rancher 1, however a similar process can also produce monsters for Monster Rancher 2. We understand the CD information that is used to create monsters, however the tables relating to type, subtype, and stats have not yet been pulled out. Maybe someday I'll revisit it for Monster Rancher 2, but it's not currently a high priority. You can check out the [GitHub](https://github.com/OmnigamerSDA/MonsterMaker) for the latest release and source code.