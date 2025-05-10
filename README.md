# 2016-client
how to patch the cool client
*Note*
i gonna test some stuff then i will give the files link and i will edit this

its my first time messing with github thing so yea

# You will Need

1. Be enough smart to do this
2. a 10 letter domain or 14 letter domain
3. Hex Editor https://mh-nexus.de/en/hxd/ (Hxd)
4. 32x Debug https://x64dbg.com/ (x64 debug wont work) 



# Setting up the Website

Your domain needs to be 14 letters or 10
**Example**: domain.net finobe.com domain14.ix.tc

After that Paste theses files *in your website*

# Patching the client

go on https://archive.roblonium.com/Client/Windows/RobloxPlayer/main%20%28roblox.com%29/2016/

grab the 12.2016 client

Now, you need to have Hxd and 32x Debug!

with hxd press *Ctrl + R*
then a window will appear replace roblox.com with your domain

if your domain is 14 characters then replace http://www.roblox.com with your 14 character domain like this:

http://domain14.ix.tc

DO NOT DO http://www.domain14.ix.tc
or the client will be broken!

press *Ctrl + F* 
then another window will appear
search for *BGIAA*
then there will be a base64 code
replace it with

**BgIAAACkAABSU0ExAAQAAAEAAQAdbgKO2az2CNiZWlnReZEHme4DeoMUCc1UGVS73S8RzOovtJp/P92RTklp7iYRiEM7PQHaJoU8nQ3mAHaWV/p2tKRNU7/jrEwVvgYD75A31RbRsz2zqVvEcuTi/RuZG45kqsxmtN2gaWCNxDo2ry3O5SmP9CNM86595MubfsXcrw==**

Now go on file and press on *Save as*
save it as **patched.exe** or whatever name you want **must include .exe in the end**

open the client with 32x debug (the one that you messed with hxd)

then you will be on cpu
click on *symboyls* (my writing sucks idk if its right)

then there will be something like **patched.exe** (the name of your client)
Double click it
There will be a "Az" button on the top bar
click on it
it will start to search stuff

after its done Search for "Trust Check failed"
there will be 3 trust check
double click on the first that appear
there will be something like

**push thenameofyourclient**

on top of it there will be something like 

**jne thenameofyourclient**

Select it then press the space bar

change the jne to jmp
press ok

go on **references**

then there will be the others trust check

go on the second one

after some random stuff there will be a jne
do the same thing that you have done with the first one

go back on references there will have the third one, do the same thing that you did to the second one

go back to references

Search for **invalid request 5**

do the same thing that you did to the trust check

there will be a jne above it then change to jmp

# Finishing the patch
Go on file then go on patch file, press the patch file and rename it to something else since you cant overwrite the other .exe
you just patched the damn client but its not done yet

in the client folder there will be **AppSettings.xml**
edit it with notepad or something then there will be something like

http://www.roblox.com

change it to *your domain*
Save it

# Final Steps

Create a .bat file then edit it 
write

**start yourclientnamegoeshere.exe -a "http://yourdomaingoeshere/login/negotiate.ashx" -j "http://yourdomaingoeshere/game/join.ashx" -t "1"**
save it
open it to see if it works
when the client open it should appear a error like
"Failed to connect to the game ID=17"
if if appears the Congratulations your client works

if it appear "Could not connect to the game due to joinscript failure"
dm me for help


# Patching RCCService (NEEDED)
Download the rccservice
with hxd open it

replace roblox.com with your domain
do the same thing that i told you
if it 14 letters then replace
http://www.roblox.com
with your domain something like

http://domain14.net

yea replace domain14.net with your 14 letter domain

save it as "patched.exe" or something like that

change the appsettings to your domain

if needed edit the "run.bat" and change "start rccservice.exe" to "start yourccservicenamegoeshere.exe"

# Final Steps

open run.bat
then it will appear some stuff wait until a while
then open your .bat in your client folder
then it should join




if you need any help dm me on discorda (mayhv23)
