# gobot

Gobot is an IRC bot written in Golang - that can currently annoy you by repeating what you tell it. 

Here is an example of it in practice:

```
[20:40:43] <@nikhita> gobot hello!
[20:40:43] <gobot> nikhita " hello!"
[20:40:57] <@nikhita> gobot you are awesome
[20:40:58] <gobot> nikhita " you are awesome"
[20:41:25] <@nikhita> gobot stop copying me!!!
[20:41:26] <gobot> nikhita " stop copying me!!!"
```

Gobot intends to become more helpful in the future by becoming a Markov Chain IRC bot and giving you snarky replies!

(yeah, it will probably still annoy you).


## Installation

Please make sure that you are in your $GOPATH before executing the following commands. This makes use of the awesome irc client library by [husio](https://github.com/husio/irc).

```
go get github.com/husio/irc
git clone https://github.com/nikinath/gobot.git
cd gobot
go build
./gobot
```

## Usage

Currently, Gobot offers you these three commands:

```
	JOIN    <channel> [<key>]
	PRIVMSG <nick> <message to be sent>
	PART    <channel>
```

* **JOIN** - This is used to join a particular channel on Freenode. If a key is required for the channel, it can be mentioned too.
* **PRIVMSG** - This is used to send a private message to any user in the channel. You need to mention the nick of the user followed my the message that you want to send.
* **PART** - This is used to kick gobot out of the channel.

## Example

Gobot can be used to join any channel on Freenode. An example is shown below. Please write the desired channel name and nick name while executing.

```
JOIN #go-nuts
PRIVMSG nikhita hey, this is so cool!
PART #go-nuts
```

## Development

Gobot is still a simple bot but I am in the process of turning it into a [Markov Chain bot](http://stackoverflow.com/questions/5306729/how-do-markov-chain-chatbots-work). TLDR: A Markov Chain bot will generate new sentences using the words said previously and build intelligible replies.

If you'd like to know more or want to get in touch, please email at nikitaraghunath at gmail dot com or visit https://nikinath.github.io/.
