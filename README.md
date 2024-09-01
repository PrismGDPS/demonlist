# Make Own DemonList
## Also put credits to aredl and tsl (there is some nonproven info that redlime is one of creators of list)
So i highly recommend downloading new versions of aredl's demonlists "https://github.com/All-Rated-Extreme-Demon-List/AREDL" and updating your demonlist by yourself. but this is just simple way to easily copy aredl's demonlist src. (so you can spend time editing it fast) Ah before it starts check this https://discord.com/channels/1087797698771566644/1268510011009536041 Also delete the file tutorial.txt in data

So this is tutorial below for every single feature that is important
```
MADE BY CATCOOLYE : LINK TO CREATOR : https://www.youtube.com/@catcoolye/
FOR SUPPORT PLS WRITE ME IN DISCORD: catcoolye

ChangeLog:
To change stuff in _changelog.json, read this

Actions are only placed, raised, removed, lowered, tolegacy.
Also for date use: unix timestamp. https://www.unixtimestamp.com/
If level has been created than in "from rank": write null after.
If level has been raised up than in "from rank": previous rank. and in "to_rank": new rank where it has been placed.
And if level has been lowered than do steps like with raising level. but in reverse.
"From rank": previous rank.
And "to_rank" new rank. (needs to be lower)
Tolegancy: (NO INFO)
Also here is a example how does every tutorial:
	{
		"date": 1722398057,
		"action": "placed",
		"name": "brain_power",
		"to_rank": 768,
		"from_rank": null,
		"above": "pound_town",
		"below": "zenith"
	}, 
(if level is last remove ",")

Editors:
So if you want editors to not be the same as editors of aredl. then go into _editors.json.
And change some stuff. if you want different name then in "name": "type your nickname".
If you have youtube or other platforms then in "link": "type link" (you can leave it empty if you want).:
it can look like that:

{
        "role": "owner",
        "members": [
            {
                "name": "iiLogan",
                "link": "https://www.youtube.com/channel/UCPyzU-PttFOyup6UYQ-rQMQ"
            }
        ]
    },
If you have multiple people in one category it may look like that:
{
        "role": "owner",
        "members": [
            {
                "name": "iiLogan",
                "link": "https://www.youtube.com/channel/UCPyzU-PttFOyup6UYQ-rQMQ"
            },
            {
                "name": "iiLogan",
                "link": "https://www.youtube.com/channel/UCPyzU-PttFOyup6UYQ-rQMQ"
            }
        ]
    },
Helpful stuff: (role names: owner, coowner, admin, trial, helper, dev) if you didn't change role names or modify this template. then all of the role names should be named like that.

legacy and list. (_list_init.json and _legacy_init.json is old one so dont touch them):
so they pretty easy.
Manually put on what place demon is.
Like we have two demons that we want to put.
so they named "test_1" and "test_2" know that you need to put JSON name of level. We will make a JSON file of the level later
so if test 1 is harder than test 2 we put it like that in demonlist
{"test_1",
 "test_2"
}
Also dont forget to remove "," if it the last level on the list. because list will break.

pack lists:
so if you want to have pack lists on your demonlist: play around with _packlist.json:
so if you want custom name for pack of levels than do this "name": "yourlist name": To have custom levels in packs do like in legacy and list tutorial.
Colour for list: that a hard one. play around with yourself with it. cuz i have no idea how can i explain it to you.
Pack tiers: exact same thing as pack list but a lil different but you can do it yourself.

LEVELS EDITOR. aka demons:
so if you dont want to use boring gd official demons. and want to use your own. then go into one of alot levels (i deleted all of them but left only two of them: wave breaker and ZOOOOOOOOOOOOOOOOOOM and i say to do it for you too) that i left in data folder:
so first things first name json file for example test_1.json.
Then open the file:
Next paste this code
{
	"id": 1,
	"name": "Level Name",
	"author": "Test3",
	"creators": [
		"Test1",
		"Test2"
	],
	"verifier": "verifier",
	"verification": "link verification",
	"percentToQualify": 51,
	"password": "put here password",
	"records": []
}
after that you want to change stuff: so in id paste demon id. in "name": "paste your demon name",
Then in author paste who uploaded the level on your gdps.
Then looks there is creators thing: now if your demon is COLLAB then paste a couple of creators of the level there.
I think with verifier yk what to do. But let me explain verification, percentToQualify, password and records.
SO verification: if level was verified then paste the link of video verification.
PercentToQualify: basically how many percent do you need to beat the level. i recommend to put there 51.
Password: for new 2.2 levels just put no password or Free To Copy. if gdps is 2.1 or has levels from 2.1 than put there password for the level. (like 111111)
The last and the most interesting one... Records: So if you want people to have records on demons and it to show up paste this code in brackets in "records":[Right here]:
		{
			"user": "Test4",
			"link": "Link",
			"percent": 100,
			"hz": 360
		}, (if it is the last level than remove ",")
So it is the last and easy one, replace  test4 with user who beat level. and replace Link with an actual link of verification.
Now percent: if percent is lower than percenttoqualify than dont put it. if yes than put it. as it is 100% than it will be on the list anyway. and in hz put how many hz/fps player has beaten level on. so as we gone throught all of the data files. lets go throught other stuff a lil. To change nickname of the demonlist to not be "AREDL" then go into index.html and open it in any app is easy for ya. i am using notepad: so you will see a lot of stuff. we need All Rated Extreme Demons List. Rename it to whatever you want.  then next scroll down and you will see AREDL and v1.7.2. put version what you want and rename it to what you want. Then scroll down and you will see discord.gg/aredl. add other link to what you want. i am gonna go with my discord server. and we almost ended. but you want custom rules. If no then skip this and youre done:
Custom rules: go into js/pages and open lists.js. you will get warning but click ok then scroll to the row 119. and ends at row 182. if you want you can change stuff but i wont talk about it. cuz there is ALAT
Also aredl bot tutorial mbe soon so wait for it.

MAKE WEBSITE. if you can do it by yourself then skip this but i will go throught it: so open pages.dev. (you need to have GitHub and this project on it). the next task is to long in to your GitHub account throught Cloudflare. next when youve done it go to Workers & Pages then click create. Then click pages (connect here to git if you didnt), choose your account in next page. and click on your names project (ik it is repository) then click Begin setup then name in field box right below project name. and then click and deploy. so when it is done you should get to the site. if you dont there is 2 solutions: wait a little bit. redeploy your website. just simply clicking what is on image
also if you want to update your demonlist do last thing again but update files that you need to update and make branch than it will update

UPDATE VERSION 1.1
for this guide update i will show new stuff.

so new stuff:
File _supporters.json (i wont talk about it cuz it is like _editors.json).
Update for Level Files (gonna talk bout it)
And packtier reexplained.
Packtier: So i meant that it is like packs for levels. And it is like not. It is like pack for another packs
Level Files update.
Nothing really changed but there is a new one thing. is TAGS. now write tags like the showen below. You can put anything and extend as you want. and you can remove tags too. so this is the all for the update for guide. 
```
