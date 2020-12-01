# polytoria-web-apis

uncompleted list

| Domain | Description |
| -: | :- |
| [api.polytoria.com](https://api.polytoria.com/docs) | Misc Endpoints |

Probably undocumented APIs
=================
* [Chat APIs](#chat-apis)
* [User APIs](#user-apis)
* [Asset APIs](#asset-apis)
* [Game APIs](#game-apis)
* [Forum APIs](#forum-apis)
* [Guild APIs](#guild-apis)


Chat APIs
---------
#### Fetch conversations
* https://polytoria.net/api/fetch/chat/conversations

#### Fetch chats
* https://polytoria.net/api/fetch/chat/chats?id=[chatID]
> chatID: localStorage.getItem("chatID");

#### Send a chat message
* https://polytoria.net/api/chat/send
> id: chatID

> msg: message 2 send

#### Start a new conversation
* https://polytoria.net/api/chat/start_conversation
> id: target user id

> csrf: your csrf

#### Fetch new messages
* https://polytoria.net/api/fetch/chat/newmessages?id=[chatID]
> chatID: localStorage.getItem("chatID");

User APIs
---------
#### Fetch user's inventory
* https://polytoria.com/api/fetch/inventory?id=[userID]&type=[type]&limit=[limit]&p=[page]
> userID: target user id

> type: hat, face, tool, shirt, pants

> limit: any number (default 6)

> p: page

#### Friend button info
* https://polytoria.net/api/users/friendbutton?id=[userid]
> id: target user id


#### 
* https://polytoria.net/api/forum/reply
> 


#### 
* https://polytoria.net/api/forum/reply
> 


#### 
* https://polytoria.net/api/forum/reply
> 


#### Interact with a trade
* https://polytoria.com/api/trade/action
> id: trade id

> action: accept, reject, cancel

> csrf: your csrf token

#### Convert your currency
* https://polytoria.com/api/currency/convert
> csrf: your csrf token

> brick-input or stud-input: number of bricks or studs


Asset APIs
---------
#### Search
* https://polytoria.com/api/fetch/search?q=[search_query]


Game APIs
---------
#### 
* https://polytoria.net
> 

Forum APIs
---------
#### Fetch posts
* https://polytoria.net/api/fetch/forum/threads?id=1[subforum_id]&limit=[limit]&offset=[offset]
> limit: 10

> offset: page * limit

#### 
* https://polytoria.net/api/forum/reply
> 


#### Reply to a post
* https://polytoria.net/api/forum/reply
> csrf: your csrf

> content: message

> reply_to: post id

> captcha: captcha response

Guild APIs
---------
#### Join a guild
* https://polytoria.net/api/guilds/join?id=[id]
> id: guild id

#### Leave a guild
* https://polytoria.net/api/guilds/leave?id=[id]
> id: guild id

#### Post on a guild wall
* https://polytoria.net/api/guilds/post-wall
> gid: group id

> g-recaptcha-response: captcha response key

> message: message 2 post

> csrf: your csrf

#### Load a guild wall
* https://polytoria.net/api/fetch/guilds/wall?id=[id]&p=[page]
> id: guild id

> p: page

#### Load a guild store
* https://polytoria.net/api/fetch/guilds/store?id=[id]&p=[page]
> id: guild id

> p: page

#### Load guild members
* https://polytoria.net/api/fetch/guilds/members?gid=[id]&role=[role_value]&page=[page]
> gid: id

> role: chosen role id

> page: page

Broken APIs
---------
# Add reaction (forum post ig)
* https://polytoria.com/api/addreaction.php?e=[emoji_id]&pid=[post_id]
