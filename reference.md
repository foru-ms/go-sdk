# Reference
## Auth
<details><summary><code>client.Auth.Register(request) -> *foru_ms_sdk.PostAuthRegisterResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PostAuthRegisterRequest{
        Username: "username",
        Email: "email",
        Password: "password",
    }
client.Auth.Register(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**username:** `string` — Username
    
</dd>
</dl>

<dl>
<dd>

**email:** `string` — Email
    
</dd>
</dl>

<dl>
<dd>

**displayName:** `*string` — Display Name
    
</dd>
</dl>

<dl>
<dd>

**password:** `string` — Password (min 8 chars)
    
</dd>
</dl>

<dl>
<dd>

**roles:** `[]string` — Roles
    
</dd>
</dl>

<dl>
<dd>

**bio:** `*string` — Bio
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` — Extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Auth.Login(request) -> *foru_ms_sdk.PostAuthLoginResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PostAuthLoginRequest{
        Login: "login",
        Password: "password",
    }
client.Auth.Login(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**login:** `string` — Username or Email
    
</dd>
</dl>

<dl>
<dd>

**password:** `string` — Password
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Auth.GetCurrentUser() -> *foru_ms_sdk.GetAuthMeResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.Auth.GetCurrentUser(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Auth.RequestPasswordReset(request) -> *foru_ms_sdk.PostAuthForgotPasswordResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PostAuthForgotPasswordRequest{
        Email: "email",
    }
client.Auth.RequestPasswordReset(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**email:** `string` — User Email
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Auth.ResetPassword(request) -> *foru_ms_sdk.PostAuthResetPasswordResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PostAuthResetPasswordRequest{
        Password: "password",
    }
client.Auth.ResetPassword(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**password:** `string` — New Password (min 8 chars)
    
</dd>
</dl>

<dl>
<dd>

**oldPassword:** `*string` — Old Password (for change password)
    
</dd>
</dl>

<dl>
<dd>

**email:** `*string` — Email (required if using oldPassword)
    
</dd>
</dl>

<dl>
<dd>

**token:** `*string` — Reset Token
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Tags
<details><summary><code>client.Tags.ListAllTags() -> *foru_ms_sdk.GetTagsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetTagsRequest{}
client.Tags.ListAllTags(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**search:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Tags.CreateATag(request) -> *foru_ms_sdk.PostTagsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PostTagsRequest{
        Name: "name",
    }
client.Tags.CreateATag(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `string` — Tag name
    
</dd>
</dl>

<dl>
<dd>

**slug:** `*string` — Tag slug (unique identifier)
    
</dd>
</dl>

<dl>
<dd>

**description:** `*string` — Tag description
    
</dd>
</dl>

<dl>
<dd>

**color:** `*string` — Hex color code
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` — Extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Tags.GetATag(ID) -> *foru_ms_sdk.GetTagsIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetTagsIDRequest{
        ID: "id",
    }
client.Tags.GetATag(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Tags.DeleteATag(ID) -> *foru_ms_sdk.DeleteTagsIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteTagsIDRequest{
        ID: "id",
    }
client.Tags.DeleteATag(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Tags.UpdateATag(ID, request) -> *foru_ms_sdk.PatchTagsIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PatchTagsIDRequest{
        ID: "id",
    }
client.Tags.UpdateATag(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — Tag name
    
</dd>
</dl>

<dl>
<dd>

**slug:** `*string` — Tag slug (unique identifier)
    
</dd>
</dl>

<dl>
<dd>

**description:** `*string` — Tag description
    
</dd>
</dl>

<dl>
<dd>

**color:** `*string` — Hex color code
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` — Extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Tags.ListTagSubscribers(ID) -> *foru_ms_sdk.GetTagsIDSubscribersResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetTagsIDSubscribersRequest{
        ID: "id",
    }
client.Tags.ListTagSubscribers(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Tag ID
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Pagination cursor
    
</dd>
</dl>

<dl>
<dd>

**limit:** `*int` — Items per page
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Tags.GetASubscriberFromTag(ID, SubID) -> *foru_ms_sdk.GetTagsIDSubscribersSubIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetTagsIDSubscribersSubIDRequest{
        ID: "id",
        SubID: "subId",
    }
client.Tags.GetASubscriberFromTag(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Tag ID
    
</dd>
</dl>

<dl>
<dd>

**subID:** `string` — Subscriber ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Tags.DeleteASubscriberFromTag(ID, SubID) -> *foru_ms_sdk.DeleteTagsIDSubscribersSubIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteTagsIDSubscribersSubIDRequest{
        ID: "id",
        SubID: "subId",
    }
client.Tags.DeleteASubscriberFromTag(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Tag ID
    
</dd>
</dl>

<dl>
<dd>

**subID:** `string` — Subscriber ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Threads
<details><summary><code>client.Threads.ListAllThreads() -> *foru_ms_sdk.GetThreadsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetThreadsRequest{}
client.Threads.ListAllThreads(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**search:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Threads.CreateAThread(request) -> *foru_ms_sdk.PostThreadsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PostThreadsRequest{
        Title: "title",
        Body: "body",
    }
client.Threads.CreateAThread(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**title:** `string` — Thread title
    
</dd>
</dl>

<dl>
<dd>

**body:** `string` — Thread content (Markdown supported)
    
</dd>
</dl>

<dl>
<dd>

**userID:** `*string` — Author user ID (required for API key auth, ignored for JWT auth)
    
</dd>
</dl>

<dl>
<dd>

**tags:** `[]string` — List of tag slugs, names, or IDs to attach
    
</dd>
</dl>

<dl>
<dd>

**poll:** `*foru_ms_sdk.PostThreadsRequestPoll` — Poll data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Threads.GetAThread(ID) -> *foru_ms_sdk.GetThreadsIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetThreadsIDRequest{
        ID: "id",
    }
client.Threads.GetAThread(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Threads.DeleteAThread(ID) -> *foru_ms_sdk.DeleteThreadsIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteThreadsIDRequest{
        ID: "id",
    }
client.Threads.DeleteAThread(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Threads.UpdateAThread(ID, request) -> *foru_ms_sdk.PatchThreadsIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PatchThreadsIDRequest{
        ID: "id",
    }
client.Threads.UpdateAThread(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**title:** `*string` — New title
    
</dd>
</dl>

<dl>
<dd>

**body:** `*string` — New content
    
</dd>
</dl>

<dl>
<dd>

**locked:** `*bool` — Lock/unlock thread
    
</dd>
</dl>

<dl>
<dd>

**pinned:** `*bool` — Pin/unpin thread
    
</dd>
</dl>

<dl>
<dd>

**tags:** `[]string` — Update tags by slug, name, or ID
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` — Update extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Threads.ListThreadPosts(ID) -> *foru_ms_sdk.GetThreadsIDPostsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetThreadsIDPostsRequest{
        ID: "id",
    }
client.Threads.ListThreadPosts(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Thread ID
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Pagination cursor
    
</dd>
</dl>

<dl>
<dd>

**limit:** `*int` — Items per page
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Threads.GetAPostFromThread(ID, SubID) -> *foru_ms_sdk.GetThreadsIDPostsSubIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetThreadsIDPostsSubIDRequest{
        ID: "id",
        SubID: "subId",
    }
client.Threads.GetAPostFromThread(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Thread ID
    
</dd>
</dl>

<dl>
<dd>

**subID:** `string` — Post ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Threads.DeleteAPostFromThread(ID, SubID) -> *foru_ms_sdk.DeleteThreadsIDPostsSubIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteThreadsIDPostsSubIDRequest{
        ID: "id",
        SubID: "subId",
    }
client.Threads.DeleteAPostFromThread(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Thread ID
    
</dd>
</dl>

<dl>
<dd>

**subID:** `string` — Post ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Threads.ListThreadReactions(ID) -> *foru_ms_sdk.GetThreadsIDReactionsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetThreadsIDReactionsRequest{
        ID: "id",
    }
client.Threads.ListThreadReactions(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Thread ID
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Pagination cursor
    
</dd>
</dl>

<dl>
<dd>

**limit:** `*int` — Items per page
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Threads.CreateAReactionInThread(ID, request) -> *foru_ms_sdk.PostThreadsIDReactionsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PostThreadsIDReactionsRequest{
        ID: "id",
        Type: foru_ms_sdk.PostThreadsIDReactionsRequestTypeLike,
    }
client.Threads.CreateAReactionInThread(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Thread ID
    
</dd>
</dl>

<dl>
<dd>

**type_:** `*foru_ms_sdk.PostThreadsIDReactionsRequestType` — Type of reaction
    
</dd>
</dl>

<dl>
<dd>

**userID:** `*string` — User ID (required for API key auth, ignored for JWT auth)
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` — Additional custom data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Threads.RemoveYourReactionFromThread(ID) -> *foru_ms_sdk.DeleteThreadsIDReactionsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Removes the authenticated user's reaction. No subId needed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteThreadsIDReactionsRequest{
        ID: "id",
    }
client.Threads.RemoveYourReactionFromThread(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Thread ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Threads.GetAReactionFromThread(ID, SubID) -> *foru_ms_sdk.GetThreadsIDReactionsSubIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetThreadsIDReactionsSubIDRequest{
        ID: "id",
        SubID: "subId",
    }
client.Threads.GetAReactionFromThread(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Thread ID
    
</dd>
</dl>

<dl>
<dd>

**subID:** `string` — Reaction ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Threads.DeleteAReactionFromThread(ID, SubID) -> *foru_ms_sdk.DeleteThreadsIDReactionsSubIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteThreadsIDReactionsSubIDRequest{
        ID: "id",
        SubID: "subId",
    }
client.Threads.DeleteAReactionFromThread(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Thread ID
    
</dd>
</dl>

<dl>
<dd>

**subID:** `string` — Reaction ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Threads.ListThreadSubscribers(ID) -> *foru_ms_sdk.GetThreadsIDSubscribersResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetThreadsIDSubscribersRequest{
        ID: "id",
    }
client.Threads.ListThreadSubscribers(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Thread ID
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Pagination cursor
    
</dd>
</dl>

<dl>
<dd>

**limit:** `*int` — Items per page
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Threads.GetASubscriberFromThread(ID, SubID) -> *foru_ms_sdk.GetThreadsIDSubscribersSubIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetThreadsIDSubscribersSubIDRequest{
        ID: "id",
        SubID: "subId",
    }
client.Threads.GetASubscriberFromThread(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Thread ID
    
</dd>
</dl>

<dl>
<dd>

**subID:** `string` — Subscriber ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Threads.DeleteASubscriberFromThread(ID, SubID) -> *foru_ms_sdk.DeleteThreadsIDSubscribersSubIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteThreadsIDSubscribersSubIDRequest{
        ID: "id",
        SubID: "subId",
    }
client.Threads.DeleteASubscriberFromThread(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Thread ID
    
</dd>
</dl>

<dl>
<dd>

**subID:** `string` — Subscriber ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Threads.GetThreadPoll(ID) -> *foru_ms_sdk.GetThreadsIDPollResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetThreadsIDPollRequest{
        ID: "id",
    }
client.Threads.GetThreadPoll(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Thread ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Threads.CreateThreadPoll(ID, request) -> *foru_ms_sdk.PostThreadsIDPollResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PostThreadsIDPollRequest{
        ID: "id",
        Title: "title",
        Options: []*foru_ms_sdk.PostThreadsIDPollRequestOptionsItem{
            &foru_ms_sdk.PostThreadsIDPollRequestOptionsItem{
                Title: "title",
            },
        },
    }
client.Threads.CreateThreadPoll(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Thread ID
    
</dd>
</dl>

<dl>
<dd>

**title:** `string` — Poll question/title
    
</dd>
</dl>

<dl>
<dd>

**options:** `[]*foru_ms_sdk.PostThreadsIDPollRequestOptionsItem` — Poll options (2-20)
    
</dd>
</dl>

<dl>
<dd>

**expiresAt:** `*time.Time` — Optional expiration time
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` — Additional custom data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Threads.UpdateThreadPoll(ID, request) -> *foru_ms_sdk.PatchThreadsIDPollResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PatchThreadsIDPollRequest{
        ID: "id",
    }
client.Threads.UpdateThreadPoll(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Thread ID
    
</dd>
</dl>

<dl>
<dd>

**title:** `*string` — Poll question/title
    
</dd>
</dl>

<dl>
<dd>

**closed:** `*bool` — Close the poll
    
</dd>
</dl>

<dl>
<dd>

**expiresAt:** `*time.Time` — Optional expiration time
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` — Additional custom data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Posts
<details><summary><code>client.Posts.ListAllPosts() -> *foru_ms_sdk.GetPostsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetPostsRequest{}
client.Posts.ListAllPosts(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**search:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Posts.CreateAPost(request) -> *foru_ms_sdk.PostPostsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PostPostsRequest{
        ThreadID: "threadId",
        Body: "body",
    }
client.Posts.CreateAPost(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**threadID:** `string` — Thread ID to post in
    
</dd>
</dl>

<dl>
<dd>

**body:** `string` — Post content (Markdown supported)
    
</dd>
</dl>

<dl>
<dd>

**userID:** `*string` — Author user ID (required for API key auth, ignored for JWT auth)
    
</dd>
</dl>

<dl>
<dd>

**parentID:** `*string` — Parent post ID for threading
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Posts.GetAPost(ID) -> *foru_ms_sdk.GetPostsIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetPostsIDRequest{
        ID: "id",
    }
client.Posts.GetAPost(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Posts.DeleteAPost(ID) -> *foru_ms_sdk.DeletePostsIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeletePostsIDRequest{
        ID: "id",
    }
client.Posts.DeleteAPost(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Posts.UpdateAPost(ID, request) -> *foru_ms_sdk.PatchPostsIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PatchPostsIDRequest{
        ID: "id",
    }
client.Posts.UpdateAPost(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**body:** `*string` — Updated post content
    
</dd>
</dl>

<dl>
<dd>

**threadID:** `*string` — Move post to another thread
    
</dd>
</dl>

<dl>
<dd>

**parentID:** `*string` — Change parent post
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` — Update extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Posts.ListPostReactions(ID) -> *foru_ms_sdk.GetPostsIDReactionsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetPostsIDReactionsRequest{
        ID: "id",
    }
client.Posts.ListPostReactions(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Post ID
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Pagination cursor
    
</dd>
</dl>

<dl>
<dd>

**limit:** `*int` — Items per page
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Posts.CreateAReactionInPost(ID, request) -> *foru_ms_sdk.PostPostsIDReactionsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PostPostsIDReactionsRequest{
        ID: "id",
        Type: foru_ms_sdk.PostPostsIDReactionsRequestTypeLike,
    }
client.Posts.CreateAReactionInPost(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Post ID
    
</dd>
</dl>

<dl>
<dd>

**type_:** `*foru_ms_sdk.PostPostsIDReactionsRequestType` — Type of reaction
    
</dd>
</dl>

<dl>
<dd>

**userID:** `*string` — User ID (required for API key auth, ignored for JWT auth)
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` — Additional custom data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Posts.RemoveYourReactionFromPost(ID) -> *foru_ms_sdk.DeletePostsIDReactionsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Removes the authenticated user's reaction. No subId needed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeletePostsIDReactionsRequest{
        ID: "id",
    }
client.Posts.RemoveYourReactionFromPost(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Post ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Posts.GetAReactionFromPost(ID, SubID) -> *foru_ms_sdk.GetPostsIDReactionsSubIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetPostsIDReactionsSubIDRequest{
        ID: "id",
        SubID: "subId",
    }
client.Posts.GetAReactionFromPost(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Post ID
    
</dd>
</dl>

<dl>
<dd>

**subID:** `string` — Reaction ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Posts.DeleteAReactionFromPost(ID, SubID) -> *foru_ms_sdk.DeletePostsIDReactionsSubIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeletePostsIDReactionsSubIDRequest{
        ID: "id",
        SubID: "subId",
    }
client.Posts.DeleteAReactionFromPost(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Post ID
    
</dd>
</dl>

<dl>
<dd>

**subID:** `string` — Reaction ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Posts.ListPostPosts(ID) -> *foru_ms_sdk.GetPostsIDPostsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetPostsIDPostsRequest{
        ID: "id",
    }
client.Posts.ListPostPosts(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Post ID
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Pagination cursor
    
</dd>
</dl>

<dl>
<dd>

**limit:** `*int` — Items per page
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Posts.GetAPostFromPost(ID, SubID) -> *foru_ms_sdk.GetPostsIDPostsSubIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetPostsIDPostsSubIDRequest{
        ID: "id",
        SubID: "subId",
    }
client.Posts.GetAPostFromPost(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Post ID
    
</dd>
</dl>

<dl>
<dd>

**subID:** `string` — Post ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Posts.DeleteAPostFromPost(ID, SubID) -> *foru_ms_sdk.DeletePostsIDPostsSubIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeletePostsIDPostsSubIDRequest{
        ID: "id",
        SubID: "subId",
    }
client.Posts.DeleteAPostFromPost(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Post ID
    
</dd>
</dl>

<dl>
<dd>

**subID:** `string` — Post ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## PrivateMessages
<details><summary><code>client.PrivateMessages.ListAllPrivateMessages() -> *foru_ms_sdk.GetPrivateMessagesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetPrivateMessagesRequest{}
client.PrivateMessages.ListAllPrivateMessages(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**search:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PrivateMessages.CreateAPrivateMessage(request) -> *foru_ms_sdk.PostPrivateMessagesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PostPrivateMessagesRequest{
        RecipientID: "recipientId",
        Body: "body",
    }
client.PrivateMessages.CreateAPrivateMessage(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**recipientID:** `string` — Recipient User ID
    
</dd>
</dl>

<dl>
<dd>

**senderID:** `*string` — Sender user ID (required for API key auth, ignored for JWT auth)
    
</dd>
</dl>

<dl>
<dd>

**title:** `*string` — Message title (optional for replies)
    
</dd>
</dl>

<dl>
<dd>

**body:** `string` — Message content
    
</dd>
</dl>

<dl>
<dd>

**parentID:** `*string` — Parent Message ID (for replies)
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` — Extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PrivateMessages.GetAPrivateMessage(ID) -> *foru_ms_sdk.GetPrivateMessagesIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetPrivateMessagesIDRequest{
        ID: "id",
    }
client.PrivateMessages.GetAPrivateMessage(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PrivateMessages.DeleteAPrivateMessage(ID) -> *foru_ms_sdk.DeletePrivateMessagesIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeletePrivateMessagesIDRequest{
        ID: "id",
    }
client.PrivateMessages.DeleteAPrivateMessage(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PrivateMessages.ListPrivateMessageReplies(ID) -> *foru_ms_sdk.GetPrivateMessagesIDRepliesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetPrivateMessagesIDRepliesRequest{
        ID: "id",
    }
client.PrivateMessages.ListPrivateMessageReplies(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Private Message ID
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Pagination cursor
    
</dd>
</dl>

<dl>
<dd>

**limit:** `*int` — Items per page
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PrivateMessages.CreateAReplyInPrivateMessage(ID, request) -> *foru_ms_sdk.PostPrivateMessagesIDRepliesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PostPrivateMessagesIDRepliesRequest{
        ID: "id",
        RecipientID: "recipientId",
        Body: "body",
    }
client.PrivateMessages.CreateAReplyInPrivateMessage(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Private Message ID
    
</dd>
</dl>

<dl>
<dd>

**recipientID:** `string` — Recipient User ID
    
</dd>
</dl>

<dl>
<dd>

**senderID:** `*string` — Sender user ID (required for API key auth, ignored for JWT auth)
    
</dd>
</dl>

<dl>
<dd>

**title:** `*string` — Message title (optional for replies)
    
</dd>
</dl>

<dl>
<dd>

**body:** `string` — Message content
    
</dd>
</dl>

<dl>
<dd>

**parentID:** `*string` — Parent Message ID (for replies)
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` — Extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PrivateMessages.GetAReplyFromPrivateMessage(ID, SubID) -> *foru_ms_sdk.GetPrivateMessagesIDRepliesSubIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetPrivateMessagesIDRepliesSubIDRequest{
        ID: "id",
        SubID: "subId",
    }
client.PrivateMessages.GetAReplyFromPrivateMessage(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Private Message ID
    
</dd>
</dl>

<dl>
<dd>

**subID:** `string` — Reply ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PrivateMessages.DeleteAReplyFromPrivateMessage(ID, SubID) -> *foru_ms_sdk.DeletePrivateMessagesIDRepliesSubIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeletePrivateMessagesIDRepliesSubIDRequest{
        ID: "id",
        SubID: "subId",
    }
client.PrivateMessages.DeleteAReplyFromPrivateMessage(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Private Message ID
    
</dd>
</dl>

<dl>
<dd>

**subID:** `string` — Reply ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Users
<details><summary><code>client.Users.ListAllUsers() -> *foru_ms_sdk.GetUsersResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetUsersRequest{}
client.Users.ListAllUsers(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**search:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Users.GetAUser(ID) -> *foru_ms_sdk.GetUsersIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetUsersIDRequest{
        ID: "id",
    }
client.Users.GetAUser(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Users.DeleteAUser(ID) -> *foru_ms_sdk.DeleteUsersIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteUsersIDRequest{
        ID: "id",
    }
client.Users.DeleteAUser(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Users.UpdateAUser(ID, request) -> *foru_ms_sdk.PatchUsersIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PatchUsersIDRequest{
        ID: "id",
    }
client.Users.UpdateAUser(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**displayName:** `*string` — Display name
    
</dd>
</dl>

<dl>
<dd>

**bio:** `*string` — User bio
    
</dd>
</dl>

<dl>
<dd>

**signature:** `*string` — Forum signature
    
</dd>
</dl>

<dl>
<dd>

**username:** `*string` — Username (letters, numbers, underscores, hyphens)
    
</dd>
</dl>

<dl>
<dd>

**email:** `*string` — Email address
    
</dd>
</dl>

<dl>
<dd>

**password:** `*string` — New password
    
</dd>
</dl>

<dl>
<dd>

**url:** `*string` — Website URL
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` — Extended data
    
</dd>
</dl>

<dl>
<dd>

**roles:** `[]string` — Role slugs (admin only)
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Users.ListUserFollowers(ID) -> *foru_ms_sdk.GetUsersIDFollowersResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetUsersIDFollowersRequest{
        ID: "id",
    }
client.Users.ListUserFollowers(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — User ID
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Pagination cursor
    
</dd>
</dl>

<dl>
<dd>

**limit:** `*int` — Items per page
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Users.GetAFollowerFromUser(ID, SubID) -> *foru_ms_sdk.GetUsersIDFollowersSubIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetUsersIDFollowersSubIDRequest{
        ID: "id",
        SubID: "subId",
    }
client.Users.GetAFollowerFromUser(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — User ID
    
</dd>
</dl>

<dl>
<dd>

**subID:** `string` — Follower ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Users.DeleteAFollowerFromUser(ID, SubID) -> *foru_ms_sdk.DeleteUsersIDFollowersSubIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteUsersIDFollowersSubIDRequest{
        ID: "id",
        SubID: "subId",
    }
client.Users.DeleteAFollowerFromUser(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — User ID
    
</dd>
</dl>

<dl>
<dd>

**subID:** `string` — Follower ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Users.ListUserFollowing(ID) -> *foru_ms_sdk.GetUsersIDFollowingResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetUsersIDFollowingRequest{
        ID: "id",
    }
client.Users.ListUserFollowing(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — User ID
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Pagination cursor
    
</dd>
</dl>

<dl>
<dd>

**limit:** `*int` — Items per page
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Users.GetAFollowingFromUser(ID, SubID) -> *foru_ms_sdk.GetUsersIDFollowingSubIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetUsersIDFollowingSubIDRequest{
        ID: "id",
        SubID: "subId",
    }
client.Users.GetAFollowingFromUser(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — User ID
    
</dd>
</dl>

<dl>
<dd>

**subID:** `string` — Following ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Users.DeleteAFollowingFromUser(ID, SubID) -> *foru_ms_sdk.DeleteUsersIDFollowingSubIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteUsersIDFollowingSubIDRequest{
        ID: "id",
        SubID: "subId",
    }
client.Users.DeleteAFollowingFromUser(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — User ID
    
</dd>
</dl>

<dl>
<dd>

**subID:** `string` — Following ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Roles
<details><summary><code>client.Roles.ListAllRoles() -> *foru_ms_sdk.GetRolesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetRolesRequest{}
client.Roles.ListAllRoles(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**search:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Roles.CreateARole(request) -> *foru_ms_sdk.PostRolesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PostRolesRequest{
        Name: "name",
    }
client.Roles.CreateARole(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `string` — Role name
    
</dd>
</dl>

<dl>
<dd>

**slug:** `*string` — Role slug (unique identifier)
    
</dd>
</dl>

<dl>
<dd>

**description:** `*string` — Role description
    
</dd>
</dl>

<dl>
<dd>

**color:** `*string` — Role color hex
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` — Extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Roles.GetARole(ID) -> *foru_ms_sdk.GetRolesIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetRolesIDRequest{
        ID: "id",
    }
client.Roles.GetARole(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Roles.DeleteARole(ID) -> *foru_ms_sdk.DeleteRolesIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteRolesIDRequest{
        ID: "id",
    }
client.Roles.DeleteARole(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Roles.UpdateARole(ID, request) -> *foru_ms_sdk.PatchRolesIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PatchRolesIDRequest{
        ID: "id",
    }
client.Roles.UpdateARole(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — Role name
    
</dd>
</dl>

<dl>
<dd>

**slug:** `*string` — Role slug (unique identifier)
    
</dd>
</dl>

<dl>
<dd>

**description:** `*string` — Role description
    
</dd>
</dl>

<dl>
<dd>

**color:** `*string` — Role color hex
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` — Extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Reports
<details><summary><code>client.Reports.ListAllReports() -> *foru_ms_sdk.GetReportsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetReportsRequest{}
client.Reports.ListAllReports(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**search:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Reports.CreateAReport(request) -> *foru_ms_sdk.PostReportsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PostReportsRequest{
        Type: "type",
    }
client.Reports.CreateAReport(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**type_:** `string` — Report type (e.g. spam, abuse)
    
</dd>
</dl>

<dl>
<dd>

**description:** `*string` — Reason for reporting
    
</dd>
</dl>

<dl>
<dd>

**userID:** `*string` — Reporter user ID (required for API key auth, ignored for JWT auth)
    
</dd>
</dl>

<dl>
<dd>

**reportedID:** `*string` — ID of user being reported
    
</dd>
</dl>

<dl>
<dd>

**threadID:** `*string` — ID of thread being reported
    
</dd>
</dl>

<dl>
<dd>

**postID:** `*string` — ID of post being reported
    
</dd>
</dl>

<dl>
<dd>

**privateMessageID:** `*string` — ID of private message being reported
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Reports.GetAReport(ID) -> *foru_ms_sdk.GetReportsIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetReportsIDRequest{
        ID: "id",
    }
client.Reports.GetAReport(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Reports.DeleteAReport(ID) -> *foru_ms_sdk.DeleteReportsIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteReportsIDRequest{
        ID: "id",
    }
client.Reports.DeleteAReport(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Notifications
<details><summary><code>client.Notifications.ListAllNotifications() -> *foru_ms_sdk.GetNotificationsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetNotificationsRequest{}
client.Notifications.ListAllNotifications(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**search:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Notifications.CreateANotification(request) -> *foru_ms_sdk.PostNotificationsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PostNotificationsRequest{
        UserID: "userId",
        Type: "type",
    }
client.Notifications.CreateANotification(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**userID:** `string` — Target user ID to receive notification (maps to userId)
    
</dd>
</dl>

<dl>
<dd>

**notifierID:** `*string` — User ID who triggered the notification (optional, defaults to authenticated user)
    
</dd>
</dl>

<dl>
<dd>

**type_:** `string` — Notification type (e.g. mention, reply, follow)
    
</dd>
</dl>

<dl>
<dd>

**description:** `*string` — Notification text content
    
</dd>
</dl>

<dl>
<dd>

**threadID:** `*string` — Related thread ID
    
</dd>
</dl>

<dl>
<dd>

**postID:** `*string` — Related post ID
    
</dd>
</dl>

<dl>
<dd>

**privateMessageID:** `*string` — Related private message ID
    
</dd>
</dl>

<dl>
<dd>

**status:** `*foru_ms_sdk.PostNotificationsRequestStatus` — Initial notification status
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` — Additional notification data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Notifications.GetANotification(ID) -> *foru_ms_sdk.GetNotificationsIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetNotificationsIDRequest{
        ID: "id",
    }
client.Notifications.GetANotification(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Notifications.DeleteANotification(ID) -> *foru_ms_sdk.DeleteNotificationsIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteNotificationsIDRequest{
        ID: "id",
    }
client.Notifications.DeleteANotification(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Notifications.UpdateANotification(ID, request) -> *foru_ms_sdk.PatchNotificationsIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PatchNotificationsIDRequest{
        ID: "id",
    }
client.Notifications.UpdateANotification(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**status:** `*foru_ms_sdk.PatchNotificationsIDRequestStatus` — Notification status
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` — Update extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Webhooks
<details><summary><code>client.Webhooks.ListAllWebhooks() -> *foru_ms_sdk.GetWebhooksResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetWebhooksRequest{}
client.Webhooks.ListAllWebhooks(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**search:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Webhooks.CreateAWebhook(request) -> *foru_ms_sdk.PostWebhooksResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PostWebhooksRequest{
        Name: "name",
        URL: "url",
        Events: []string{
            "events",
        },
    }
client.Webhooks.CreateAWebhook(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `string` — Webhook name
    
</dd>
</dl>

<dl>
<dd>

**url:** `string` — Target URL
    
</dd>
</dl>

<dl>
<dd>

**events:** `[]string` — List of event types (e.g. post.created)
    
</dd>
</dl>

<dl>
<dd>

**secret:** `*string` — Secret for signature verification (auto-generated if missing)
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Webhooks.GetAWebhook(ID) -> *foru_ms_sdk.GetWebhooksIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetWebhooksIDRequest{
        ID: "id",
    }
client.Webhooks.GetAWebhook(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Webhooks.DeleteAWebhook(ID) -> *foru_ms_sdk.DeleteWebhooksIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteWebhooksIDRequest{
        ID: "id",
    }
client.Webhooks.DeleteAWebhook(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Webhooks.ListWebhookDeliveries(ID) -> *foru_ms_sdk.GetWebhooksIDDeliveriesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetWebhooksIDDeliveriesRequest{
        ID: "id",
    }
client.Webhooks.ListWebhookDeliveries(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Webhook ID
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Pagination cursor
    
</dd>
</dl>

<dl>
<dd>

**limit:** `*int` — Items per page
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Webhooks.GetADeliveryFromWebhook(ID, SubID) -> *foru_ms_sdk.GetWebhooksIDDeliveriesSubIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetWebhooksIDDeliveriesSubIDRequest{
        ID: "id",
        SubID: "subId",
    }
client.Webhooks.GetADeliveryFromWebhook(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Webhook ID
    
</dd>
</dl>

<dl>
<dd>

**subID:** `string` — Delivery ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Webhooks.DeleteADeliveryFromWebhook(ID, SubID) -> *foru_ms_sdk.DeleteWebhooksIDDeliveriesSubIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteWebhooksIDDeliveriesSubIDRequest{
        ID: "id",
        SubID: "subId",
    }
client.Webhooks.DeleteADeliveryFromWebhook(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — Webhook ID
    
</dd>
</dl>

<dl>
<dd>

**subID:** `string` — Delivery ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Integrations
<details><summary><code>client.Integrations.ListAllIntegrations() -> *foru_ms_sdk.GetIntegrationsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetIntegrationsRequest{}
client.Integrations.ListAllIntegrations(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**search:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Integrations.CreateAnIntegration(request) -> *foru_ms_sdk.PostIntegrationsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PostIntegrationsRequest{
        Type: "type",
        Config: map[string]any{
            "key": "value",
        },
    }
client.Integrations.CreateAnIntegration(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**type_:** `string` — Integration type (e.g. slack, discord)
    
</dd>
</dl>

<dl>
<dd>

**config:** `map[string]any` — JSON configuration
    
</dd>
</dl>

<dl>
<dd>

**enabled:** `*bool` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Integrations.GetAnIntegration(ID) -> *foru_ms_sdk.GetIntegrationsIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetIntegrationsIDRequest{
        ID: "id",
    }
client.Integrations.GetAnIntegration(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Integrations.DeleteAnIntegration(ID) -> *foru_ms_sdk.DeleteIntegrationsIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteIntegrationsIDRequest{
        ID: "id",
    }
client.Integrations.DeleteAnIntegration(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Integrations.UpdateAnIntegration(ID, request) -> *foru_ms_sdk.PatchIntegrationsIDResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PatchIntegrationsIDRequest{
        ID: "id",
    }
client.Integrations.UpdateAnIntegration(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — Integration name
    
</dd>
</dl>

<dl>
<dd>

**config:** `map[string]any` — JSON configuration (merged with existing)
    
</dd>
</dl>

<dl>
<dd>

**active:** `*bool` — Enable/disable integration
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## SsOs
<details><summary><code>client.SsOs.ListAllSsOs() -> *foru_ms_sdk.GetSSOResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetSSORequest{}
client.SsOs.ListAllSsOs(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**search:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.SsOs.CreateAnSSO(request) -> *foru_ms_sdk.PostSSOResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PostSSORequest{
        Name: "name",
        ClientID: "clientId",
        ClientSecret: "clientSecret",
        Issuer: "issuer",
        AuthorizationEndpoint: "authorizationEndpoint",
        TokenEndpoint: "tokenEndpoint",
        UserInfoEndpoint: "userInfoEndpoint",
    }
client.SsOs.CreateAnSSO(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `string` — Provider name (e.g. Google)
    
</dd>
</dl>

<dl>
<dd>

**clientID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**clientSecret:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**issuer:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**authorizationEndpoint:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**tokenEndpoint:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**userInfoEndpoint:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.SsOs.GetAnSSO(ID) -> *foru_ms_sdk.GetSsoIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.GetSsoIdRequest{
        ID: "id",
    }
client.SsOs.GetAnSSO(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.SsOs.DeleteAnSSO(ID) -> *foru_ms_sdk.DeleteSsoIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteSsoIdRequest{
        ID: "id",
    }
client.SsOs.DeleteAnSSO(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.SsOs.UpdateAnSSO(ID, request) -> *foru_ms_sdk.PatchSsoIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.PatchSsoIdRequest{
        ID: "id",
    }
client.SsOs.UpdateAnSSO(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — Provider name
    
</dd>
</dl>

<dl>
<dd>

**domain:** `*string` — Email domain to match
    
</dd>
</dl>

<dl>
<dd>

**clientID:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**clientSecret:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**issuer:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**authorizationEndpoint:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**tokenEndpoint:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**userInfoEndpoint:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**active:** `*bool` — Enable/disable provider
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>
