
# spacebotlist.js

# SpaceBotList api wrapper for node.js


**NPM:** [npmjs.com/package/vcodes.js](https://www.npmjs.com/package/spacebotlist.js)<br>

´
## Installation
*If you have trouble with the installation, please feel free to visit our [discord](https://spacebotlist.xyz/dc) address.*
- `npm i spacebotlist.js`

```js
const spacebotlist = require("vcodes.js");
const dbl = new spacebotlist("TOKEN-HERE", client);

client.on("ready", async () => {
  dbl.serverCount();
  // console.log("Server count posted")
  
  let hasVote = await dbl.hasVoted("800344695069999144");
  if(hasVote === true) {
    console.log("Voted")
  } else {
    console.log("Vote please.")
  }
  
  
  let search = await dbl.search("800344695069999144")
  console.log(search)
  /*
  {
    avatar: 'https://cdn.discordapp.com/avatars/800344695069999144/8d4499339467130069897e90d528b5b4.webp',
    botID: '800344695069999144',
    username: 'Fyso',
    discrim: '0507',
    shortDesc: 'Cool Bot',
    prefix: '.',
    votes: 2,
    ownerID: '715491864739840063',
    owner: 'SkyAlumny',
    coowners: [ '' ],
    tags: [ 'Moderation', 'Fun' ],
    longDesc: longDesc,
    certificate: 'Certified'
  }
  */
});
```

