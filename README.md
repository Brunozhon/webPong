# Web Pong

Play my recreation of [Pong](https://brunozhon.github.io/webPong/) here! I learned a lot about the `<canvas>` element while I was working on this project! (And I might've stolen some bouncy ball code from MDN, too.)

This is part one of a series called Pong in Every Language. Part two is [over here](https://github.com/Brunozhon/fs-pong).

## Installation

No installation needed! [Play online right now!](https://brunozhon.github.io/webPong/)

If you want to play Web Pong locally, run:

```bash
git clone https://github.com/Brunozhon/webPong
```

Then, set up a server using your favorite command/program to set up a server in your current directory.

> **How do you set up a server?**
>
> In case you don't know your favorite command/program to set up a server, here's a simple one.
>
> 1. Create a file named `server.js` and paste this code in:
>
> ```javascript
> var http = require('http');
> var url = require('url');
> var fs = require('fs');
>
> http.createServer(function (req, res) {
>   var q = url.parse(req.url, true);
>   var filename = "." + q.pathname;
>   fs.readFile(filename, function(err, data) {
>     if (err) {
>       res.writeHead(404, {'Content-Type': 'text/html'});
>       return res.end("404 Not Found");
>     } 
>     res.writeHead(200, {'Content-Type': 'text/html'});
>     res.write(data);
>     return res.end();
>   });
> }).listen(8080);
> ```
>
> 2. [Install Node.js.](https://nodejs.org/en) (Come to think of it, that should've been Step 1.)
> 3. Type `node server.js` and voilà, you have a local copy up and running!

## Contributing

**I will not be accepting any pull requests or issues as this project is finished.**
