*NPM:** [npmjs.com/package/disbotlist](https://www.npmjs.com/package/disbotlist/)<br>

## Installation
*If you have trouble with the installation, please feel free to visit our [discord](https://discord.gg/c96hPfyWQd) address.*
- `npm i disbotlist`

#### 1. Where can I get DisBotList.xyz api?
  Ans: [JavaScript](https://www.npmjs.com/package/disbotlist)
            [Python](https://pypi.org/project/disbotlist/)

#### 2. How do I install it?
  Ans: JavaSciprt: npm i disbotlist or npm install disbotlist
            Python: pip install disbotlist

#### 3. Does it have any GitHub Repository?
  Ans: Yes It Is [Here](https://github.com/disbotlist-xyz/disbotlist-api)

#### 4. What is it's uses?
  Ans: To get the daily vote count, server count and information about your bot.
Examples:  avatar, botID, discriminator, shortDescription, prefix, votes, serverCount, ownerID, owner, co-owners, tags, longDescription, certificate etc.

#### 5. How can I get my bot's server count?
  `Ans: JavaScript:`
```const disbot = require("disbotlist");
const dbl = new disbot("TOKEN-HERE", client);

client.on("ready", async () => {
  dbl.serverCount();
  console.log("Server count posted")
```
  ### Python: 
```from disbotlist import disbotlist
from discord.ext import commands

client = commands.Bot(command_prefix="!") 
dbl = disbotlist(client,"token of disbotlist")

@client.event
async def on_ready():
  x = await dbl.serverCountPost()
  print(x)

client.run("token") 
```

#### 6. How can I get my bot's vote count?
  `Ans:`
```let hasVote = await dbl.hasVoted("Your-bot-id");
  if(hasVote === true) {
    console.log("Voted")
  } else {
    console.log("Vote please.")
  }
  
  
  let search = await dbl.search("Your-bot-id")
  console.log(search)
```

#### 7. Full Example?
  `Ans:`
```const disbot = require("disbotlist");
const dbl = new disbot("TOKEN-HERE", client);

client.on("ready", async () => {
  dbl.serverCount();
  console.log("Server count posted")
  
  let hasVote = await dbl.hasVoted("your-bot-id");
  if(hasVote === true) {
    console.log("Voted")
  } else {
    console.log("Vote please.")
  }
  
  
  let search = await dbl.search("Your-bot-id")
  console.log(search)

  /* SearchResults
  {
    avatar: '',
    botID: '',
    username: '',
    discrim: '',
    shortDesc: '',
    prefix: '! [changable]',
    votes: 31,
    ownerID: '',
    owner: '',
    coowners: [ '' ],
    tags: [ 'Moderation', 'NSFW', 'Music' ],
    longDesc: longDesc,
    certificate: 'Certified'
  }
  */
});
```
