MuseCat Help
---
Commands related to the Discord bot MuseCat and how to use them.
<br>
<br>

Content
---
- [Moderation](#moderation)
  - [Clear](#clear)
  - [Mute](#mute)
  - [Kick](#kick)
  - [Ban](#ban)
  - [Announce](#announce)
  - [Channel](#channel)
    - [Channel Lockdown](#channel-lockdown)
    - [Channel Hide](#channel-hide)
  - [NSFW Ban](#nsfwban)
  - [New Emoji Role](#newemojirole)
  - [Warning](#warnings)
    - [warnings add](#warnings-add)
    - [warnings lookup user](#warnings-lookup-user)
    - [warnings lookup id](#warnings-lookup-id)
    - [warnings remove specific](#warnings-remove-specific)
    - [Full Pardon](#fullpardon)
  - [Filter](#filter)
    - [filter word add](#filter-word-add)
    - [filter word remove](#filter-word-remove)
    - [filter word list](#filter-word-list)
  - [Settings](#settings)
    - [settings logchannel](#settings-logchannel)
    - [settings joinchannel](#settings-joinchannel)
    - [settings announceupdate](#settings-announceupdate)
    - [settings allow_nsfw](#settings-allow_nsfw)
  - [Autorole](#autorole)
    - [Autorole add](#autorole-add)
    - [Autorole remove](#autorole-remove)
    - [Autorole list](#autorole-list)
- [Other](#other)
  - [Motd](#motd)
  - [Feedback](#feedback)
  - [Eightball](#eightball)
  - [Ping](#ping)
  - [Who Is](#whois)
  - [Spotify](#spotify)
  - [Server Info](#serverinfo)
  - [About](#about)
  - [NSFW Commands](#nsfwcommands)
    - [NSFW Sexuality](#nsfwsexuality)
    - [Art Search](#artsearch)
<br>
<br>
<br>


### Moderation
---
### Clear

**Description**: Quickly clears a given message amount
<br>
<br>
**Context**:
/clear [`(amount to clear)`]
<br>
**Example**: /clear `5`

**Permissions required**: `manage messages`
<br>
<br>
<br>
### Mute

**Description**: Mutes a given member for a specified amount of time
<br>
<br>
**Context**:
/mute [`user`], optional: [`time`]
<br>
**Example**: /mute `Wumpus`, `1day`
> **Note**: Doing this command to a already muted member will unmute the member
<br>
<br>
**Note**: If no mute time is specified, then the user will remain muted until the mute is removed by a moderator

**Permissions required**: `manage messages`
<br>
<br>
<br>
### Kick

**Description**: Removed a member from the server without banning them
<br>
<br>
**Context**:
/kick [`user`], [`reason`]
<br>
**Example**: /kick `Wumpus`, `Spamming chat`

**Permissions required**: `Kick Members`
<br>
<br>
<br>

### Ban

**Description**: Permanently removed a given member from the server
<br>
<br>
**Context**:
/ban [`user`], [`reason`], optional: [`Amount of days to delete users messages`]


**Permissions required**: `manage messages`
<br>
<br>
<br>

### Announce

**Description**: Generate a message embed and posts as an announcment

> This command has not yet been ported to SLASH, for now the command can be triggered by directly @ mentioning the bot in chat like `@musecat announce`

<br>
<br>

**Context**:
@mention `announce`
<br>
**Example**: @mention `announce`

**Permissions required**: `manage messages`
<br>
<br>
<br>

## CHANNEL
Parent for all channel related commands
<br>
<br>

### **Channel Lockdown**
**Description**: Makes a channel read-only for anyone with the @everyone role
<br>
<br>
**Context**:
/channel lockdown [`channel`]
<br>
**Example**: /channel lockdown `#general`
> **Note**: To undo a lockdown, just run the command again

**Permissions required**: `Manage Channels`
<br>
<br>
<br>

### Channel Hide

**Description**: Hides a channel from anyone with the @everyone role
<br>
<br>
**Context**:
/channel hide [`channel`]
<br>
**Example**: /channel hide `#general`
> **Note**: To show a channel again, just re-run the command

**Permissions required**: `Manage Channels`
<br>
<br>
<br>

### Nsfwban

**Description**: Bans someone from using NSFW commands
<br>
<br>
**Context**:
/nsfwban [`user`], list-required: [`enabled`, `disabled`]
<br>
<br>
**Example**: /nsfwban `Wumpus`, `Disabled`
<br>
> Enabled: User is allowed to use NSFW commands
>
> Disabled: User is not allowed to use NSFW commands


**Permissions required**: `Manage Messages`

**Note**: This command will not show unless inside of a NSFW channel. This is to prevent users from using the command outside of NSFW channels.
<br>
<br>
<br>

### NewEmojiRole

**Description**: Adds a new click-to-add emoji to the current channel
<br>
<br>
**Context**:
/newemojirole [`emoji`], [`Role`], [`message`], [`Channel`]
<br>
**Example**: /newemojirole `🤔`, `@muted`, You played yourself, #general

**Permissions required**: `manage roles`
<br>
<br>
<br>

### Warnings
---

### warnings add

**Description**: Warns a given member
<br>
<br>
**Context**:
/warnings add [`member`] [optional: `dm_member: yes/no`]
<br>
**Example**: /warnings add `Wumpus` `yes`
> **Note**: After running a command, Discord will give a paragraph popup where you can type the reason of the warning.

**Permissions required**: `moderate members`
<br>
<br>
<br>

### warnings lookup user

**Description**: Sends a list of all warnings a user has to the moderator log channel
<br>
<br>
**Context**:
/warnings lookup user [`user`]
<br>
**Example**: /warnings lookup user `Wumpus`

**Permissions required**: `moderate members`
<br>
<br>
<br>

### warnings lookup id

**Description**: Finds information on a specific warning on a user by ID
<br>
<br>
**Context**:
/warnings lookup id [`id`]
<br>
**Example**: /warnings lookup id `1234567`


**Permissions required**: `manage messages`
<br>
<br>
<br>

### warnings remove specific

**Description**: Removes a specific warning from a given user
<br>
<br>
**Context**:
/warnings remove specific [`id`]

**Permissions required**: `manage messages`
<br>
<br>
<br>

### FullPardon

**Description**: Removes all warnings from a given user
<br>
<br>
**Context**:
/fullpardon [`user`]
<br>
**Example**: /fullpardon `Wumpus`

**Permissions required**: `manage messages`
<br>
<br>
<br>

## Filter

### filter word add

**Description**: Adds a word to the message word filter
<br>
<br>
**Context**:
/filter word add [`word`], Rating: list-required [`Minor`, `Moderate`, `Severe`]
<br>
**Example**: /filter word add `dynobot`, `Minor`

**Permissions required**: `manage messages`
<br>
<br>
<br>

### filter word remove

**Description**: Removes a word from the message filter
<br>
<br>
**Context**:
/filter word remove [`word`]


**Permissions required**: `manage messages`
<br>
<br>
<br>

### filter word list

**Description**: Generated a entire list of filtered words
<br>
<br>
**Context**:
/filter word list
<br>
**Example**: /filter word list

**Permissions required**: `manage messages`
<br>
<br>
<br>

## settings
---

### settings logchannel

**Description**: Updates the channel moderation logs are sent to, message edits, and so on
<br>
<br>
**Context**:
/settings logchannel [`channel`]
<br>
**Example**: /settings logchannel `#General`

**Permissions required**: `manage server`
<br>
<br>
<br>

### settings joinchannel

**Description**: Updates the channel new joins/leaves are posted
<br>
<br>
**Context**:
/settings joinchannel [`channel`]
<br>
**Example**: /settings joinchannel `#general`

**Permissions required**: `manage server`
<br>
<br>
<br>

### settings AnnounceUpdate

**Description**: Updates fallback channel for announcments
<br>
<br>
**Context**:
/settings announceupdate [`channel`]
<br>
**Example**: /settings announceupdate `#general`

**Permissions required**: `manage guild`
<br>
<br>
<br>

### settings allow_nsfw

**Description**: Enabled and disabled all NSFW commands on the server
<br>
<br>
**Context**:
/settings allow_nsfw [choice: list-required [`enabled`, `disabled`]]
<br>

**Permissions required**: `manage server`

> Note: by default, NSFW commands are disabled

<br>
<br>
<br>

## Autorole

### Autorole add

**Description**: Adds a role to the list of roles given to users on join
<br>
<br>
**Context**:
/autorole add [`role`]
<br>
**Example**: /autorole add `@users`


**Permissions required**: `manage roles`
<br>
<br>
<br>

### autorole remove

**Description**: Removes an role from Autorole list
<br>
<br>
**Context**:
/autorole remove [`role`]
<br>
**Example**: /autorole remove `@users`

**Permissions required**: `manage roles`
<br>
<br>
<br>

### autorole list

**Description**: Generates a list of all roles given to users on join
<br>
<br>
**Context**:
/allautoroles
<br>

**Permissions required**: `None`
> Note: Anyone can do this command due to users being able to know what roles are in autorole by just clicking on a new members profile and looking at "roles"
<br>
<br>
<br>


### Other
---
### Motd

**Description**: Shows the bot's message of the days and general announcements
<br>
<br>
**Context**:
/motd
<br>
**Example**: /motd

**Permissions required**: `None`
<br>
<br>
<br>


### Feedback

**Description**: Provides feedback about the current state about the bot
<br>
<br>
**Context**:
/feedback
<br>
**Example**: /feedback
> **Note**: This will open a popup inside of Discord with three boxes asking you to type text on your feedback. This may require a update to your Discord client.

**Permissions required**: `None`
<br>
<br>
<br>

### About

**Description**: Fetches information on the bot
<br>
<br>
**Context**:
/about
<br>
**Example**: /about

**Permissions required**: `None`
<br>
<br>
<br>


### ServerInfo

**Description**: Fetches a lot of information on the current server
<br>
<br>
**Context**:
/serverinfo
<br>
**Example**: /serverinfo

**Permissions required**: `None`
<br>
<br>
<br>

### Spotify

**Description**: Fetches information about what a user is listening to on Spotify
<br>
<br>
**Context**:
/spotify [`user`]
<br>
**Example**: /spotify `Wumpus`

**Permissions required**: `None`
<br>
<br>
<br>

### WhoIs

**Description**: Fetches information on a given user
<br>
<br>
**Context**:
/whois [`user`]
<br>
**Example**: /whois `Wumpus`

**Permissions required**: `None`
<br>
<br>
<br>

### Ping

**Description**: Makes sure the bot is online, and fetches ping to Discord's server
<br>
<br>
**Context**:
/ping
<br>
**Example**: /ping

**Permissions required**: `None`
<br>
<br>
<br>


### Eightball

**Description**: Asks a eightball a question
<br>
<br>
**Context**:
/eightball [`question`]
<br>

**Permissions required**: `None`
<br>
<br>
<br>

### NSFWCommands
---

### NsfwSexuality

**Description**: Specifies what type of results you want on NSFW commands
<br>
<br>
**Context**:
/nsfwsexuality [preference: list-required: [`Any`, `Hetrosexual`, `Homosexual`, `Lesbian`]]
<br>
**Example**: /nsfwsexuality `Any`
**note**: This command will not show unless inside of a NSFW channel. This is to prevent users from using the command outside of NSFW channels.

**Permissions required**: `None`
<br>
<br>
<br>

### ArtSearch

**Description**: Searches either E621 or E926 for images.
<br>
<br>
**Context**:
/artsearch website: list-required[`e621`, `e926`], optinal: [`search term`]
<br>
**Example**: /artsearch `e621`, `fox -chicken`
**note**: This command will not show unless inside of a NSFW channel. This is to prevent users from using the command outside of NSFW channels.

**Permissions required**: `None`

> Note: By default, NSFW commands are disabled. You can enable them. For more information refer to [NSFW Update](#nsfwupdate).
<br>
<br>
<br>
