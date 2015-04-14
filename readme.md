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
$ tweety destination_user_name "The complete message"
```

_Note_ that if your message is longer than 140 characters, TDM will split it into as many parts as required and it'll send all parts sequentially.

###Receiving / Reading

With TDM you can do both: listing the latest 20 messages of your inbox, or reading a specific message. 
Here is how:

####Listing inbox
In order to read the latest 20 messages of your inbox, just use the following command:

```
$ tweety read inbox
```

You'll get a list of messages with the id of the message, the screen name of the sender, when was it send, and a small part of the text.
Something like this:

```
--- [ Inbox ](last 20 messages) ---
[403959669888401400] FROM: someUser - 11/22/2013 - 4:54:25 pm - This message is too ...
[403951109326524400] FROM: anotherUser - 11/22/2013 - 4:20:24 pm - Testing short message
[364477670723043300] FROM: anotherUser1 - 08/5/2013 - 5:07:03 pm - Thank you so much for followin...
[352955266691657700] FROM: ImJaken - 07/4/2013 - 10:01:07 pm - Thank you so much for followin...
[326768482609930240] FROM: dribble - 04/23/2013 - 3:44:11 pm - Thanks for the follow! Check o...
[315868386716430340] FROM: coderbits - 03/24/2013 - 1:51:06 pm - Here is your beta invitation f...

 To read the full content of a message, do: `tweety read ID` (where ID is the first number shown above)```
```

####Reading a specific message
If you want to the the full content of a specific message, just use the ID listed above, like this:

```
$ tweety read 315868386716430340
```

And you'll get something like this:

```
--- [ Message from: someUser on 11/20/2013 - 4:23:12 pm ] ---
Hey, this is your direct message!
```

##Running this code locally

If you've downloaded the code and want to try it for yourself, you'll have to register an app on the twitter dev site and rename the file under `/lib/twitter-keys-sample.json` to `/lib/twitter-keys.json` filling in the tokens required.

