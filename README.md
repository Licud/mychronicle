# MyChronicle

Diary app to record what happens in a day. 

Adding this as one of my active projects. I got intrigued by 'FreeWriting' which is essentially writing on a diary with a set amount of time with no stopping. You just write and a timer will start with the goal of looking back on the day and focusing on items that you learned, issues you faced and minimal details on how you overcome them.

## Why
I wanted a place to journal so I'll build my own. Could use other apps but wanted the challenge while actually learning on the side. Also I fell down a rabbit hole reading about Freewriting and figured — how hard could it be? (famous last words.)

## Features

- I'd want a web UI that will effectively just present you with a giant text box. The moment a character is written, the timer starts. Once the timer ends, no going back - forces me to actually think through the day before starting to write.
- Plan to deploy this online so it should support multiple users. A key will be used to encrypt the message so even with malicious access to the database, heck or even me, I won't be able to see the actual entry. To that end, the user will have to remember the key themselves, lose it and goodbye to the entries.
- User would not be allowed to delete a diary entry. 
- User can only modify the current day's diary entry, and only one entry can be made for the day. 
- There should be a signup page where the user signs up and provides their encryption key. Might look into passwordless login techniques like Magic Links instead of keeping a password on the db, tbc. 
- Would probably add a reset button for accounts that lose their key.. It's pretty simple really, I'll delete all entries on the db :D Can't decrypt them anyway if the key gets lost.. 
- Display old entries - if you provide your key, not sure what the layout would look like but I'll figure it out.

## Maybe, Who knows
- I'm not confirming this feature because I don't know how I can make it work yet - but if you have an AI API key, and you give it to the app, I'll push your entries to that AI and have it summarize the entries for you one time. Of course, it will be opt in as you actually need to give your API key, which again I won't store and only use one time. No promises - I'll probably only use the AI summary once myself out of curiosity and never again so maybe don't give personal info? Ah I'll figure it out..probably. I mean, it'll be up to a user anyway if they really want to feed entries to their AI of choice.

## Privacy Model

Your entries are encrypted on your device before they ever hit the server, using a key that only you know. I don't store it, I don't recover it, I genuinely cannot read your diary. Lose the key and the entries are gone — that's the deal. It's not a bug, it's the whole point.

## Tech stack

- PostgreSql db
- FastApi backend
- React Frontend

## Deployment

- Supabase to host db and backend, tbc
- Railway to host React, tbc

## Notes

I might commit some things at the start while I learn the tech stack, so bear with. :P 
