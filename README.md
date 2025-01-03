Minetest mod "Stamina+thirst"
=====================

(C) 2015 - BlockMen
(C) 2016 - Auke Kok <sofar@foo-projects.org>
(C) 2025 - MaoriG


About this mod:
---------------
This mod adds a stamina, hunger, and hydratation mechanics to Minetest. Actions like
crafting, walking, digging or fighting make the player exhausted. When
enough exhaustion has been accumulated, the player gets more tired,
and loses hunger.

If a player is low on hunger or thirst, they start taking periodical damage,
and ultimately will die if they do not eat food.

Eating food no longer heals the player. Instead, it increases the
satiation of the player. The hunger bar shows how well fed the player
is. More bread pieces means more satiation.

To take wáter you should punch a block that is in the wáter with a empty hand


Q&A time: Why won't I move the stamina bar to the right?

Answer: this conflicts with the builtin breath bar. To move the
builtin breath bar, I basically have to entirely re-implement it
in lua including timers to catch breath changes for each online
player, which is all a waste of time, just to move a few pixels
around.


For Modders:
------------
This mod intercepts minetest.item_eat(), and applies the hp_change
as stamina change. The value can be positive (increase stamina) or
negative (periodically damage the player by 1 hp).

See API.txt for information on the API.

License:
--------
Code:
- all code LGPL-2.1+
Textures:
- stamina_hud_poison.png - BlockMen (CC-BY 3.0)
- stamina_hud_fg.png - PilzAdam (WTFPL), modified by BlockMen
- stamina_hud_bg.png - PilzAdam (WTFPL), modified by BlockMen
Sounds:
- stamina_eat.*.ogg - http://www.freesound.org/people/sonictechtonic/sounds/242215/ CC-BY-3.0

