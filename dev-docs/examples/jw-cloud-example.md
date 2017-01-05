---
layout: player_example
title: JW Cloud Player Integration
description: Show a prebid ad in a cloud hosted JW Player

top_nav_section: dev_docs
nav_section: quick-start

hide: true
beta: true

about:
- Setting up JW Player to dynamically play ads.
- Using a cloud-hosted JW player.
- Using invokeVideoPlayer to set up and access the JW Player instance.
- Dynamically inserting a preroll ad into JW Player.

player_notes:
- You must have the correct JW Player license that allows you to play advertising.
- The different methods of embedding JW Player on your site can be found <a href="https://support.jwplayer.com/customer/portal/articles/1406723-mp4-video-embed">here</a>. 
- For this example we will be using method 1, a cloud-hosted player and JW Platform hosted content. To see an example using the self-hosted player, click <a href="#">here</a>.
- No matter what embedding method you choose to use, you must follow the <b>custom embed</b> instructions. You cannot use the single-line embed.
- If you're using a cloud-hosted player, <b>do not enable advertising in the platform</b>. We'll do it on page so that we can use the vast url from prebid.
- You can set up most of your player's settings in the platform. The platform settings will be used unless overridden on the page in the setup call.

jsfiddle_link: jsfiddle.net/shirleylberry/zt70zj9z/embedded/html/

code_lines: 142
code_height: 3000

pid: 20
---
<br><br><br>
<br><br><br>
<br><br><br>
<!-- <div markdown="1">
#### Line 12 to 15: Pre-define invokeVideoPlayer
invokeVideoPlayer is called when all the bids are returned from prebid. Defining invokeVideoPlayer at the start of the page ensures that this function will always be defined, and we will always be storing the url of the vast tag, regardless of the timing of the rest of the page. 
</div> -->
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
<!-- <div markdown="1">
#### Line 74: Call invokeVideoPlayer
Once all the bids are back, call invokeVideoPlayer and pass in the url. This will either store the url in the variable tempTag, or pass it to the video player.
</div> -->
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
<div markdown="1">
#### Line 113: Include the player library
The script tag for your cloud-hosted video player can be found in your JW Platform account on the player's page, under 'Cloud Player Library URL'. The player will use the settings you define in JW Platform unless you override them on the page in the setup call.
</div>
<div markdown="1">
#### Line 115: Get a reference to the player instance
Get a reference to the player by calling `jwplayer()` and passing in the id of the div you want to load the player into.
</div>
<div markdown="1">
#### Line 118 to 123: Call setup on the player instance
Call `setup()` on the player instance with the settings you want. We need to pass in a media file and an advertising block with a `client` defined.
</div>
<div markdown="1">
#### Line 120 to 122: Pass in Advertising
We must pass in an `"advertising"` block in our settings in order to enable advertising for this player. We can also specify the tag or an ad schedule here but for this demo we'll insert the tag dynamically before the content plays.
</div>
<div markdown="1">
#### Line 125 to 127: Play a prebid ad as a preroll
Before the player begins to play the content video, play an ad.
</div>


