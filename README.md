# Youtube Playlist Summary

![Travis](https://img.shields.io/travis/alincode/youtube-playlist-summary.svg)
![GitHub package version](https://img.shields.io/github/package-json/v/badges/shields.svg)
[![](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Dependency Status](https://img.shields.io/david/alincode/youtube-playlist-summary.svg?style=flat)](https://david-dm.org/alincode/youtube-playlist-summary)
![node version](https://img.shields.io/node/v/youtube-playlist-summary.svg)
<!-- ![npm downloads](https://img.shields.io/npm/dm/youtube-playlist-summary.svg) -->

<p align="center">
it could help you easy to get all playlist informations.
</p>

### Requirements

* node 8.x.x
### Install

```
$ npm install --save youtube-playlist-summary
```

### Usage

* [How to Get YouTube API Key - Easy way - YouTube](https://www.youtube.com/watch?v=_U_VS12uu-o)

```js
const PlaylistSummary = require('youtube-playlist-summary');
const config = {
    "GOOOGLE_API_KEY": "YOUR_GOOOGLE_API_KEY"
};

const ps = new PlaylistSummary(config);
const CHANNEL_ID = 'UCQCaS3atWyNHEy5PkDXdpNg';
const PLAY_LIST_ID = 'PL9f8_QifuTL4CS8-OyA-4WADhkddOnRS4';

ps.getPlaylistItems(PLAY_LIST_ID).then(result => {
  console.log(result);
}).catch(error => {
  console.error(error);
});

ps.getPlaylists(CHANNEL_ID).then(result => {
  console.log(result);
}).catch(error => {
  console.error(error);
});

ps.getSummary(CHANNEL_ID).then(result => {
  console.log(result);
}).catch(error => {
  console.error(error);
});
```

## License

[MIT](LICENSE)