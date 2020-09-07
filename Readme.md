# Discord.js

discord.js is a powerful Node.js module that allows you to easily interact with the Discord API.

- Object-oriented
Steps to create bot :

- [ ] Configuring `dotenv`
- [ ] import Class from `Discord.js`
  - `Client` and `WebhookClient` classes
- [ ] Creating object Instance of classes
  - `Client` with Partials: `MESSAGE`, `REACTION`
  - `WebhookClient` with `WEBHOOK_ID` and `WEBHOOK_TOKEN`
- [ ] Creating Prefix variable
- [ ] Checking Events using `on()` based on following properties:
  - `ready` on login
    - [ ] `${client.user.tag}` for successfully login
    - [ ] Check for `message.content` startsWith given Prefix
    - [ ] Read the Message content `message.content` for command and store in a spread variable `[CMD_NAME, ...args]`
        - [ ] Perform following operation on content:
            - `trim` for spaces
            - `split` for list of args
            - `substring` with `Prefix.length`
      
      - [ ] if command is to `KICK` i.e., `if (CMD_NAME === 'kick')` then
        1. Check if member has permission `KICK_MEMBERS` to perform `KICK`
        2. Check if command is empty i.e,`args.length===0`.
        3. Get members for channel from CMD_NAME[0] store in cache `const member = message.guild.members.cache.get(args[0])`
            - Perform `KICK` `then` send 'kicked' on error `catch` 'Cannot kick user'.
        4. If not members found return `no member found`.

      - [ ] if Command is to Ban user `else if (CMD_NAME === 'ban')`
        1. check for `hasPermission` for member to Ban
        2. check if command given is empty
        3. Get the permitted member then Ban
            - if error catches 'An error occurred. Either I do not have permissions or the user was not found'
      - [ ] else if (CMD_NAME === 'announce')
  - [ ] `message`
    - [ ] if `author is bot` return
    - [ ] if 
  - [ ] Adding reaction to message `messageReactionAdd`
  - [ ] Removing message reaction `messageReactionRemove`
- [ ] Login with DISCORD_BOT_TOKEN



##### Made with ♥ by <a href="https://github.com/punitkmryh">punitDev</a>
[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://github.com/punitkmryh)
