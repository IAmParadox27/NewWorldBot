# New World Discord Bot (Queue Simulator)

## Invite
https://discord.com/api/oauth2/authorize?client_id=894709991309733899&permissions=396210859088&scope=bot%20applications.commands

## Overview
The bot allows you to query the status of a particular New World server and get the current active players, queue time and whether it's accepting players for character creation.

Slash commands are taking priority at the moment - as such new features will only be provided using slash commands. Older features support both.

## Commands
The bot supports before prefix message commands and slash commands. The prefix is "!nw " (without quotes)

<h3>Create Pinned Message</h3>
<h4>!nw setpin [world name]</h4>
<h4>/createpin world: channel: should_pin:</h4>
This will create an auto-updating message which will display the status of the world you provide and pin it to the channel the message is sent to.

Currently the bot only supports 1 pinned post per discord server, but this is something I'm looking to rework to allow multiple posts. If this is run when a post already exists it will update the world that the already created message uses when it updates.

The bot must have permission to send messages in this channel.

The slash command asks what channel to post to and whether the message it posts should be pinned in that channel.

<h3>Set Personal World</h3>
<h4>!nw setdefault [world name]</h4>
<h4>/setworld world:</h4>
This will set the default world for you as a discord user and will allow you to run <b>!nw status</b> or <b>/status</b> without needing to provide a world.

<h3>Status</h3>
<h4>!nw status [world name (optional)]</h4>
<h4>/status world: (optional)</h4>
This will query the status of the provided world. If a world is not provided it requires the user to have run <b>!nw setdefault</b> or <b>/setworld</b> first.

<h3>Unpin and Remove Pinned Post</h3>
<h4>!nw unpin</h4>
<h4>/unpin</h4>
This will remove the posted message in the server its run in.

<h3>Pull Socials</h3>
<h4>/pullsocials channel:</h4>
This will post twitter posts from @PlayNewWorld into the channel provided. It will not post tweets that have already happened and will only post new ones. At the moment this does include replies so this may get cluttered. It was designed to allow people to see when server outages had been posted.

## Planned Features

At the moment there are lots of planned features. Mainly relating to things like in game stats being able to be seen within discord, but at current I've not found a way to do this, but it is actively being investigated.
