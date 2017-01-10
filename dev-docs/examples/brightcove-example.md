---
layout: player_example
title: Brightcove Player Integration
description: Show a prebid ad in a Brightcove player

top_nav_section: dev_docs
nav_section: quick-start

hide: true
beta: true

about:
- Using invokeVideoPlayer to set up and access the Brightcove player instance.
- Using bc() to make sure the player is loaded before playing an ad.
- Playing an ad using Brightcove's IMA3 plugin.
- Configuring the player's ima3 settings on page.

player_notes:
- For this demo we'll be configuring the player's ima3 settings on the page. Make sure you load the ima3 script and css file in addition to your player script.
- Don't enable ima3 in your player's Video Cloud settings. We'll be setting up ima3 on the page.

jsfiddle_link: jsfiddle.net/shirleylberry/dd4wd8z7/embedded/html/

code_lines: 137
code_height: 2950

pid: 32
---
<br>
<div markdown="1">
#### Line 4: Load the ima3 css file
Load the ima3 css file to ensure the ad displays correctly in the player.
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
<br><br>
<div markdown="1">
#### Line 74: Create video element
Create your video element. You can copy paste this from the embed code in Video Cloud. Add an id tag to your player so that we can get a reference to it later. 
</div>
<br><br>
<div markdown="1">
#### Line 74: Include player script
Link to the player script from Brightcove. This will also be part of the embed code provided by Video Cloud.
</div>
<div markdown="1">
#### Line 74: Include ima3 plugin script
Link to the ima3 plugin. Since we are not configuring the plugin in Video Cloud, we need to include this script on the page. 
</div>
<br>
<div markdown="1">
#### Line 74: Define invokeVideoPlayer
Redefine invokeVideoPlayer and pass in the vast url we got back from prebid. We'll ue this url in our ima3 plugin configuration.
</div>
<div markdown="1">
#### Line 74: Use bc to reference the video player
Redefine invokeVideoPlayer and pass in the vast url we got back from prebid. We'll ue this url in our ima3 plugin configuration.
</div>
<br><br><br>
<br><br><br>
<br><br><br>



