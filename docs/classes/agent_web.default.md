[@livechat/lc-sdk-js](../README.md) / [agent/web](../modules/agent_web.md) / default

# Class: default

[agent/web](../modules/agent_web.md).default

## Hierarchy

- [`WebAPI`](internal.WebAPI.md)

  ↳ **`default`**

## Table of contents

### Constructors

- [constructor](agent_web.default.md#constructor)

### Properties

- [APIURL](agent_web.default.md#apiurl)
- [clientID](agent_web.default.md#clientid)
- [tokenGetter](agent_web.default.md#tokengetter)
- [type](agent_web.default.md#type)
- [version](agent_web.default.md#version)

### Methods

- [addUserToChat](agent_web.default.md#addusertochat)
- [banCustomer](agent_web.default.md#bancustomer)
- [createCustomer](agent_web.default.md#createcustomer)
- [deactivateChat](agent_web.default.md#deactivatechat)
- [deleteChatProperties](agent_web.default.md#deletechatproperties)
- [deleteEventProperties](agent_web.default.md#deleteeventproperties)
- [deleteThreadProperties](agent_web.default.md#deletethreadproperties)
- [followChat](agent_web.default.md#followchat)
- [followCustomer](agent_web.default.md#followcustomer)
- [getChat](agent_web.default.md#getchat)
- [getCustomer](agent_web.default.md#getcustomer)
- [listAgentsForTransfer](agent_web.default.md#listagentsfortransfer)
- [listArchives](agent_web.default.md#listarchives)
- [listChats](agent_web.default.md#listchats)
- [listRoutingStatuses](agent_web.default.md#listroutingstatuses)
- [listThreads](agent_web.default.md#listthreads)
- [markEventsAsSeen](agent_web.default.md#markeventsasseen)
- [multicast](agent_web.default.md#multicast)
- [removeUserFromChat](agent_web.default.md#removeuserfromchat)
- [resumeChat](agent_web.default.md#resumechat)
- [send](agent_web.default.md#send)
- [sendEvent](agent_web.default.md#sendevent)
- [sendRichMessagePostback](agent_web.default.md#sendrichmessagepostback)
- [sendTypingIndicator](agent_web.default.md#sendtypingindicator)
- [setRoutingStatus](agent_web.default.md#setroutingstatus)
- [startChat](agent_web.default.md#startchat)
- [tagThread](agent_web.default.md#tagthread)
- [transferChat](agent_web.default.md#transferchat)
- [unfollowChat](agent_web.default.md#unfollowchat)
- [unfollowCustomer](agent_web.default.md#unfollowcustomer)
- [untagThread](agent_web.default.md#untagthread)
- [updateChatProperties](agent_web.default.md#updatechatproperties)
- [updateCustomer](agent_web.default.md#updatecustomer)
- [updateEventProperties](agent_web.default.md#updateeventproperties)
- [updateThreadProperties](agent_web.default.md#updatethreadproperties)
- [uploadFile](agent_web.default.md#uploadfile)

## Constructors

### constructor

• **new default**(`clientID`, `tokenGetter`, `options?`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `clientID` | `string` |
| `tokenGetter` | [`TokenGetter`](../modules/authorization.md#tokengetter) |
| `options?` | [`WebAPIOptions`](../interfaces/objects.WebAPIOptions.md) |

#### Overrides

[WebAPI](internal.WebAPI.md).[constructor](internal.WebAPI.md#constructor)

#### Defined in

[agent/web.ts:33](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L33)

## Properties

### APIURL

• **APIURL**: `string`

#### Inherited from

[WebAPI](internal.WebAPI.md).[APIURL](internal.WebAPI.md#apiurl)

#### Defined in

[internal/index.ts:15](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/internal/index.ts#L15)

___

### clientID

• `Protected` `Readonly` **clientID**: `string`

#### Inherited from

[WebAPI](internal.WebAPI.md).[clientID](internal.WebAPI.md#clientid)

#### Defined in

[internal/index.ts:28](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/internal/index.ts#L28)

___

### tokenGetter

• `Protected` `Readonly` **tokenGetter**: [`TokenGetter`](../modules/authorization.md#tokengetter)

#### Inherited from

[WebAPI](internal.WebAPI.md).[tokenGetter](internal.WebAPI.md#tokengetter)

#### Defined in

[internal/index.ts:29](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/internal/index.ts#L29)

___

### type

• `Protected` `Readonly` **type**: `apiType`

#### Inherited from

[WebAPI](internal.WebAPI.md).[type](internal.WebAPI.md#type)

#### Defined in

[internal/index.ts:30](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/internal/index.ts#L30)

___

### version

• **version**: `string`

#### Inherited from

[WebAPI](internal.WebAPI.md).[version](internal.WebAPI.md#version)

#### Defined in

[internal/index.ts:16](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/internal/index.ts#L16)

## Methods

### addUserToChat

▸ **addUserToChat**(`chat_id`, `user_id`, `user_type`, `visibility`, `ignore_requester_presence?`): `Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

Adds a user to the chat. You can't add more than one customer user type to the chat.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `chat_id` | `string` | chat to add user to |
| `user_id` | `string` | user to add |
| `user_type` | `string` | customer or agent |
| `visibility` | `string` | possible values: all, agents |
| `ignore_requester_presence?` | `boolean` | if true, allows to add user to chat even if the requester is not present in the chat |

#### Returns

`Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

#### Defined in

[agent/web.ts:138](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L138)

___

### banCustomer

▸ **banCustomer**(`id`, `days`): `Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

Bans the customer for a specific period of time. It immediately disconnects all active sessions of this customer
and does not accept new ones during the ban lifespan.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `id` | `string` | ID of customer to ban |
| `days` | `number` | ban duration in days |

#### Returns

`Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

#### Defined in

[agent/web.ts:349](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L349)

___

### createCustomer

▸ **createCustomer**(`opts?`): `Promise`<[`CreateCustomerResponse`](../interfaces/agent_structures.CreateCustomerResponse.md)\>

Creates a new Customer user type.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `opts?` | [`CustomerParameters`](../interfaces/agent_structures.CustomerParameters.md) | customer data |

#### Returns

`Promise`<[`CreateCustomerResponse`](../interfaces/agent_structures.CreateCustomerResponse.md)\>

#### Defined in

[agent/web.ts:330](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L330)

___

### deactivateChat

▸ **deactivateChat**(`id`, `ignore_requester_presence?`): `Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

Deactivates a chat by closing the currently open thread. Sending messages to this thread will no longer be possible.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `id` | `string` | chat ID to deactivate |
| `ignore_requester_presence?` | `boolean` | if true, allows to deactivate the chat even if the requester is not present in the chat |

#### Returns

`Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

#### Defined in

[agent/web.ts:96](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L96)

___

### deleteChatProperties

▸ **deleteChatProperties**(`id`, `properties`): `Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

Deletes chat properties

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `id` | `string` | chat to delete properties |
| `properties` | [`Properties`](../interfaces/objects.Properties.md) | properties to delete |

#### Returns

`Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

#### Defined in

[agent/web.ts:224](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L224)

___

### deleteEventProperties

▸ **deleteEventProperties**(`chat_id`, `thread_id`, `event_id`, `properties`): `Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

Deletes event properties

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `chat_id` | `string` | chat ID of event to delete |
| `thread_id` | `string` | thread ID of event to delete |
| `event_id` | `string` | event to delete properties |
| `properties` | [`Properties`](../interfaces/objects.Properties.md) | properties to delete |

#### Returns

`Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

#### Defined in

[agent/web.ts:284](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L284)

___

### deleteThreadProperties

▸ **deleteThreadProperties**(`chat_id`, `thread_id`, `properties`): `Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

Deletes thread properties

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `chat_id` | `string` | chat ID of thread to delete |
| `thread_id` | `string` | thread to delete properties |
| `properties` | [`Properties`](../interfaces/objects.Properties.md) | properties to delete |

#### Returns

`Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

#### Defined in

[agent/web.ts:248](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L248)

___

### followChat

▸ **followChat**(`id`): `Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

Marks a chat as followed. All changes to the chat will be sent to the requester until the chat is reactivated or unfollowed.
Chat members don't need to follow their chats. They receive all chat pushes regardless of their follower status.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `id` | `string` | chat ID to follow |

#### Returns

`Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

#### Defined in

[agent/web.ts:108](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L108)

___

### followCustomer

▸ **followCustomer**(`id`): `Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

Marks a customer as followed. As a result, the requester (an agent) will receive
the info about all the changes related to that customer via pushes.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `id` | `string` | ID of customer to follow |

#### Returns

`Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

#### Defined in

[agent/web.ts:412](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L412)

___

### getChat

▸ **getChat**(`chat_id`, `thread_id?`): `Promise`<[`GetChatResponse`](../interfaces/agent_structures.GetChatResponse.md)\>

It returns a thread that the current Agent has access to in a given chat.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `chat_id` | `string` | ID of a chat to get |
| `thread_id?` | `string` | thread ID to get (if not provided, last thread is returned) |

#### Returns

`Promise`<[`GetChatResponse`](../interfaces/agent_structures.GetChatResponse.md)\>

#### Defined in

[agent/web.ts:59](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L59)

___

### getCustomer

▸ **getCustomer**(`id`): `Promise`<[`GetCustomerResponse`](../interfaces/agent_structures.GetCustomerResponse.md)\>

Returns the info about the Customer with a given id.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `id` | `string` | customer ID to get |

#### Returns

`Promise`<[`GetCustomerResponse`](../interfaces/agent_structures.GetCustomerResponse.md)\>

#### Defined in

[agent/web.ts:322](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L322)

___

### listAgentsForTransfer

▸ **listAgentsForTransfer**(`chat_id`): `Promise`<[`AgentForTransfer`](../interfaces/agent_structures.AgentForTransfer.md)[]\>

It returns the Agents you can transfer a chat to. Agents are sorted ascendingly by the total number of active chats they have. Note that:
- The method only returns Agents with statuses online and not accepting chats. Offline Agents aren't returned.
- Only chats with Customers are taken into account in total_active_chats.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `chat_id` | `string` | chat ID you want to transfer |

#### Returns

`Promise`<[`AgentForTransfer`](../interfaces/agent_structures.AgentForTransfer.md)[]\>

#### Defined in

[agent/web.ts:403](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L403)

___

### listArchives

▸ **listArchives**(`opts?`): `Promise`<[`ListArchivesResponse`](../interfaces/agent_structures.ListArchivesResponse.md)\>

It returns a list of the chats an Agent has access to. Together with a chat, the events of one thread from this chat are returned.

The list classification is based on threads; 1 chat per 1 thread. Thus, the same chat object may appear on the list several times,
but each time with a different thread. The returned chat is a complete object, not only a chat summary.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `opts?` | [`ListArchivesParameters`](../interfaces/agent_structures.ListArchivesParameters.md) | options like filters or pagination |

#### Returns

`Promise`<[`ListArchivesResponse`](../interfaces/agent_structures.ListArchivesResponse.md)\>

#### Defined in

[agent/web.ts:70](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L70)

___

### listChats

▸ **listChats**(`opts?`): `Promise`<[`ListChatsResponse`](../interfaces/agent_structures.ListChatsResponse.md)\>

It returns summaries of the chats an Agent has access to.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `opts?` | [`ListChatParameters`](../interfaces/agent_structures.ListChatParameters.md) | set of filters and pagination to limit returned entries |

#### Returns

`Promise`<[`ListChatsResponse`](../interfaces/agent_structures.ListChatsResponse.md)\>

#### Defined in

[agent/web.ts:41](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L41)

___

### listRoutingStatuses

▸ **listRoutingStatuses**(`group_ids?`): `Promise`<[`SetRoutingStatusResponse`](../interfaces/agent_structures.SetRoutingStatusResponse.md)[]\>

Returns the current routing status of each agent.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `group_ids?` | `number`[] | groups to list agent routing statuses from |

#### Returns

`Promise`<[`SetRoutingStatusResponse`](../interfaces/agent_structures.SetRoutingStatusResponse.md)[]\>

#### Defined in

[agent/web.ts:428](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L428)

___

### listThreads

▸ **listThreads**(`chat_id`, `opts?`): `Promise`<[`ListThreadsResponse`](../interfaces/agent_structures.ListThreadsResponse.md)\>

Returns threads that the current Agent has access to in a given chat.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `chat_id` | `string` | chat ID to get threads from |
| `opts?` | [`ListThreadsParameters`](../interfaces/agent_structures.ListThreadsParameters.md) | additional options like pagination and sorting |

#### Returns

`Promise`<[`ListThreadsResponse`](../interfaces/agent_structures.ListThreadsResponse.md)\>

#### Defined in

[agent/web.ts:50](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L50)

___

### markEventsAsSeen

▸ **markEventsAsSeen**(`chat_id`, `seen_up_to`): `Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

Marks events as seen by Agent.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `chat_id` | `string` | chat to mark events |
| `seen_up_to` | `string` | date up to which mark events |

#### Returns

`Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

#### Defined in

[agent/web.ts:367](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L367)

___

### multicast

▸ **multicast**(`recipients`, `content`, `type?`): `Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

This method serves for the chat-unrelated communication. Messages sent using multicast are not being saved.
For example, it could be used in an app that sends notifications to Agents or Customers,
when a certain condition is met (e.g. an important Customer started the chat).

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `recipients` | [`MulticastRecipients`](../interfaces/agent_structures.MulticastRecipients.md) | who should receive multicast |
| `content` | `object` | = JSON content to send |
| `type?` | `string` | message type |

#### Returns

`Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

#### Defined in

[agent/web.ts:393](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L393)

___

### removeUserFromChat

▸ **removeUserFromChat**(`chat_id`, `user_id`, `ignore_requester_presence?`): `Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

Removes a user from chat. Removing customer user type is not allowed. It's always possible to remove the requester from the chat.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `chat_id` | `string` | chat to remove user from |
| `user_id` | `string` | user to remove |
| `ignore_requester_presence?` | `boolean` | if true, allows to remove user from chat even if the requester is not present in the chat |

#### Returns

`Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

#### Defined in

[agent/web.ts:159](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L159)

___

### resumeChat

▸ **resumeChat**(`param`): `Promise`<[`ResumeChatResponse`](../interfaces/agent_structures.ResumeChatResponse.md)\>

Restarts an archived chat

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `param` | `string` \| [`ResumeChatParameters`](../interfaces/agent_structures.ResumeChatParameters.md) | either string ID of a chat to activate or full initial chat object |

#### Returns

`Promise`<[`ResumeChatResponse`](../interfaces/agent_structures.ResumeChatResponse.md)\>

#### Defined in

[agent/web.ts:86](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L86)

___

### send

▸ **send**<`T`\>(`name`, `req`): `Promise`<`T`\>

#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | `unknown` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `name` | `string` |
| `req` | `any` |

#### Returns

`Promise`<`T`\>

#### Inherited from

[WebAPI](internal.WebAPI.md).[send](internal.WebAPI.md#send)

#### Defined in

[internal/index.ts:37](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/internal/index.ts#L37)

___

### sendEvent

▸ **sendEvent**(`chat_id`, `event`, `attach_to_last_thread?`): `Promise`<[`SendEventResponse`](../interfaces/agent_structures.SendEventResponse.md)\>

Sends an Event object. Use this method to send a message by specifing the Message event type in the request.
It's possible to write to a chat without joining it. The user sending an event will be automatically added to the chat
with the present parameter set to false.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `chat_id` | `string` | chat to send event to |
| `event` | [`Event`](../modules/objects.md#event) | Event object |
| `attach_to_last_thread?` | `boolean` | if true, adds event to last inactive thread |

#### Returns

`Promise`<[`SendEventResponse`](../interfaces/agent_structures.SendEventResponse.md)\>

#### Defined in

[agent/web.ts:179](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L179)

___

### sendRichMessagePostback

▸ **sendRichMessagePostback**(`opts`): `Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

Sends postback for rich message

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `opts` | [`SendRichMessagePostbackParameters`](../interfaces/agent_structures.SendRichMessagePostbackParameters.md) | postback data |

#### Returns

`Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

#### Defined in

[agent/web.ts:206](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L206)

___

### sendTypingIndicator

▸ **sendTypingIndicator**(`chat_id`, `is_typing`, `visibility?`): `Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

Sends typing indicator

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `chat_id` | `string` | chat for typing indicator |
| `is_typing` | `boolean` | status of typing |
| `visibility?` | `string` | possible values: all, agents |

#### Returns

`Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

#### Defined in

[agent/web.ts:377](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L377)

___

### setRoutingStatus

▸ **setRoutingStatus**(`status`, `agent_id?`): `Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

Changes the status of an Agent or a Bot Agent.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `status` | [`RoutingStatus`](../enums/objects.RoutingStatus.md) | status to set |
| `agent_id?` | `string` | ID of agent to update status |

#### Returns

`Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

#### Defined in

[agent/web.ts:358](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L358)

___

### startChat

▸ **startChat**(`opts?`): `Promise`<[`StartChatResponse`](../interfaces/agent_structures.StartChatResponse.md)\>

Starts a chat

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `opts?` | [`StartChatParameters`](../interfaces/agent_structures.StartChatParameters.md) | options like initial chat data or continuous switch |

#### Returns

`Promise`<[`StartChatResponse`](../interfaces/agent_structures.StartChatResponse.md)\>

#### Defined in

[agent/web.ts:78](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L78)

___

### tagThread

▸ **tagThread**(`chat_id`, `thread_id`, `tag`): `Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

Tags thread with given tag

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `chat_id` | `string` | chat ID of thread to tag |
| `thread_id` | `string` | thread to tag |
| `tag` | `string` | tag to add |

#### Returns

`Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

#### Defined in

[agent/web.ts:304](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L304)

___

### transferChat

▸ **transferChat**(`id`, `opts?`): `Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

Transfers a chat to an Agent or a group.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `id` | `string` | chat to transfer |
| `opts?` | [`TransferChatParameters`](../interfaces/agent_structures.TransferChatParameters.md) | specific request flags |

#### Returns

`Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

#### Defined in

[agent/web.ts:126](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L126)

___

### unfollowChat

▸ **unfollowChat**(`id`): `Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

Removes the requester from the chat followers. After that, only key changes to the chat (like transfer_chat or close_active_thread)
will be sent to the requester. Chat members cannot unfollow the chat.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `id` | `string` | chat ID to unfollow |

#### Returns

`Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

#### Defined in

[agent/web.ts:117](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L117)

___

### unfollowCustomer

▸ **unfollowCustomer**(`id`): `Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

Removes the agent from the list of customer's followers.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `id` | `string` | ID of customer to unfollow |

#### Returns

`Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

#### Defined in

[agent/web.ts:420](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L420)

___

### untagThread

▸ **untagThread**(`chat_id`, `thread_id`, `tag`): `Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

Removes tag from thread

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `chat_id` | `string` | chat ID of thread to untag |
| `thread_id` | `string` | thread to untag |
| `tag` | `string` | tag to remove |

#### Returns

`Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

#### Defined in

[agent/web.ts:314](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L314)

___

### updateChatProperties

▸ **updateChatProperties**(`id`, `properties`): `Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

Updates chat properties

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `id` | `string` | chat to update properties |
| `properties` | [`Properties`](../interfaces/objects.Properties.md) | properties to update |

#### Returns

`Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

#### Defined in

[agent/web.ts:215](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L215)

___

### updateCustomer

▸ **updateCustomer**(`id`, `opts`): `Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

Updates Customer's properties.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `id` | `string` | ID of a customer to update |
| `opts` | [`CustomerParameters`](../interfaces/agent_structures.CustomerParameters.md) | properties to update |

#### Returns

`Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

#### Defined in

[agent/web.ts:339](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L339)

___

### updateEventProperties

▸ **updateEventProperties**(`chat_id`, `thread_id`, `event_id`, `properties`): `Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

Updates event properties

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `chat_id` | `string` | chat ID of event to update |
| `thread_id` | `string` | thread ID of event to update |
| `event_id` | `string` | event to update properties |
| `properties` | [`Properties`](../interfaces/objects.Properties.md) | properties to update |

#### Returns

`Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

#### Defined in

[agent/web.ts:263](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L263)

___

### updateThreadProperties

▸ **updateThreadProperties**(`chat_id`, `thread_id`, `properties`): `Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

Updates thread properties

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `chat_id` | `string` | chat ID of thread to update |
| `thread_id` | `string` | thread to update properties |
| `properties` | [`Properties`](../interfaces/objects.Properties.md) | properties to update |

#### Returns

`Promise`<[`EmptyResponse`](../interfaces/agent_structures.EmptyResponse.md)\>

#### Defined in

[agent/web.ts:234](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L234)

___

### uploadFile

▸ **uploadFile**(`file`, `filename`): `Promise`<[`UploadFileResponse`](../interfaces/agent_structures.UploadFileResponse.md)\>

Uploads a file to the server as a temporary file. It returns a URL that expires after 24 hours unless the URL is used in send_event.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `file` | `string` \| `Buffer` | path of file to upload or Buffer with content |
| `filename` | `string` | filename for uploaded file |

#### Returns

`Promise`<[`UploadFileResponse`](../interfaces/agent_structures.UploadFileResponse.md)\>

#### Defined in

[agent/web.ts:192](https://github.com/livechat/lc-sdk-js/blob/a3fdde0/src/agent/web.ts#L192)