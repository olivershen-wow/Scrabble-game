# Scrabble Game

Online multi-player Scrabble game implemented in Java using TCP, Thread, and JavaFX.

## Use

### Server

```
$ java -jar ScrabbleServer.jar [options] -p <port>
```

Default port is 55555.

### Client

```
$ java -jar ScrabbleClient.jar
```


## Component

### Server
- send message to a certain player to act
- broadcast messages to all other players when current player acts
### Client
- handle operations from the server
### Client GUI
- display user interface
- show user instruction
- update the board
- show the score
- pass current turn
- vote if selection is a word

## Implementation
- TCP
- thread-per-connection architecture

## Demo
![Login](https://raw.githubusercontent.com/oliverShen1994/Scrabble-Game/master/Resource/Login.png)

![Desk](https://raw.githubusercontent.com/oliverShen1994/Scrabble-Game/master/Resource/Desk.png)

![Board](https://raw.githubusercontent.com/oliverShen1994/Scrabble-Game/master/Resource/Board&Score.png)
