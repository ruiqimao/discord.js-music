# Discord.js Music Plugin

Installation:
```bash
npm install discord.js-music
```

This is a music plugin for Discord.js. Using it is as easy as:
```javascript
const Client = require('discord.js').Client;
const music = require('discord.js-music');

const client = new Client();
music(client);

client.loginWithToken('< bot token here >');
```

The module consists of a single function, which takes two arguments:
```javascript
/*
 * Initialize the music plugin.
 *
 * @param client The Discord.js client.
 * @param options (Optional) A set of options to use:
 *                prefix: The prefix to use for the command (default '!').
 *                global: Whether to use the same queue for all servers
 *                        instead of server-specific queues (default false).
 *                maxQueueSize: The maximum queue size (default 20).
 */
music(client, options);
```

The commands available are:
* `play <url|search>`: Play a video/music. It can take a URL from various services (YouTube, Vimeo, YouKu, etc). If no URL is specified, the bot will search Google for the video.
* `skip [number]`: Skip some number of songs. Will skip 1 song if a number is not specified.
* `queue`: Display the current queue.
* `pause`: Pause music playback.
* `resume`: Resume music playback.
