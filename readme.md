[![npm status](http://img.shields.io/npm/v/tweety.svg)](https://www.npmjs.org/package/tweety)
[![npm status](https://img.shields.io/npm/dm/tweety.svg)](https://www.npmjs.org.package/tweety)

#Tweety
Use twitter through your terminal

##Installing

```
$ npm install tweety -g
```


##Usage:

###Initializing
Identify yourself! You'll only have to do this once.
```
$ tweety init
```
It'll prompt you to visit a URL, that URL will ask you to identify the app on twitter, and then it'll show you a code. Back on the command line,  enter that code and the app will save your tokens on a local json file.

###Sending:

To send a message, just run the following command:

```
$ tweety someUserName "The complete message"
```

_Note_ that if your message is longer than 140 characters, tweety will split it into as many parts as required and it'll send all parts sequentially. I should also point out, when typing the username you're sending your message to - you do **not** need to put an @ at the beginning. If you were to send a message to me (@ImJaken) then your command would look like this:

```
$ tweety ImJaken "Hey Jaken!"
```

###Receiving / Reading

With tweety you can do both: listing the latest 20 messages of your inbox, or reading a specific message. 
Here is how:

####Listing inbox
In order to read the latest 20 messages of your inbox, just use the following command:

```
$ tweety read inbox
```

You'll get a list of messages with the id of the message, the screen name of the sender, when was it send, and a small part of the text.
Something like this:

```
--- [ Inbox ]
[403959669888401400] FROM: someUser - 11/22/2013 - 4:54:25 pm - Hey, this is your d...
```

####Reading a specific message
If you want to the the full content of a specific message, just use the ID listed above, like this:

```
$ tweety read 403959669888401400
```

And you'll get something like this:

```
--- [ Message from: someUser on 11/20/2013 - 4:23:12 pm ] ---
Hey, this is your direct message!
```
