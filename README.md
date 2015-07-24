# squealing-octo-hockeypuck
We don't even know what we're doing.

## Brain Dump Initiative (thanks Jeff for pointing out my oversight) (thanks for the spellcheck Rob)
- bracket generation
- generate brackets based on "weights" (who you lose more often to, rarely played, march madness, etc)
  - generate a bracket ends registration, allows new sign ups
- challenge callout
  - notifications
- annonymous login, guest
- random name generation for guest accounts, or everyone!
- tournament sign up
  - cut off time
  - remove sign up
- gravatar sign in for avatar
- titles/rankings/achievements for levels of winning (King, Master, Corgilobster, The Button Masher)
- Store data in a database (mongodb?)
- keep track of tournament records
  - who they use
  - win/loss
  - win loss to (the character and the real life human being)
  - tournament status, outcome
- maintain user statistics
  - historical ish (title and date)
- voting system? for seeds? forum page
  - choose game to play
- don't do weekly tournaments, instead provide a calendar for events
  - signup for future events
- depending on record against another user, provide a handicap
- feed on home page, updating with tournament events
- MAKE IT MODULAR (cannot work for xbox darts, because Robert owns that game, no one should even play if he is)
- quick setup (heroku, digital ocean, raspberry pi, rackspace, etc.) (phase II)
- slack integration
- actions? <person> taunts <person>
- tournament of champions
- interface for adding players, etc to the database
- allow for tournaments
- analytics

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
- Wins and Losses
  - Data: [User.UUID, Game.Title, Character.UUID, Wins, Losses]
