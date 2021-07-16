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
* [Ad APIs](#ad-apis)
* [Other APIs](#other-apis)


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
* https://polytoria.com/api/fetch/favourites?id=[userID]&type=[type]&limit=[limit]&p=[page]
> userID: target user id

> type: hat, face, tool, shirt, pants

> limit: any number (default 6)

> p: page

#### Fetch user's favourites
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

#### Convert your currency (deprecated)
* https://polytoria.com/api/currency/convert
> csrf: your csrf token

> brick-input or stud-input: number of bricks or studs

#### "Calculate" recieved currency
* https://polytoria.com/api/exchange/market-value?currency=[type]&amount=[amount]

> type: bricks, studs

> amount: an amount of bricks OR studs, lol?

#### Place limit order
* https://polytoria.com/api/exchange/place-limit-order
> amount-give: how much u will give

> amount-ask: how much u asked

> currency: bricks or studs

> split (optional): 1 = true, 0 = false

> csrf: your csrf token

#### Place market order
* https://polytoria.com/api/exchange/place-market-order
> amount: how much bricks or studs

> currency: bricks or studs

> csrf: your csrf token

#### Cancel order
* https://polytoria.com/api/exchange/cancel-order
> id: order id

> csrf: your csrf token

#### Log-out
* https://polytoria.com/login/expire

#### Verify Email
* https://polytoria.com/api/auth/verify-email
> csrf: your csrf token

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

#### Purchase a pack
* https://polytoria.com/api/catalog/purchase-pack
> id: pack item id
> csrf: your csrf token

#### View pack contents
* https://polytoria.com/api/fetch/catalog/pack-contents?id=
> id: pack item id

#### Open pack
* https://polytoria.com/api/catalog/open-pack
> id: pack id
> csrf: csrf token


#### Favourite an item
* https://polytoria.com/api/catalog/favourite
> id: item id
> csrf: your csrf token

#### Fetch total item favourites
* https://polytoria.com/api/fetch/catalog/favourites?id=[id]
> id: item id

#### Fetch chart data
* https://polytoria.com/api/fetch/chart?id=[itemid]
> id: limited item id - needs to be an limited item

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
> OLD CLIENTS: go to polytoria://launch_[GAME LAUNCH TOKEN]

> NEW CLIENTS: polytoria://client/game_token_hash_idk

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

#### Give user reputation (not tested, use at ur own risk!!)
* https://polytoria.com/api/forum/rep
> id: post id

> csrf: your csrf

> neg: (default: 0) (not tested yet, possibly uses negative numbers and normal numbers e.g. -29 or 29 mixed with userid???)

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

#### Load your guilds (guilds you're in)
* https://polytoria.com/api/fetch/guilds/myguilds?page=[page]
> page: page number

> limit: add &limit=limitnumber at the end of the url

#### Load popular guilds
* https://polytoria.com/api/fetch/guilds/popularguilds?page=[page]&q=[query]
> page: page number

> query: search query, (optional -> can be blank)

Ad APIs
---------
#### Get a user-created ad
* https://polytoria.com/api/userads/fetch

#### Get a user-created ad redirect
* https://polytoria.com/api/userads/adgateway?b=[adId]

> adId: advertisement id

Other APIs
---------
#### Leaderboard
* https://polytoria.com/api/fetch/leaderboard?c=[category]&p=[page]
> Category: networth, posts, comments, views, sales

> Page: page number

Broken APIs
---------
#### Add reaction (forum post ig)
* https://polytoria.com/api/addreaction.php?e=[emoji_id]&pid=[post_id]

#### Open Purchase Collectible Modal (not broken but y know it doesnt work when ur not on the site)
* https://polytoria.com/api/fetch/catalog/limited?id=[itemid]

