# CustomClientBlocker

A simple plugin that kicks player using specific client brand

![Modrinth](https://img.shields.io/modrinth/dt/xsOXeDko?logo=modrinth&label=Modrinth)

## Installation

Download plugin at [Modrinth(Under review)](https://modrinth.com/plugin/custom-client-blocker) or [Releases](https://github.com/pikokr/CustomClientBlocker/releases) 

or, you can also download [snapshot builds](https://jenkins.paring.moe/job/Paper/job/CustomClientBlocker/)

## Usage

### Configuration

You can configure this plugin by editing `plugins/CustomClientBlocker/config.yml`

```yaml
# The list of clients to block
blacklist:
  - forge
# Kick message
kickMessage: Using %client% is not allowed!
```

### Commands

The base command is `/clientblocker` or `/ccb`

And base permission is `customclientblocker.command`

| Command | Description                                      | Permission                                                                     |
|---------|--------------------------------------------------|--------------------------------------------------------------------------------|
| players | Lists players, but the connected client is shown | `customclientblocker.command.players`                                          |
| list    | Lists which clients are blocked                  | `customclientblocker.command.list`                                             |
| block   | Adds an entry to client blacklist                | `customclientblocker.command.block` or `customclientblocker.command.modify`    |
| unblock | Removes an entry to client blacklist             | `customclientblocker.command.unblock`  or `customclientblocker.command.modify` |
| reload  | Reloads the setting from config file             | `customclientblocker.command.reload`                                           |

### Bypassing specific players

You can add an except by adding permission `customclientblocker.bypass` to a player
