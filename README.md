When we were kids, we used to play Dots & Boxes game in school. It's still a popular game in school : https://en.wikipedia.org/wiki/Dots_and_Boxes

This is that game made online. It's an online multiplayer implementation of Dots-and-Boxes !

Built with VueJS, d3.js, [P2PT](//github.com/subins2000/p2pt). Uses WebTorrent trackers for making Peer-to-Peer connections for multiplayer.

## Build Setup

```
npm i
npm run dev
```

Trackers list is included in `src/components/Game.vue`. You may want to change that or add your own [local tracker](https://github.com/subins2000/p2pt/blob/master/start-tracker.js) for development.