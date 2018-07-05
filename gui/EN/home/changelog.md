# ChangeLog

This is a fairly major update to Olex2. The major changes are outlined below.

## Reworked Help System for the GUI

You may have noticed that the help system looks different to what it used to be. It is also much more complete -- although nowhere as complete as we would like it to be.

The entire help system is generated from MarkDown files which are available from 

URL[https://github.com/Olex2/help/tree/master/gui/EN,GITHUB],

where these files render into some very readable format. This also means: anyone can contribute to our help system -- please request commit permission from us and we will welcome you as a valued contributor. In the long term, we are also planning to make this help available in different languages -- if you can help with a translation, please also let us know.

## New HAR

The Hishfeld Atom Refinement team around **Simon Grabowsky** and **Dylan Jyatilaka** have been working hard to update this exciting new refinement program. It is available through Olex2 from Tools > HARt.

## EXTI

Sometimes it is necessary to refine the extinction, and sometimes it is not. Olex2 now makes this decision automatically (it refines EXTI if the value is twice it's e.s.d.). If un-tick the box, EXTI will **not** be refined, and if you *re-tick* the box, it **will** be refined. You are in control!

## No more \_publ\_* items in the CIF

After many discussions with publishers, the IUCr and the CCDC, we have decided to remove all items starting with \_publ\_* from our CIF files. These have been replaced with \_audit\_* instead. This makes a lot of sense: each structure is a 'stand-alone' piece of work and its authors should be clearly known and acknowledged, regardless of where this structure will eventually end up. More info on URL[https://www.iucr.org/__data/iucr/cifdic_html/1/cif_core.dic/Caudit_author.html,\_audit\_author] here

