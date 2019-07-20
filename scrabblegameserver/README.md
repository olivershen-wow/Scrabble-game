## ScrabbleGameServer

## Task
# To Do:
* Register user names
* Start a game
* Vote
* Update UI
* Exit

# Description
* InputHandler.java: InputHandle class. Deal with command line parameters when starting with the java jar file.
* Server.java: Server class. Start a server thread and up to 4 client threads. Deal with the message exchange.
* Message.java: Message class.

# Message
## client -> server  
* INIT (my username) 登录  
* INVITE (others username) 邀请  
* INVITE_RESPONSE (yes/no) 邀请回复  
* START () 开始游戏  
* PLACE_TILE (row, col, letter) 放置棋子  
* PASS () 跳过投票  
* POLL (word) 发起投票  
* VOTE_RESPONSE (YES/NO DOUBLE) 投票回复  


## server -> client  
* UPDATELIST LOBBY_ONLINE_PLAYER (all online usernames) 更新在线用户列表  
* UPDATETABLE LOBBY_TABLE_PLAYER (usernames of the table) 更新桌子的用户列表  
* INVITE (username) 邀请指定用户  
* UPDATE PLACE (row, col, letter) 放置棋子  
* UPDATE VOTE_PANE (word(s) 可能有两个) 显示界面投票面板
* UPDATE SCORE_PANE (username, score) 更新玩家分数  
* POLL (poll) 发起投票 (广播给发起人之外的人, 可以投一个词或两个词)  


# Server Functions:
* 维护所有在线玩家  
* 维护一桌的玩家  
* 计算投票结果  
* 控制玩家顺序 （每个玩家防止棋子 -> 选择是否发起投票 ->是  发起投票 -> 等待其他玩家投票结果 -> 计算投票是否成功 ->  
                                                    ->否  下一个玩家