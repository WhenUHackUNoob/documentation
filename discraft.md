# Discraft

Discraft is the newest and most advanced plugin to link your discord server to your Minecraft server, with built in report systems, punishment alerts,
both chat and console webhooks and more, Discraft is the best plugin to use when linking up your Minecraft and Discord server.

> ## Getting Started
First, find the configuration file. This is most likely found in the plugins/Discraft directory. Once ou are in the configuration file, you should be
greeted with something like this:
```yml
# Enter your discord link here.
discord-link: ""
```
If so, perfect! All of the sections in the configuration have little helpers above them, giving you all the info you need.

> ## Configuring
```yml
# Enter your discord link here.
discord-link: ""
```
Please enter your discord server invite here. This will be sent to people when they execute the discord command.

```yml
# Add all your webhooks here to start with the plugin!
webhooks:
  server-chat: ""
  server-console: ""
  report: ""
  punishments: ""
  avatar-url: ""
```
Add all your webhook links here. **Do NOT add webhook links in report if you do not have the built-in reports feature enabled, and do not add a**
**link to punishments if the plugin does not support your punishment system. The current supported plugins are: Litebans**. Insert the avatar URL link to the avatar url section. This can be an imgur link, or any other image delivery service.

```yml
# Set this to true to use the built in report system
enable-reports: true
```
This enables the built-in report feature. When this is enabled, Discraft can send alerts to your discord when a new report is submitted. We are
looking into creating an API for other plugins to support this feature in the future, but at the moment we can only use the built in report system.

```yml
# Set this to the language you want the plugin to use. If invalid, plugin will default to English.
language: "en_UK"
```
The language section is very self explanatory, change this to set the language of the plugin. This means all users will get messages in this language, not just admins. The current supported languages are **English (UK)**. To translate to any language, please message me on [Discord](https://discord.whenuhackunoob.com)