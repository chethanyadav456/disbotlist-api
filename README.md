*NPM:** [npmjs.com/package/disbotlist](https://www.npmjs.com/package/disbotlist/)<br>

## Installation
*If you have trouble with the installation, please feel free to visit our [discord](https://discord.gg/c96hPfyWQd) address.*
- `npm i disbotlist`

```js
const disbot = require("disbotlist");
const dbl = new disbot("TOKEN-HERE", client);

client.on("ready", async () => {
  dbl.serverCount();
  // console.log("Server count posted")
  
  let hasVote = await dbl.hasVoted("845357509132550184");
  if(hasVote === true) {
    console.log("Voted")
  } else {
    console.log("Vote please.")
  }
  
  
  let search = await dbl.search("845357509132550184")
  console.log(search)
  /*
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
