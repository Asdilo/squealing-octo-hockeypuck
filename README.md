# squealing-octo-hockeypuck
![](./squealing-octo-hockeypuck.png)

We don't even know what we're doing.

## Technology

Below is a list of technologies we're using for `squealing-octo-hockeypuck`.

- Raspberry Pi
- MongoDB, Expressjs, Angular, Node.js (MEAN) stack
- [ZenHub](https://www.zenhub.io/)

## Features

Below is a list of milestones for the dashboard. These are intended to be
manageable chunks of work that can be done in at least a two hour span of work
among several developers. To find more information about these features, check
out the "Milestones" section in Issues.

- Development Setup
- User management
- Match management
- Bracket generation
- Tournament management

## Schemas
Question marks (?) denote a boolean value.
Brackets ([]) denote an array of values.
Braces ({}) denote a key value-map.

- User
  - Data: [Name, Nickname, Title, Achievement, UUID]
  - Has: {Game Character - Times played}
- Game Character
  - Data: [Name, UUID]
- Tournament Event
  - Data: [Date, Winner, User, Voting, Bracket, UUID, Game UUID, Team?, Challenge?]
  - Has: [Match]
  - Part of: [Calendar]
- Match
  - Data: [User, User, Game Character, Game Character, Winner, Loser, UUID, Time]
- Calendar
  - Has: [Tournament Event, Location]
- Game
  - Data: [Title, Game Character, Description, URL, UUID]
- Record
  - Data: [User.UUID, Game.Title, Character.UUID, Wins, Losses]
