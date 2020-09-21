# Installing and Running SimpleChat, Phase 1

## Install OCSF First

To run the SimpleChat, you must first install [OCSF](/ocsf)
and make sure ocsf is in your classpath (or is a
subdirectory of simplechat1)

## Compile All Java Files

Then you must compile the .java files, including those in the
subdirectories.

## Starting SimpleChat Server

To run the SimpleChat you must first start a server:

```
java EchoServer
```

Then you start one or more clients:

```
java ClientConsole
```

To run a client on a different machine, you enter

```
java ClientConsole <serveraddress>
```

Where `<serveraddress>` is the IP address or host name of the machine where the
server is runing. Once a client is running, you can type some text; the
text will be echoed to any other clients that are running.

To learn how this code works, consult the book
[Object-Oriented Software Engineering:
Practical Software Development using UML and Java](https://www.lloseng.com)
by Lethbridge and Lagani&egrave;re. The book contains many exercises where you will add
features to SimpleChat.

If the server won't start, it might be because the default `port` number
of `5555` is already in use. Follow the exercises in the book to improve the
code and solve this problem.
