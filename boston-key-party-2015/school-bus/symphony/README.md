# Boston Key Party CTF 2015: symphony

**Category:** 
**Points:** 
**Solves** 
**Description:**

> A less than four characters number, bigger than 999?Maybe the bug is elsewhere. : 25

## Write-up

**BKP CTF 2015 Symphony Writeup - xenocidewiki**

http://52.10.107.64:8002 - You were given this link for the challenge, where you had a password field, and the description was: "A less than four characters number, bigger than 999? Maybe the bug is elsewhere" - Basically it told you you had to enter in a number that is 3 chars but that is bigger than 999, interesting right? So i simply tried to enter in 1000 for fun, and it told me that it was too long, then i entered 999 and it told me "Too Short". 

What i usually do in these situations is that i check the page source, and so i did.. 
I looked at it a bit, and i could see a link to "index.txt" so i clicked it, basically it just gave you the whole page source! Which made things easier, although you cannot view the page right now 
( http://52.10.107.64:8002/index.txt) then well i can tell you that it was pretty easy from then on. You could see that the php function is calling "is_numeric" which basically checks for if the number you enter in is numeric, now while you check some stuff about that function on php.net then you can notice what 'is_numeric' accepts as a input. 

It stands under "Description" on the page what the function accepts, so what i did, is just went to the main page of the challenge, entered '9e9' and so i got the flag and scored 25 points for my team. 

Pretty easy huh? ;) 

I also got a bit of help from my friend t understand it, what he said is that '9e9' equals '9 * 10 ^2' which is ofc higher than 999, and thats the reason it got accepted.

## Other write-ups and resources

* none yet
