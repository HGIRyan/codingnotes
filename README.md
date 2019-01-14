# -This Is My Coding Notes Repo-
## Problems & Solutions
* While Hosting and trying to start my server I ran into an issue of 
      events.js:173
      throw er; // Unhandled 'error' event
      ^

Error: listen EADDRINUSE: address already in use :::80
    at Server.setupListenHandle [as _listen2] (net.js:1255:14)
    at listenInCluster (net.js:1303:12)
    at Server.listen (net.js:1391:7)
    at Function.listen (/root/ad-free-app/node_modules/express/lib/application.js:618:24)
    at massive.then.db (/root/ad-free-app/server/server.js:27:9)
    at process.internalTickCallback (internal/process/next_tick.js:77:7)
Emitted 'error' event at:
    at emitErrorNT (net.js:1282:8)
    at process.internalTickCallback (internal/process/next_tick.js:72:19)
