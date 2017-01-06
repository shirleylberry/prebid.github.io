---
layout: player_example
title: Ooyala Player Integration
description: Show a prebid ad in an Ooyala player

top_nav_section: dev_docs
nav_section: quick-start

hide: true
beta: true

about:
- Using the Ooyala v4 player API.
- Using Ooyala's Google IMA plugin.
- Passing a vast tag to the Ooyala player.

player_notes:
- This guide uses the V4 Ooyala player. To get the embed code for the V4 player, select <b>New Ooyala Played (V4) Embed Code</b> in the embed options instead of HTML Embed Code. 
- Do not select an ad set in the 'Monetize' tab. We'll control that setting on the page.

jsfiddle_link: jsfiddle.net/shirleylberry/hxzue5eu/embedded/html/

code_lines: 156
code_height: 3350

pid: 34
---
<br><br><br>
<br><br><br>
<br><br>
<div markdown="1">
#### Line 7 to 22: Load Player Scripts
Load the Ooyla player scripts you plan to use. You must load the core player script, and the scripts for whatever video formats you want to support. The scripts themselvs and a guide for choosing which ones you need can be found [here](http://help.ooyala.com/video-platform/documentation/concepts/pbv4_plugins.html).
</div>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br>
<div markdown="1">
#### Line 126 to 140: Define player settings
Define the settings you want for your player in a JSON object. This object will be part of the embed code you copy paste from Ooyala Backlot.
</div>
<br>
<div markdown="1">
#### Line 132 to 137: Add the ad paramters to the player settings
Create a new JSON object in the player parameters. The key should be the ads plugin. 
Make sure you follow correct [JSON formatting](http://www.w3schools.com/js/js_json_syntax.asp) as you add the ad parameters.
</div>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<div markdown="1">
#### Line 130: Initialize the player
Get a reference to the player by calling `videojs()` and passing in your player's ID. Set its `src` to the content video you want to play.
</div>
<br>
<div markdown="1">
#### Line 136 to 138: Play the ad
Once the player's IMA3 plugin has loaded, use the plugin to play an ad as a preroll by calling `adrequest()` and passing in the url from prebid.
</div>


