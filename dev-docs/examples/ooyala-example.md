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

code_lines: 154
code_height: 3350

pid: 34
---
<br><br><br>
<br><br><br>
<br><br>
<div markdown="1">
#### Line 7 to 22: Load Player Scripts
Load the Ooyla player scripts you plan to use. You must load the core player script, the scripts for whatever video formats you want to support, and the scripts for the ad manager you want to use. The scripts themselves and a guide for choosing which ones you need can be found [here](http://help.ooyala.com/video-platform/documentation/concepts/pbv4_plugins.html).
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
<br>
<div markdown="1">
#### Line 126 to 140: Define player settings
Define the settings you want for your player in a JSON object. Most of these lines will be part of the embed code you copy paste from Ooyala Backlot.
</div>
<br>
<div markdown="1">
#### Line 132 to 137: Add the ad parameters to the player settings
Create a new JSON object in the player parameters. The key should be the ad manager you're using (in our case we're using the [Google ima ads manager](http://help.ooyala.com/video-platform/concepts/pbv4_ads_dev_google_ima.html), so the key is `"google-ima-ads-manager"`). The ima ads manager requires an ad set (which we've named `"all_ads"`. 
Make sure you follow proper [JSON formatting](http://www.w3schools.com/js/js_json_syntax.asp) as you add the ad parameters.
</div>
<br><br>
<div markdown="1">
#### Line 141 to 143: Initialize the player
Use the `OO.ready()` event to make sure that all the necessary Ooyala plugins have loaded before creating the player. Once it has, call `create()` and pass in the div you're creating the player in, the ID of the content video, and the player settings we created above.
</div>


