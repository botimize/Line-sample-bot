This sample-bot uses [linebot](https://github.com/boybundit/linebot) framework

## Documentation

- [Line Messaging API](https://devdocs.line.me/en/)

## Channel token

- To start [Messaging API](https://business.line.me/zh-hant/services/bot)

- Get Channel ID,Secret,Token [Document](https://developers.line.me/messaging-api/getting-started)

## Example
  
```js
var linebot = require('linebot');

var bot = linebot({
    channelId: CHANNEL_ID,
    channelSecret: CHANNEL_SECRET,
    channelAccessToken: CHANNEL_ACCESS_TOKEN
});

bot.on('message', function (event) {
    event.reply(event.message.text).then(function (data) {
        // success
    }).catch(function (error) {
        // error
    });
});

bot.listen('/linewebhook', 3000);
```

