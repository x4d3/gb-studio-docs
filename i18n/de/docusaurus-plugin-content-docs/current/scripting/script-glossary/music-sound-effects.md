---
sidebar_position: 2
#
# This file is autogenerated. DO NOT MODIFY DIRECTLY
#
---

import ScriptEventPreview from '@site/src/components/ScriptEventPreview';

# Musik & Sound Effekte

## Musik: Titel Abspielen
Plays a music file. If you play a new song while another song is playing, the old song will stop automatically.
<ScriptEventPreview title={"Musik: Titel Abspielen"} fields={[{"key":"musicId","label":"Song","description":"The song to play.","type":"music","defaultValue":"LAST_MUSIC"}]} />

- **Song**: The song to play.  

## Sound: Effekt abspielen
<ScriptEventPreview title={"Sound: Effekt abspielen"} fields={[{"key":"type","type":"soundEffect","label":"Sound-Effekte","defaultValue":"beep","flexBasis":"60%"},{"key":"priority","label":"Priorität","type":"priority","options":[["low","Niedrig"],["medium","Mittel"],["high","Hoch"]],"defaultValue":"medium","flexBasis":"15%"},{"key":"pitch","type":"number","label":"Tonhöhe","conditions":[{"key":"type","eq":"beep"}],"min":1,"max":8,"step":1,"defaultValue":4},{"key":"frequency","type":"number","label":"Frequenz in Hz","conditions":[{"key":"type","eq":"tone"}],"min":0,"max":20000,"step":1,"defaultValue":200},{"key":"duration","type":"number","label":"Duration","unitsField":"units","unitsDefault":"time","conditions":[{"key":"type","in":["beep","crash","tone"]}],"min":0,"max":4.25,"step":0.01,"defaultValue":0.5},{"key":"wait","type":"checkbox","label":"Warten bis zum Ende","conditions":[{"key":"type","in":["beep","crash","tone"]}],"defaultValue":true,"flexBasis":"100%"},{"key":"effect","type":"number","label":"Effekt Index","min":0,"max":60,"defaultValue":0,"conditions":[{"key":"type","soundType":"fxhammer"}]}]} />

- **Sound-Effekte**  
- **Priorität**  
- **Tonhöhe**  
- **Frequenz in Hz**  
- **Duration**  
- **Warten bis zum Ende**  
- **Effekt Index**  

## Musik Routine setzen
Attach a script to one of the four music routines that can be triggered from a .uge file. In the music editor you are able to use the call routine effect in your songs to trigger these scripts in time to music.

**Referenzen**  
[/docs/assets/music/music-huge#effects](/docs/assets/music/music-huge#effects)<ScriptEventPreview title={"Musik Routine setzen"} fields={[{"key":"routine","label":"Routine","description":"The music routine, either 0, 1, 2 or 3.","type":"number","defaultValue":0,"min":0,"max":3},{"key":"__scriptTabs","type":"tabs","defaultValue":"trigger","values":{"trigger":"On Call"}},{"key":"true","label":"On Call","description":"The script to run when the routine is called.","type":"events","allowedContexts":["global","entity"],"conditions":[{"key":"__scriptTabs","in":[null,"trigger"]}]}]} />

- **Routine**: The music routine, either 0, 1, 2 or 3.  
- **On Call**: The script to run when the routine is called.  

## Musik: Anhalten
Stops any currently playing music.
<ScriptEventPreview title={"Musik: Anhalten"} fields={[{"label":"Stoppt die Musik, die zuvor abgespielt wurde."}]} />

