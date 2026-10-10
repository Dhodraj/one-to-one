# one-to-one

A one-to-one video call in the browser. Each person gets an ID. One shares it, the other calls it. The video goes peer to peer over WebRTC with simple-peer, and a small Socket.IO server passes the call signals between the two.

Built in January 2022.

The signalling server used to run on Heroku. That server is gone, so the deployed front end no longer connects. Run both parts on your machine instead.

## Run it

```bash
cd backend
npm install
npm start            # Socket.IO server on port 5000

cd ../my-app
npm install
npm start
```

Before starting the front end, change the server address in `my-app/src/SocketContext.js` from the Heroku URL to `http://localhost:5000`.
