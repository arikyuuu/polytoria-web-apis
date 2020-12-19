# polytoria-web-apis

uncompleted list

| Domain | Description |
| -: | :- |
| [api.polytoria.com](https://api.polytoria.com/docs) | Misc Endpoints |

Probably undocumented APIs
=================
* [Chat APIs](#chat-apis)
* [User APIs](#user-apis)
* [Item APIs](#item-apis)
* [Friendship APIs](#friendship-apis)
* [Avatar APIs](#avatar-apis)
* [Asset APIs](#asset-apis)
* [Game APIs](#game-apis)
* [Forum APIs](#forum-apis)
* [Guild APIs](#guild-apis)


Chat APIs
---------
#### Fetch conversations
* https://polytoria.com/api/fetch/chat/conversations

#### Fetch chats
* https://polytoria.com/api/fetch/chat/chats?id=[chatID]
> chatID: localStorage.getItem("chatID");

#### Send a chat message
* https://polytoria.com/api/chat/send
> id: chatID

> msg: message 2 send

#### Start a new conversation
* https://polytoria.com/api/chat/start_conversation
> id: target user id

> csrf: your csrf

#### Fetch new messages
* https://polytoria.com/api/fetch/chat/newmessages?id=[chatID]
> chatID: localStorage.getItem("chatID");

User APIs
---------
#### Fetch user info
* https://polytoria.com/api/fetch/user/clientinfo?username=[username]
> username: ya lol

#### Fetch user's inventory
* https://polytoria.com/api/fetch/inventory?id=[userID]&type=[type]&limit=[limit]&p=[page]
> userID: target user id

> type: hat, face, tool, shirt, pants

> limit: any number (default 6)

> p: page

#### Load user's wall
* https://polytoria.com/api/fetch/user/wall?id=[id]&p=[page]
> id: user id

> p: page id

#### Block a user
* https://polytoria.com/api/users/block
> csrf: your csrf token

> id: user id

#### Interact with a trade
* https://polytoria.com/api/trade/action
> id: trade id

> action: accept, reject, cancel

> csrf: your csrf token

#### Convert your currency
* https://polytoria.com/api/currency/convert
> csrf: your csrf token

> brick-input or stud-input: number of bricks or studs

#### Log-off
* https://polytoria.com/login/expire

Item APIs
---------

#### Fetch catalog
* https://polytoria.com/api/fetch/catalog/items?page=[page]&type=[type]&sort=[sortType]&q=[searchQuery]
> page: page (optional)

> type: hat, face, shirt, pants, tool

> sortType: 0 (featured), 1 (best selling), 2 (recently updated), 3 (least expensive), 4 (most expensive)

> searchQuery: search query (optional)


#### Purchase an item
* https://polytoria.com/api/catalog/purchase
> csrf: your csrf token

> id: item id

#### Remove an item
* https://polytoria.com/api/catalog/remove-inventory
> csrf: your csrf token

> id: item id 


#### Fetch item comments
* https://polytoria.com/api/fetch/catalog/comments?id=[id]&limit=[limit]&offset=[offset]
> id: item id

> limit: any number (default 4)

> offset (optional): + 4 * commpage (commpage AKA COMMENT PAGE)

#### Comment on an item
* https://polytoria.com/api/catalog/comment
> id: item id

> content: message

> g-recaptcha-response: captcha response key

> csrf: your csrf


#### Load resellers
* https://polytoria.com/api/fetch/catalog/resellers?id=[id]&limit=[limit]&offset=[offset]
> id: item id

> limit: any number (default 4)

> offset (optional): + 4 * respage

#### Load owners
* https://polytoria.com/api/fetch/catalog/owners?id=[id]&limit=[limit]&page=[page]
> id: item id

> limit: any number (default 4)

> page: page

#### Purchase an limited item
* https://polytoria.com/api/catalog/purchasecollectible
> id: limited item id

> csrf: yo csrf token lol

#### Offsale all
* https://polytoria.com/api/catalog/offsale_all
> id: item id

> csrf: your csrf tokenn thingy

#### Sell an limited item
* https://polytoria.com/api/catalog/sellcollectible?serial=[itemserialid]&price=[price]&itemid=[itemid]&csrf=[csrf]
> itemserialid: your item's serial id

> price: chosen price

> itemid: item id

> csrf: your csrf tokenn thingy

#### Purchase an limited item
* https://polytoria.com/api/catalog/purchasecollectible
> id: limited item id

> csrf: yo csrf token lol

Friendship APIs
---------

#### Fetch all friend requests
* https://polytoria.com/api/fetch/requests?p=[page]

#### Fetch all friends
* https://polytoria.com/api/fetch/friends?p=[page]

#### Fetch user's friends
* https://polytoria.com/api/fetch/user/friends?id=[id]&p=[page]

#### Friend button info
* https://polytoria.com/api/users/friendbutton?id=[id]
> id: user id

#### Send a friend request
* https://polytoria.com/api/users/addfriend
> csrf: your csrf token

> id: user id

#### Remove a friend
* https://polytoria.com/api/users/removefriend
> csrf: your csrf token

> id: user id

Avatar APIs
---------
#### Load items
* https://polytoria.com/api/fetch/wardrobe?type=[type]&limit=[limit]&page=[page]
> type: face, pants, hat, shirt, tool

> limit: default is 8

> page: page

#### Load wearing items
* https://polytoria.com/api/fetch/wearing

#### Set part color
* https://polytoria.com/api/avatar/setcolor
> part: body part (Torso, LeftLeg, LeftArm, RightLeg, RightArm, Head)

> color: chosen color

> csrf: your csrf token

#### Wear
* https://polytoria.com/api/avatar/wear
> id: item id

> csrf: your csrf token

#### Unwear
* https://polytoria.com/api/avatar/unwear
> id: item id

> csrf: your csrf token

#### Render
* https://polytoria.com/api/avatar/render
> csrf: your csrf token

> if you want to force redraw use this => forceRedraw: 1

#### Load outfits
* https://polytoria.com/api/fetch/outfits?limit=[limit]&page=[page]
> limit: default is 8

> page: page

#### Wear an outfit
* https://polytoria.com/api/avatar/loadoutfit
> csrf: your csrf token

> id: outfit id

#### Save an outfit
* https://polytoria.com/api/avatar/saveoutfit
> csrf: your csrf token

> name: outfit name

#### Delete an outfit
* https://polytoria.com/api/avatar/deleteoutfit
> csrf: your csrf token

> id: outfit id


Asset APIs
---------
#### Search
* https://polytoria.com/api/fetch/search?q=[search_query]

#### Validate username
* https://polytoria.com/api/settings/validate_username?username=[username]

Game APIs
---------
#### Fetch all games
* https://polytoria.com/api/fetch/games?page=[page]&type=[type]
> page: a PAGE number bro (default is 0 on every &page= ig)

> type: popular, updated

#### Get a game launch token 
* https://polytoria.com/api/games/request-server
> csrf: your token

> id: game id

#### Get a callback status
* https://polytoria.com/api/games/fetch-callback-status?h=
> h: hash

#### Launch a game (not an api but wahtever)
> go to polytoria://launch_[GAME LAUNCH TOKEN]

#### Activate/deactivate a game
* https://polytoria.com/api/games/toggle-active
> id: game id

> csrf: yes u know what is this already

Forum APIs
---------
#### Fetch posts
* https://polytoria.com/api/fetch/forum/threads?id=1[subforum_id]&limit=[limit]&offset=[offset]
> limit: 10

> offset: page * limit

#### Reply to a post
* https://polytoria.com/api/forum/reply
> csrf: your csrf

> content: message

> reply_to: post id

> captcha: captcha response

Guild APIs
---------
#### Join a guild
* https://polytoria.com/api/guilds/join?id=[id]
> id: guild id

#### Leave a guild
* https://polytoria.com/api/guilds/leave?id=[id]
> id: guild id

#### Post on a guild wall
* https://polytoria.com/api/guilds/post-wall
> gid: group id

> g-recaptcha-response: captcha response key

> message: message 2 post

> csrf: your csrf

#### Load a guild wall
* https://polytoria.com/api/fetch/guilds/wall?id=[id]&p=[page]
> id: guild id

> p: page

#### Load a guild store
* https://polytoria.com/api/fetch/guilds/store?id=[id]&p=[page]
> id: guild id

> p: page

#### Load guild members
* https://polytoria.com/api/fetch/guilds/members?gid=[id]&role=[role_value]&page=[page]
> gid: id

> role: chosen role id

> page: page

Broken APIs
---------
#### Add reaction (forum post ig)
* https://polytoria.com/api/addreaction.php?e=[emoji_id]&pid=[post_id]

#### Open Purchase Collectible Modal (not broken but y know it doesnt work when ur not on the site)
* https://polytoria.com/api/fetch/catalog/limited?id=[itemid]
