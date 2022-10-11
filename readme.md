MuseCat Help
---
Commands related to the Discord bot MuseCat and how to use them.
<br>
<br>

Content
---
- [Other](#other)
  - [Motd](#motd) (Message of The Day)
  - [Feedback](#feedback)
  - [Eightball](#eightball)
  - [Ping](#ping)
  - [Who Is](#whois)
  - [Spotify](#spotify)
  - [Server Info](#serverinfo)
  - [About](#clear)
  - [NSFW Commands](#nsfwcommands)
    - [NSFW sexuality](#nsfwsexuality)
    - [Art Search](#artsearch)
- [Moderation](#moderation)
  - [Clear](#clear)
  - [Mute](#mute)
  - [Kick](#kick)
  - [Ban](#ban)
  - [Announce](#announce)
  - [Lockdown Channel](#lockdownchannel)
  - [Hide Channel](#hidechannel)
  - [NSFW Ban](#nsfwban)
  - [New Emoji Role](#newemojirole)
  - [Warning](#warningsection)
    - [Warn](#warn)
    - [Warnings](#warnings)
    - [Warning ID](#warningid)
    - [Pardon](#pardon)
    - [Full Pardon](#fullpardon)
  - [Add Bad Word](#addbadword)
  - [Remove Bad Word](#removebadword)
  - [All Filtered Words](#allfilteredwords)
  - [Config](#config)
    - [Log Update](#logupdate)
    - [Join Channel](#joinchannel)
    - [Announce Update](#announceupdate)
    - [NSFW Update](#nsfwupdate)
    - [Add Auto Role](#addautorole)
    - [Remove Auto Role](#removeautorole)
    - [All Auto Roles](#allautoroles)
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

### LockdownChannel

**Description**: Makes a channel read-only for anyone with the @everyone role
<br>
<br>
**Context**:
/lockdownchannel [`channel`]
<br>
**Example**: /lockdownchannel `#general`
> **Note**: To undo a lockdown, just run the command again

**Permissions required**: `Manage Channels`
<br>
<br>
<br>

### HideChannel

**Description**: Hides a channel from anyone with the @everyone role
<br>
<br>
**Context**:
/hidechannel [`channel`]
<br>
**Example**: /hidechannel `#general`
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

### WarningSection
---

### Warn

**Description**: Warns a given member without notifying them
<br>
<br>
**Context**:
/warn [`user`]
<br>
**Example**: /warn `Wumpus`
> **Note**: After running a command, Discord will give a paragraph popup where you can type the reason of the warning. On mobile devices this may require an update for your mobile app.

**Permissions required**: `moderate members`
<br>
<br>
<br>

### Warnings

**Description**: Sends a list of all warnings a user has to the moderator log channel
<br>
<br>
**Context**:
/warnings [`user`]
<br>
**Example**: /warnings `Wumpus`

**Permissions required**: `moderate members`
<br>
<br>
<br>

### WarningID

**Description**: Finds information on a specific warning on a user by ID
<br>
<br>
**Context**:
/warningid [`id`]
<br>
**Example**: /warningid `1234567`


**Permissions required**: `manage messages`
<br>
<br>
<br>

### Pardon

**Description**: Removes a specific warning from a given user
<br>
<br>
**Context**:
/pardon [`id`]

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

### AddBadWord

**Description**: Adds a word to the message word filter
<br>
<br>
**Context**:
/addbadword [`word`], Rating: list-required [`Minor`, `Moderate`, `Severe`]
<br>
**Example**: /addbadword `dynobot`, `Minor`

**Permissions required**: `manage messages`
<br>
<br>
<br>

### RemoveBadWord

**Description**: Removes a word from the message filter
<br>
<br>
**Context**:
/removebadword [`word`]


**Permissions required**: `manage messages`
<br>
<br>
<br>

### AllFilteredWords

**Description**: Generated a entire list of filtered words
<br>
<br>
**Context**:
/allfilteredwords
<br>
**Example**: /allfilteredwords

**Permissions required**: `manage messages`
<br>
<br>
<br>

### Config
---

### LogUpdate

**Description**: Updates the channel moderation logs are sent to, message edits, and so on
<br>
<br>
**Context**:
/logupdate [`channel`]
<br>
**Example**: /logupdate `#General`

**Permissions required**: `manage server`
<br>
<br>
<br>

### JoinChannel

**Description**: Updates the channel new joins/leaves are posted
<br>
<br>
**Context**:
/joinchannel [`channel`]
<br>
**Example**: /joinchannel `#general`

**Permissions required**: `manage server`
<br>
<br>
<br>

### AnnounceUpdate

**Description**: Updates fallback channel for announcments
<br>
<br>
**Context**:
/announceupdate [`channel`]
<br>
**Example**: /announceupdate `#general`

**Permissions required**: `manage guild`
<br>
<br>
<br>

### NsfwUpdate

**Description**: Enabled and disabled all NSFW commands on the server
<br>
<br>
**Context**:
/nsfwupdate [choice: list-required [`enabled`, `disabled`]]
<br>

**Permissions required**: `manage server`

> Note: by default, NSFW commands are disabled

<br>
<br>
<br>

### AddAutoRole

**Description**: Gives a role to members when they join
<br>
<br>
**Context**:
/addautorole [`role`]
<br>
**Example**: /addautorole `@users`


**Permissions required**: `manage roles`
<br>
<br>
<br>

### RemoveAutoRole

**Description**: Removes an role from Autorole
<br>
<br>
**Context**:
/removeautorole [`role`]
<br>
**Example**: /removeautorole `@users`

**Permissions required**: `manage roles`
<br>
<br>
<br>

### AllAutoRoles

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

**Permissions required**: `None`

> Note: By default, NSFW commands are disabled. You can enable them. For more information refer to [NSFW Update](#nsfwupdate).
<br>
<br>
<br>
