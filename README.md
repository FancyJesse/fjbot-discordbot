# FJBot-DiscordBot

[![Discord Chat](https://discordapp.com/api/guilds/361689774723170304/embed.png)](https://discord.gg/U5wDzWP8yD)
[![status](https://img.shields.io/badge/Project%20Status-inactive-inactive.svg)](#)
[![Documentation](https://readthedocs.org/projects/fjbot/badge/?version=latest)](https://fjbot.readthedocs.io/en/latest/)
[![Discordpy](https://img.shields.io/badge/discord-py-blue.svg)](https://github.com/Rapptz/discord.py)
[![Code Style: Black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/ambv/black)
[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=jesus_andrade45%40yahoo%2ecom&lc=US&item_name=GitHub%20Projects&currency_code=USD&bn=PP%2dDonationsBF%3abtn_donateCC_LG%2egif%3aNonHosted)

A Discord bot with focus on wrestling events and  [Matches](https://idleuser.com/projects/matches).

**My Discord Server:** [WatchWrestling](https://discord.gg/U5wDzWP8yD)


## Introduction

This Discord Bot was originally created back in 2017 to integrate [Matches](https://idleuser.com/projects/matches) into the server. This allows users to bet and rate matches, look up Superstar biographies, share gifs, and be alerted of upcomming wrestling events.

Originally, this bot ran through a single Python file. I had no idea that I would still be supporting the bot this long or even begin scaling it to include additonal features and commands. Because of the expansion of the bot, I decided to transition this Discord Bot project to use cogs. Made code management a whole lot easier.
Now I continue support on the bot as a hobby and development experience.


## Sample

Register an account
```console
!register
```

Get a login link via PM
```console
!login
```

Display current stats
```console
!stats
```

Display current leaderboard
```console
!top
```

Display Superstar/Wrestler's info
```console
!bio Alexa
```

Display current matches
```console
!matches
```

Bet on a match
```console
!bet 100 Brock
```

Display current bets
```console
!bets
```

> many more commands available.
> see the [documentation](https://fjbot.readthedocs.io/en/latest/)

##  Prerequisites (Development)

* Python 3
* MySQL
* Discord Server

## Setup & Deploy (Development)

Clone repository
```console
git clone https://github.com/idle-user/fjbot.git
```

Install requirements
```console
pip install discord.py[voice] mysqlclient youtube_dl tweepy m2r
```

Create config file. See [config.py](config.py)
```console
./fjbot/config.py
```

Run MySQL Database setup
*There are many tables, procedures, and triggers required to run accounts properly*
```console
# TODO
```

Run bot
```console
python3 bot.py
```


## Update History

2020-03-19
* Fixed prefix issue on PM
* Updated Start and End bot.py messages

<details>
    <summary>see more</summary>

2020-03-12
* Command name changes
* Formatting

2020-03-11
* Docstring and a lot of documentation
* Reconfigured config.py format
* Bug fixes

2020-03-06
* Updated config.py format
* Added option to change command prefix (multi-server support)
* Updated permission checks that required fixed values
* Moved event alerts from matches to scheduler cog
* Started FJBucks cog
* Updated README

2020-03-02
* Number formatting
* README overhaul coming soon

2020-01-17
* Fixed Scheduler COG
* Added support to Royal Rumble entry command

2020-01-06
* Added scheduler cog for routine alerts
* Fixed voice cog permissions for volume
* Updated config file formatting
* Removed weekly alerts from matches cog

2019-10-17
* Added AEW schedule
* Added chatango PM logging/display
* Removed Tweet tasks
* Fixes

2019-05-29
* Added basic logging
* Updated Match short-view text to include titles
* Fixed Mute and Unmute commands

2019-05-21
* Updated Matches command to display short view if too many
* Added current match command

2019-05-19
* Fixed User Register through Chatango
* Organized Chatang cog prints

2019-05-18
* Fixed User Match betting
* Fixed Match team searches

2019-05-17
* Added user register functionality
* Changed Discord message logging to prints (logging later)
* Added cooldown to Open Matches command
* Fixed betting command
* Fixed twitter cog
* Clean up

2019-05-16
* PEP 8 by using [Black](https://github.com/python/black/) - *bye-bye tabs ... :(*
* Code clean-up
* Still to be updated: twitter cog

2019-05-15
* Renamed fjbot.py to bot.py
* Updated admin commands
* Moved base user commands from matches cog to member cog
* Moved config.py to root
* Updated imports of all files
* Added a new error class for future use
* Removed unecessary log messages (moving to logging later)
* Added base royal rumble support
* Updated README structure and setup instructions
* Added 2019.05.14 updates because it mysteriously disappeared
* Still to be updated: twitter cog

2019-05-14
* Added voice cog (based on official example)
* Moved on_member_join to bot.py
* Added user reset password link command
* Updated command names and aliases
* Removed uneeded command based on rewrite

2019-05-13
* Complete rewrite in progress
* Superstar, DiscordUser, ChatangoUser, Match are now classes
* Complete overhaul of Database handling
* Database calls are now handled by the classes
* Updated function checks
* Renamed credentials.py to config.py
* Chatango Bot rewrite
* Update quickembed to support Class structures
* Cleaned up error handling
* Still be updated: twitter cog, voice cog

2019-05-06
* Complete update to comply with discord.py rewrite
* Bot messages are now embeded
* Removed cross-cog dependency
* Added quickembed.py to utils for quick embeded messages
* Commented out Tweepy unsupported calls (Repo does not support new Twitter API)
* Updated voice cog to search YouTube video by title or direct link
* Created a class for: Match, Superstar, Userstats
* Match and User classes can output their info in embed format
* Code cleanup

2019-02-05
* Added Voice cog (plays YouTube audio)
* Role checks are based only on IDs now
* Updated credential sample to include only IDs
* Added function for quick login for registered users
* Added a Discord Channel for Logging
* Added logging calls within project
* Twitter cog updated (functionality limited by latest Twitter API update)
* Updated query calls based on database table updates
* Various new functions added
* Text fixes

2018-10-14
* Added User class
* Updated cogs to use new User class
* Added direct PM to Discord Server owner function
* Updated admin cog checks
* Updated ch library with alterations (bugs found)
* Updated chatango cog to include match listings and betting
* Modifications to dbhandler to explicitly call queries
* Updated credentials to include Discord invite link
* Text fixes

2018-09-06
* Database redesign (to be included in repository)
* Various database optimization within dbhandler
* Created Class module for readability
* Removed \_\_obosolete__ directory
* Updated logging between cogs - all use main fjbot function now
* Added admin commands
* Heavily updated chatango cog
* Updated tweet log within twitter cog to use async functions
* Started progress on twitter cog to accept PMs
* Added additional checks
* Renamed wwe cog to matches
* Bug fixes

2018-06-24
* Updated database reference between cogs
* Added ch.py library used for the chatango.py cog
* Bug fixes

2018-06-10
* Bug fixes with cog communication

2018-06-09
* Transition to cog model

2018-06-08
* Initial introduction to GitHub

</details>

## License

This project is licensed under the GNU GPLv3 License - see the [LICENSE](LICENSE) file for details


## Authors

idle-user

