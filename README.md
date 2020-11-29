# polytoria-web-apis

uncompleted list

| Domain | Description |
| -: | :- |
| [api.polytoria.com](https://api.polytoria.com/docs) | Misc Endpoints |

Probably undocumented APIs
=================
* [Chat APIs](#chat-apis)

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
