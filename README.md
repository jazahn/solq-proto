
## Setting up an https server

You're going to want to run this in dev via an https server, otherwise you'll have to "allow" use of microphone on every reload. I like node's http-server: `npm install -g http-server`

### Creating SSL certs

Using it with SSL means using the '-S' flag. This is going to need ssl certs. To create them:
`openssl req -newkey rsa:2048 -new -nodes -keyout key.pem -out key.pem`
`openssl req -newkey rsa:2048 -new -nodes -x509 -days 3650 -keyout key.pem -out cert.pem`

Now you can use `http-server -S`
