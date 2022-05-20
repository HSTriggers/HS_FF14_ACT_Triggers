**THIS IS FOR GROWN UPS ONLY**

First, I have to say that this is very much based on and inspired by /u/TwilightsHerald's post [here](https://old.reddit.com/r/HealSluts/comments/czui0n/ffxiv_silly_act_tricks/). Thank you for that amazing work!

In fact, if you'd like to give my healslut triggers a try, you'll first want to head over to that post for the detailled setup instructions and the script file, which includes the images that are also used by my trigger file. I hope reusing them is okay.

Screenshot: https://github.com/HSTriggers/HS_FF14_ACT_Triggers/blob/main/HS_FF14_ACT_Triggers.png

So after seeing that post, I wanted to try adding some additional triggers that make things more interactive and came up with triggers to do the following:

* Restrict things so it only activates inside duties/dungeons

* Count commendations after finishing a dungeon and make a TTS comment depending on the number

* Chance for a random (out of three) TTS comments when healing a tank in your party

* Chance for TTS comment when healing a DPS in your party

* Chance for TTS comment when healing the other healer in your party

* Chance for TTS comment when healing yourself

* Chance for TTS comment when being healed

* TTS comment when dying (works outside of dungeons)

* TTS comment when someone in your party dies

Except for the first point, it's very easy to enable and disable these functions one by one according to your own tastes. If you like being restricted to healing only, there's also a 0 DPS slut mode with the following triggers:

* Chance for TTS comment when DPSing a single target

* Increased opacity of the spiral and suggestions when DPSing a single target (decreases over time)

* Decrease increased opacity by healing

---

**SETUP**

Download this [Healslut.xml](https://raw.githubusercontent.com/HSTriggers/HS_FF14_ACT_Triggers/main/Healslut.xml) file and import it into Triggernometry. It assumes that /u/TwilightsHerald's script is unpacked to "C:\HS\" so you have "C:\HS\Background Spiral.gif", but you can also either search and replace the path inside the XML file or edit the path to the spiral on the "Start dungeon (EDIT SPIRAL PATH HERE)" trigger that will show up inside the Healslut folder in Triggernometry. Tick on the "Healslut" folder to enable the triggers.

I modified the suggestions that are shown to use text auras to make them easier to change, but it doesn't look quite as nice as the images from the original script. You can switch it back to use the image version by ticking and unticking the triggers in the Healslut\Suggestions folder in Triggernometry. But if you use the image version, you might have to edit all the paths unless you unpacked the original script to "C:\HS\"!

Unless you find Microsoft Sam hot, you will want to look into getting a nicer Windows TTS voice.

---

**CUSTOMIZE IT**

You can double click on the triggers and should see the list of actions inside. If you just want to change the text for the suggestions or the TTS lines, you can double click on those actions and just change it. If you want to make it work outside of dungeons, you'll have to go through each trigger, go to the conditions tab and untick the inDungeon condition, but I haven't tested it that way so it might do funny things?

For the random TTS line triggers, they each have an action that sets a variable to a random value as the first action. Depending on the random number, one (or none) of the TTS actions below that are triggered, so you can adjust how often you get a TTS comment by changing the upper number. Higher numbers will make the comments more rare, while setting it to 25 will make you get a comment with every action. The ranges are:

* Tank (1-60): 1-7, 8-15, 16-24

* DPS (1-60): 1-11, 12-15, 16-24

* Healer (1-40): 1-7, 8-15, 16-24

* Heal self (1-100): 1-39, 40-79

* DPS comment (1-100): 1-3, 4-6, 7-9

If you want to change the trigger range of a line or add more, you'll have to double click the action and change the condition. Since overlapping ranges will cause issues, if you adjust the upper boundary of a line, you may also have to change the lower boundary of the next.

I'm sorry if this sounds like gibberish, but I'm bad at explaining these things.

---

**BUGS**

* It doesn't actually check if an action is a heal or a DPS action, the triggers assume that anything you cast on yourself or a party member is a heal and that anything you cast on anyone else is an attack

* Once the next extension comes out and adds classes, they have to be added to some of the conditions on certain triggers

* I made it to work on 1920x1080. I'm not sure what happens if your screen has another resolution. In the worst case you'll have to adjust the text and image aura positions

* Yoshi-P doesn't like third party tools, so don't talk about it in-game
