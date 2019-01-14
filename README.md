# -This Is My Coding Notes Repo-
## Problems & Solutions
* While Hosting and trying to start my server I ran into an issue of 
node server/server
      * ```events.js:173
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
    at process.internalTickCallback (internal/process/next_tick.js:72:19)```
      * So the problem seems to be that my server was running but not at the same time, sounds dumb I know but the solution was this
     input this into your project folder you are trying to host ```sudo lsof -i -P -n | grep LISTEN``` and you'll have a few things return for me it was this and yours will be something similar 
     ```
sshd     1564 root    3u  IPv4  15721      0t0  TCP *:22 (LISTEN)
sshd     1564 root    4u  IPv6  15736      0t0  TCP *:22 (LISTEN)
node     2114 root   25u  IPv6 135444      0t0  TCP *:80``` This is your node server port ``` (LISTEN)
```
and if you notice my node server is the last one so it was running already but when I search my hosted IP in my chrome url I was getting an endless load for some reason because of that node server running. So to fix it I had to stop the node server and to do that I ran this
```for p in `sudo lsof -n -i:80 | grep LISTEN | awk '{print $2}'`; do sudo kill -9 $p; done``` 
and it should return nothing so if you put in this code again ```sudo lsof -i -P -n | grep LISTEN ``` you should have it return similar to before but with your node server gone.
So with your Node Server stopped you can go again and run ```node server/server``` or where ever your server us running and it should work without getting the throw er;
