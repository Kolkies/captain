# Artemis

Artemis is my own personal take on a cross between GearBot and Rowboat. Of course, this bot is still in development and will be for a very long time.

## Features

You didn't come here to listen to me chatter about the unimportant stuff, you want the feature list, well here it is:
- Ban, unban, softban, kick, mute, unmute and warn commands
- Temporary muting, banning and lockdowns
- Purge in the current channel, a different channel, from a user or by bots
- Mod logging for actions, infractions, message edits/deletes and member joins/leaves
- A few handy utils like a bot invite generator and source command
- Auto role
- Anti spam and invite
- Very high configurability

## Planned features

Here's what you can look forward to by clicking the Watch button in the top right hand corner:
- Reminders
- Configurable strike system to punish users after x warnings
- Anti links and swearing
- Message archiving to save messages
- Starboards
- A web dashboard so that you don't have to restart to change a guild's config
- Custom commands

## Who can host this?

This isn't really the kind of thing your average Joe should be trying to run, especially if you have no clue about Python, Docker, Postgres or Redis. If you're one of those people but would really like an instance of Artemis, join the Discord server below (or contact me) and I'll either give you my instance or help you set one up.

## Can I use the official instance?

Yup! Though only for public servers since my hosting resources are limited. If you want to use the official instance (which means new features sooner and hosting is done for you), then contact me on Discord at JackTEK#1942. It might be easier to find me by joining [my Discord server](https://invite.gg/mila).

## Self-hosting Agreement

Another one of these? Wasn't Rowboat enough? I know, I know, but here me out, I'll try to be as lax as I can.
- You MAY NOT use the official instance's logo and name **at the same time** in *derivative* bots (forks or slightly modified instances)
- You MAY NOT host a public instance (so putting it onto bot list websites etc)
- You MAY NOT charge for usage of your instance
- You MAY allow a handful of servers (max of 15 please) to use your instance of Artemis

Of course, I can't force you to obey these rules, but not obeying them would be mean :(

## Running your own instance

So you want to run your own instance? I hope you know what you're doing. Here's what you'll need to get started:
- A PostgreSQL server
- A Redis server
- Docker on your host machine

### Deploying the bot

If you have setup everything above, you need to configure, build and run the bot, to do that follow the steps below.

#### Configuring the bot

First of, you'll **NEED** to go into the artemis folder and rename every .example.yml to just have .yml on the end (get rid of the .example). Then, you'll need to head into the config.yml and guilds.yml files to edit the settings, this might take a while.

#### Building the image

To build a Docker image of Artemis, cd into the repository and run the command below:
```
docker build . --tag artemis:latest
```

#### Running the image

Building might take a while, but once you're done, you can run Artemis by doing:
```
docker run -d --name artemis --network="host" artemis:latest
```

#### You're good to go

That's it, you've deployed your instance of Artemis. If you noticed any issues, including bugs or problems setting it up altogether, please file an issue over on the GitHub Repository or contact me on Discord (details are earlier in the readme).