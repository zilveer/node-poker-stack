## node-poker-stack -- a node.js Texas Holdem game server and web client

node-poker-stack is a [node.js](http://nodejs.org) Texas Holdem game server and web client. Some notable features
are real-time game-play and chat, multiple game rooms, support up to 10 players per room with a combination
of human and bot players.

## Features

### Game Features

* Texas Holdem game engine for up to 10 players per room based on [node-poker](https://github.com/mjhbell/node-poker).
* Configure bots to join at intervals and play against humans or other bots. They will make use of a hand evaluator, and were very useful for debugging game logic.
* Multiple simultaneous game rooms with individual game rules (blinds, buyins, # of players, etc).
* Real-time game and chat interaction between clients via web sockets.
* Robust game records are stored which include each player action and along with game results.
* Rudimentary friend system to check whether friends are online, chat, and join their games.
* A basic web client server is available (node.js + backbone.js + websocket web browser client).

### Built Using Pomelo

* Real-time communication between server and client.
* Distributed architecture to scale painlessly.
* Pluggable architecture to easily add new features.
* SDKs for a variety of clients (javascript, flash, android, iOS, cocos2d-x, C).
* See [Pomelo Framework](http://github.com/NetEase/pomelo) for more information.

### Whats Missing?

* User and table data is persisted to file store rather than database.
* Web browser client could be improved (uses vanilla bootstrap.js).
* Add more client platforms (android, ios, phonegap, etc).

## Instructions

1. git clone https://github.com/zilveer/node-poker-stack.git
2. ./npm-install.sh
3. node game-server/app
4. open another terminal window
5. node web-server/app
6. go to http://localhost:3002 to access web client
7. register a new user and login
8. create a game room, join the game, and wait
9. bots will join the game to play

## Updated Install instructions
Ok. I got it to work. For anyone that's interested. heres the instructions how to run it(at least how I did it):
Before you begin uninstall all previous node.js or npm on system and even clear caches or delete node directory just to be safe.

    download latest node.js(for me its x64 windows so i downloaded 6.11.2) and install it on your system.
    clone project by typing
    git clone https://github.com/zilveer/node-poker-stack.git
    cd node-poker-stack:
    Install pomelo globally(on windows it installs to C:\Users[yourusername]\AppData\Roaming\npm\node_modules):
    npm install -g pomelo
    install game:
    sh npm-install.sh
    run webserver:
    node web-server/app
    open another bash and run game server:
    cd game-server
    pomelo start
    open web browser and load page:
    localhost:3002

9 If everything went well. try to register and user name and password and u will be able to login.

## License

(The MIT License)

Copyright (c) 2012-2014 Edward Yang

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
