# Reference
## Auth
<details><summary><code>client.Auth.Register(request) -> *foru_ms_sdk.RegisterResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Register a new user in your forum instance. Requires API key for instance identification. Returns a JWT token for subsequent authenticated requests.
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
request := &foru_ms_sdk.RegisterAuthRequest{
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

<details><summary><code>client.Auth.Login(request) -> *foru_ms_sdk.LoginResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Authenticate an existing user. Requires API key for instance identification. Returns a JWT token for subsequent authenticated requests.
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
request := &foru_ms_sdk.LoginAuthRequest{
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

<details><summary><code>client.Auth.Me() -> *foru_ms_sdk.MeResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.Auth.Me(
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

<details><summary><code>client.Auth.ForgotPassword(request) -> *foru_ms_sdk.ForgotPasswordResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Request a password reset email. Requires API key for instance identification.
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
request := &foru_ms_sdk.ForgotPasswordAuthRequest{
        Email: "email",
    }
client.Auth.ForgotPassword(
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

<details><summary><code>client.Auth.ResetPassword(request) -> *foru_ms_sdk.ResetPasswordResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Reset password using a reset token. Requires API key for instance identification.
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
request := &foru_ms_sdk.ResetPasswordAuthRequest{
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

## Search
<details><summary><code>client.Search.Search() -> *foru_ms_sdk.SearchSearchResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.Search.Search(
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

## Tags
<details><summary><code>client.Tags.List() -> *foru_ms_sdk.TagListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of tags. Use cursor for pagination.
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
request := &foru_ms_sdk.ListTagsRequest{}
client.Tags.List(
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

**limit:** `*int` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Cursor for pagination
    
</dd>
</dl>

<dl>
<dd>

**search:** `*string` — Search tags by name or description
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Tags.Create(request) -> *foru_ms_sdk.TagResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new tag.
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
request := &foru_ms_sdk.CreateTagsRequest{
        Name: "name",
    }
client.Tags.Create(
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

<details><summary><code>client.Tags.Retrieve(ID) -> *foru_ms_sdk.TagResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a tag by ID or slug (if supported).
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
request := &foru_ms_sdk.RetrieveTagsRequest{
        ID: "id",
    }
client.Tags.Retrieve(
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
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Tags.Delete(ID) -> *foru_ms_sdk.SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete a tag.
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
request := &foru_ms_sdk.DeleteTagsRequest{
        ID: "id",
    }
client.Tags.Delete(
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
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Tags.Update(ID, request) -> *foru_ms_sdk.UpdateTagsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing tag. Only provided fields will be modified.
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
request := &foru_ms_sdk.UpdateTagsRequest{
        ID: "id",
    }
client.Tags.Update(
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

<details><summary><code>client.Tags.ListSubscribers(ID) -> *foru_ms_sdk.TagSubscriberListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of subscribers for Tag.
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
request := &foru_ms_sdk.ListSubscribersTagsRequest{
        ID: "id",
    }
client.Tags.ListSubscribers(
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

**limit:** `*int` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Cursor for pagination
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Tags.RetrieveSubscriber(ID, SubID) -> *foru_ms_sdk.RetrieveSubscriberTagsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.RetrieveSubscriberTagsRequest{
        ID: "id",
        SubID: "subId",
    }
client.Tags.RetrieveSubscriber(
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

<details><summary><code>client.Tags.DeleteSubscriber(ID, SubID) -> *foru_ms_sdk.SuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteSubscriberTagsRequest{
        ID: "id",
        SubID: "subId",
    }
client.Tags.DeleteSubscriber(
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
<details><summary><code>client.Threads.List() -> *foru_ms_sdk.ThreadListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of threads. Use cursor for pagination.
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
request := &foru_ms_sdk.ListThreadsRequest{}
client.Threads.List(
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

**limit:** `*int` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Cursor for pagination
    
</dd>
</dl>

<dl>
<dd>

**search:** `*string` — Search term for title
    
</dd>
</dl>

<dl>
<dd>

**tagID:** `*string` — Filter by tag ID
    
</dd>
</dl>

<dl>
<dd>

**userID:** `*string` — Filter by author ID
    
</dd>
</dl>

<dl>
<dd>

**sort:** `*foru_ms_sdk.ListThreadsRequestSort` — Sort criteria
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Threads.Create(request) -> *foru_ms_sdk.ThreadResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new thread.
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
request := &foru_ms_sdk.CreateThreadsRequest{
        Title: "title",
        Body: "body",
    }
client.Threads.Create(
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

**poll:** `*foru_ms_sdk.CreateThreadsRequestPoll` — Poll data
    
</dd>
</dl>

<dl>
<dd>

**locked:** `*bool` — Lock thread on creation
    
</dd>
</dl>

<dl>
<dd>

**pinned:** `*bool` — Pin thread on creation
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` — Custom extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Threads.Retrieve(ID) -> *foru_ms_sdk.ThreadResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a thread by ID or slug (if supported).
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
request := &foru_ms_sdk.RetrieveThreadsRequest{
        ID: "id",
    }
client.Threads.Retrieve(
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

<details><summary><code>client.Threads.Delete(ID) -> *foru_ms_sdk.SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete a thread.
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
request := &foru_ms_sdk.DeleteThreadsRequest{
        ID: "id",
    }
client.Threads.Delete(
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

<details><summary><code>client.Threads.Update(ID, request) -> *foru_ms_sdk.UpdateThreadsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing thread. Only provided fields will be modified.
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
request := &foru_ms_sdk.UpdateThreadsRequest{
        ID: "id",
    }
client.Threads.Update(
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

<details><summary><code>client.Threads.ListPosts(ID) -> *foru_ms_sdk.ThreadPostListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of posts for Thread.
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
request := &foru_ms_sdk.ListPostsThreadsRequest{
        ID: "id",
    }
client.Threads.ListPosts(
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

**limit:** `*int` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Cursor for pagination
    
</dd>
</dl>

<dl>
<dd>

**userID:** `*string` — Filter posts by author ID
    
</dd>
</dl>

<dl>
<dd>

**sort:** `*foru_ms_sdk.ListPostsThreadsRequestSort` — Sort posts by creation time
    
</dd>
</dl>

<dl>
<dd>

**search:** `*string` — Search within post body
    
</dd>
</dl>

<dl>
<dd>

**type_:** `*foru_ms_sdk.ListPostsThreadsRequestType` — Filter by interaction type
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Threads.RetrievePost(ID, SubID) -> *foru_ms_sdk.RetrievePostThreadsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.RetrievePostThreadsRequest{
        ID: "id",
        SubID: "subId",
    }
client.Threads.RetrievePost(
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

<details><summary><code>client.Threads.DeletePost(ID, SubID) -> *foru_ms_sdk.SuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeletePostThreadsRequest{
        ID: "id",
        SubID: "subId",
    }
client.Threads.DeletePost(
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

<details><summary><code>client.Threads.ListReactions(ID) -> *foru_ms_sdk.ThreadReactionListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of reactions for Thread.
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
request := &foru_ms_sdk.ListReactionsThreadsRequest{
        ID: "id",
    }
client.Threads.ListReactions(
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

**limit:** `*int` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Cursor for pagination
    
</dd>
</dl>

<dl>
<dd>

**type_:** `*foru_ms_sdk.ListReactionsThreadsRequestType` — Filter by reaction type
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Threads.CreateReaction(ID, request) -> *foru_ms_sdk.ThreadReactionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a Reaction in Thread.
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
request := &foru_ms_sdk.CreateReactionThreadsRequest{
        ID: "id",
        Type: foru_ms_sdk.CreateReactionThreadsRequestTypeLike,
    }
client.Threads.CreateReaction(
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

**type_:** `*foru_ms_sdk.CreateReactionThreadsRequestType` — Type of reaction
    
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

<details><summary><code>client.Threads.DeleteReaction(ID, SubID) -> *foru_ms_sdk.SuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteReactionThreadsRequest{
        ID: "id",
        SubID: "subId",
    }
client.Threads.DeleteReaction(
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

<details><summary><code>client.Threads.RetrieveReaction(ID, SubID) -> *foru_ms_sdk.RetrieveReactionThreadsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.RetrieveReactionThreadsRequest{
        ID: "id",
        SubID: "subId",
    }
client.Threads.RetrieveReaction(
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

<details><summary><code>client.Threads.ListSubscribers(ID) -> *foru_ms_sdk.ThreadSubscriberListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of subscribers for Thread.
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
request := &foru_ms_sdk.ListSubscribersThreadsRequest{
        ID: "id",
    }
client.Threads.ListSubscribers(
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

**limit:** `*int` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Cursor for pagination
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Threads.RetrieveSubscriber(ID, SubID) -> *foru_ms_sdk.RetrieveSubscriberThreadsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.RetrieveSubscriberThreadsRequest{
        ID: "id",
        SubID: "subId",
    }
client.Threads.RetrieveSubscriber(
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

<details><summary><code>client.Threads.DeleteSubscriber(ID, SubID) -> *foru_ms_sdk.SuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteSubscriberThreadsRequest{
        ID: "id",
        SubID: "subId",
    }
client.Threads.DeleteSubscriber(
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

<details><summary><code>client.Threads.RetrievePoll(ID) -> *foru_ms_sdk.ThreadPollResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.RetrievePollThreadsRequest{
        ID: "id",
    }
client.Threads.RetrievePoll(
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

<details><summary><code>client.Threads.CreatePoll(ID, request) -> *foru_ms_sdk.ThreadPollResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.CreatePollThreadsRequest{
        ID: "id",
        Title: "title",
        Options: []*foru_ms_sdk.CreatePollThreadsRequestOptionsItem{
            &foru_ms_sdk.CreatePollThreadsRequestOptionsItem{
                Title: "title",
            },
        },
    }
client.Threads.CreatePoll(
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

**options:** `[]*foru_ms_sdk.CreatePollThreadsRequestOptionsItem` — Poll options (2-20)
    
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

<details><summary><code>client.Threads.UpdatePoll(ID, request) -> *foru_ms_sdk.ThreadPollResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.UpdatePollThreadsRequest{
        ID: "id",
    }
client.Threads.UpdatePoll(
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
<details><summary><code>client.Posts.List() -> *foru_ms_sdk.PostListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of posts. Use cursor for pagination.
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
request := &foru_ms_sdk.ListPostsRequest{}
client.Posts.List(
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

**limit:** `*int` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Cursor for pagination
    
</dd>
</dl>

<dl>
<dd>

**userID:** `*string` — Filter posts by author ID
    
</dd>
</dl>

<dl>
<dd>

**sort:** `*foru_ms_sdk.ListPostsRequestSort` — Sort posts by creation time
    
</dd>
</dl>

<dl>
<dd>

**search:** `*string` — Search within post body
    
</dd>
</dl>

<dl>
<dd>

**type_:** `*foru_ms_sdk.ListPostsRequestType` — Filter by interaction type
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Posts.Create(request) -> *foru_ms_sdk.PostResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new post.
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
request := &foru_ms_sdk.CreatePostsRequest{
        ThreadID: "threadId",
        Body: "body",
    }
client.Posts.Create(
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

<details><summary><code>client.Posts.Retrieve(ID) -> *foru_ms_sdk.PostResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a post by ID or slug (if supported).
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
request := &foru_ms_sdk.RetrievePostsRequest{
        ID: "id",
    }
client.Posts.Retrieve(
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

<details><summary><code>client.Posts.Delete(ID) -> *foru_ms_sdk.SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete a post.
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
request := &foru_ms_sdk.DeletePostsRequest{
        ID: "id",
    }
client.Posts.Delete(
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

<details><summary><code>client.Posts.Update(ID, request) -> *foru_ms_sdk.UpdatePostsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing post. Only provided fields will be modified.
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
request := &foru_ms_sdk.UpdatePostsRequest{
        ID: "id",
    }
client.Posts.Update(
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

<details><summary><code>client.Posts.ListReactions(ID) -> *foru_ms_sdk.PostReactionListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of reactions for Post.
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
request := &foru_ms_sdk.ListReactionsPostsRequest{
        ID: "id",
    }
client.Posts.ListReactions(
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

**limit:** `*int` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Cursor for pagination
    
</dd>
</dl>

<dl>
<dd>

**type_:** `*foru_ms_sdk.ListReactionsPostsRequestType` — Filter by reaction type
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Posts.CreateReaction(ID, request) -> *foru_ms_sdk.PostReactionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a Reaction in Post.
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
request := &foru_ms_sdk.CreateReactionPostsRequest{
        ID: "id",
        Type: foru_ms_sdk.CreateReactionPostsRequestTypeLike,
    }
client.Posts.CreateReaction(
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

**type_:** `*foru_ms_sdk.CreateReactionPostsRequestType` — Type of reaction
    
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

<details><summary><code>client.Posts.DeleteReaction(ID, SubID) -> *foru_ms_sdk.SuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteReactionPostsRequest{
        ID: "id",
        SubID: "subId",
    }
client.Posts.DeleteReaction(
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

<details><summary><code>client.Posts.RetrieveReaction(ID, SubID) -> *foru_ms_sdk.RetrieveReactionPostsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.RetrieveReactionPostsRequest{
        ID: "id",
        SubID: "subId",
    }
client.Posts.RetrieveReaction(
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

<details><summary><code>client.Posts.ListPosts(ID) -> *foru_ms_sdk.PostPostListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of posts for Post.
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
request := &foru_ms_sdk.ListPostsPostsRequest{
        ID: "id",
    }
client.Posts.ListPosts(
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

**limit:** `*int` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Cursor for pagination
    
</dd>
</dl>

<dl>
<dd>

**userID:** `*string` — Filter posts by author ID
    
</dd>
</dl>

<dl>
<dd>

**sort:** `*foru_ms_sdk.ListPostsPostsRequestSort` — Sort posts by creation time
    
</dd>
</dl>

<dl>
<dd>

**search:** `*string` — Search within post body
    
</dd>
</dl>

<dl>
<dd>

**type_:** `*foru_ms_sdk.ListPostsPostsRequestType` — Filter by interaction type
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Posts.RetrievePost(ID, SubID) -> *foru_ms_sdk.RetrievePostPostsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.RetrievePostPostsRequest{
        ID: "id",
        SubID: "subId",
    }
client.Posts.RetrievePost(
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

<details><summary><code>client.Posts.DeletePost(ID, SubID) -> *foru_ms_sdk.SuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeletePostPostsRequest{
        ID: "id",
        SubID: "subId",
    }
client.Posts.DeletePost(
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

## Private Messages
<details><summary><code>client.PrivateMessages.List() -> *foru_ms_sdk.PrivateMessageListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of private messages. Use cursor for pagination.
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
request := &foru_ms_sdk.ListPrivateMessagesRequest{}
client.PrivateMessages.List(
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

**limit:** `*int` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Cursor for pagination
    
</dd>
</dl>

<dl>
<dd>

**query:** `*string` — Search query (title or body)
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PrivateMessages.Create(request) -> *foru_ms_sdk.PrivateMessageResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new private message.
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
request := &foru_ms_sdk.CreatePrivateMessagesRequest{
        RecipientID: "recipientId",
        Body: "body",
    }
client.PrivateMessages.Create(
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

<details><summary><code>client.PrivateMessages.Retrieve(ID) -> *foru_ms_sdk.PrivateMessageResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a private message by ID or slug (if supported).
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
request := &foru_ms_sdk.RetrievePrivateMessagesRequest{
        ID: "id",
    }
client.PrivateMessages.Retrieve(
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
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PrivateMessages.Delete(ID) -> *foru_ms_sdk.SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete a private message.
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
request := &foru_ms_sdk.DeletePrivateMessagesRequest{
        ID: "id",
    }
client.PrivateMessages.Delete(
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
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PrivateMessages.Update(ID, request) -> *foru_ms_sdk.UpdatePrivateMessagesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing private message. Only provided fields will be modified.
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
request := &foru_ms_sdk.UpdatePrivateMessagesRequest{
        ID: "id",
    }
client.PrivateMessages.Update(
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

**body:** `*string` — Message content
    
</dd>
</dl>

<dl>
<dd>

**status:** `*string` — Message status (read, unread, archived)
    
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

<details><summary><code>client.PrivateMessages.ListReplies(ID) -> *foru_ms_sdk.PrivateMessageReplyListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of replies for Private Message.
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
request := &foru_ms_sdk.ListRepliesPrivateMessagesRequest{
        ID: "id",
    }
client.PrivateMessages.ListReplies(
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

**limit:** `*int` — Items per page (max 75)
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PrivateMessages.CreateReply(ID, request) -> *foru_ms_sdk.PrivateMessageReplyResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a Reply in Private Message.
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
request := &foru_ms_sdk.CreateReplyPrivateMessagesRequest{
        ID: "id",
        RecipientID: "recipientId",
        Body: "body",
    }
client.PrivateMessages.CreateReply(
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

<details><summary><code>client.PrivateMessages.RetrieveReply(ID, SubID) -> *foru_ms_sdk.RetrieveReplyPrivateMessagesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.RetrieveReplyPrivateMessagesRequest{
        ID: "id",
        SubID: "subId",
    }
client.PrivateMessages.RetrieveReply(
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

<details><summary><code>client.PrivateMessages.DeleteReply(ID, SubID) -> *foru_ms_sdk.SuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteReplyPrivateMessagesRequest{
        ID: "id",
        SubID: "subId",
    }
client.PrivateMessages.DeleteReply(
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
<details><summary><code>client.Users.List() -> *foru_ms_sdk.UserListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of users. Use cursor for pagination.
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
request := &foru_ms_sdk.ListUsersRequest{}
client.Users.List(
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

**limit:** `*int` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Cursor for pagination
    
</dd>
</dl>

<dl>
<dd>

**search:** `*string` — Search by username or display name
    
</dd>
</dl>

<dl>
<dd>

**sort:** `*foru_ms_sdk.ListUsersRequestSort` — Sort by creation date
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Users.Create(request) -> *foru_ms_sdk.UserResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new user.
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
request := &foru_ms_sdk.CreateUsersRequest{
        Username: "username",
    }
client.Users.Create(
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

**username:** `string` — Username (letters, numbers, underscores, hyphens)
    
</dd>
</dl>

<dl>
<dd>

**email:** `*string` — Email address
    
</dd>
</dl>

<dl>
<dd>

**password:** `*string` — Password (min 8 chars)
    
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

**url:** `*string` — Website URL
    
</dd>
</dl>

<dl>
<dd>

**roles:** `[]string` — Role slugs to assign
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` — Custom extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Users.Retrieve(ID) -> *foru_ms_sdk.UserResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a user by ID or slug (if supported).
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
request := &foru_ms_sdk.RetrieveUsersRequest{
        ID: "id",
    }
client.Users.Retrieve(
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
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Users.Delete(ID) -> *foru_ms_sdk.SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete a user.
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
request := &foru_ms_sdk.DeleteUsersRequest{
        ID: "id",
    }
client.Users.Delete(
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
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Users.Update(ID, request) -> *foru_ms_sdk.UpdateUsersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing user. Only provided fields will be modified.
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
request := &foru_ms_sdk.UpdateUsersRequest{
        ID: "id",
    }
client.Users.Update(
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

<details><summary><code>client.Users.ListFollowers(ID) -> *foru_ms_sdk.UserFollowerListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of followers for User.
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
request := &foru_ms_sdk.ListFollowersUsersRequest{
        ID: "id",
    }
client.Users.ListFollowers(
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

**limit:** `*int` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Cursor for pagination
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Users.RetrieveFollower(ID, SubID) -> *foru_ms_sdk.RetrieveFollowerUsersResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.RetrieveFollowerUsersRequest{
        ID: "id",
        SubID: "subId",
    }
client.Users.RetrieveFollower(
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

<details><summary><code>client.Users.DeleteFollower(ID, SubID) -> *foru_ms_sdk.SuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteFollowerUsersRequest{
        ID: "id",
        SubID: "subId",
    }
client.Users.DeleteFollower(
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

<details><summary><code>client.Users.ListFollowing(ID) -> *foru_ms_sdk.UserFollowingListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of following for User.
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
request := &foru_ms_sdk.ListFollowingUsersRequest{
        ID: "id",
    }
client.Users.ListFollowing(
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

**limit:** `*int` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Cursor for pagination
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Users.RetrieveFollowing(ID, SubID) -> *foru_ms_sdk.RetrieveFollowingUsersResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.RetrieveFollowingUsersRequest{
        ID: "id",
        SubID: "subId",
    }
client.Users.RetrieveFollowing(
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

<details><summary><code>client.Users.DeleteFollowing(ID, SubID) -> *foru_ms_sdk.SuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteFollowingUsersRequest{
        ID: "id",
        SubID: "subId",
    }
client.Users.DeleteFollowing(
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
<details><summary><code>client.Roles.List() -> *foru_ms_sdk.RoleListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of roles. Use cursor for pagination.
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
request := &foru_ms_sdk.ListRolesRequest{}
client.Roles.List(
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

**limit:** `*int` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Cursor for pagination
    
</dd>
</dl>

<dl>
<dd>

**search:** `*string` — Search by name or slug
    
</dd>
</dl>

<dl>
<dd>

**sort:** `*foru_ms_sdk.ListRolesRequestSort` — Sort order
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Roles.Create(request) -> *foru_ms_sdk.RoleResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new role.
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
request := &foru_ms_sdk.CreateRolesRequest{
        Name: "name",
    }
client.Roles.Create(
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

<details><summary><code>client.Roles.Retrieve(ID) -> *foru_ms_sdk.RoleResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a role by ID or slug (if supported).
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
request := &foru_ms_sdk.RetrieveRolesRequest{
        ID: "id",
    }
client.Roles.Retrieve(
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

**id:** `string` — Role ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Roles.Delete(ID) -> *foru_ms_sdk.SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete a role.
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
request := &foru_ms_sdk.DeleteRolesRequest{
        ID: "id",
    }
client.Roles.Delete(
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

**id:** `string` — Role ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Roles.Update(ID, request) -> *foru_ms_sdk.UpdateRolesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing role. Only provided fields will be modified.
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
request := &foru_ms_sdk.UpdateRolesRequest{
        ID: "id",
    }
client.Roles.Update(
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

**id:** `string` — Role ID
    
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
<details><summary><code>client.Reports.List() -> *foru_ms_sdk.ReportListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of reports. Use cursor for pagination.
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
request := &foru_ms_sdk.ListReportsRequest{}
client.Reports.List(
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

**limit:** `*int` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Cursor for pagination
    
</dd>
</dl>

<dl>
<dd>

**status:** `*string` — Filter by status
    
</dd>
</dl>

<dl>
<dd>

**reporterID:** `*string` — Filter by reporter ID
    
</dd>
</dl>

<dl>
<dd>

**reportedID:** `*string` — Filter by reported user ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Reports.Create(request) -> *foru_ms_sdk.ReportResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new report.
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
request := &foru_ms_sdk.CreateReportsRequest{
        Type: "type",
    }
client.Reports.Create(
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

**status:** `*string` — Report status (default: pending)
    
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

<dl>
<dd>

**extendedData:** `map[string]any` — Custom extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Reports.Retrieve(ID) -> *foru_ms_sdk.ReportResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a report by ID or slug (if supported).
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
request := &foru_ms_sdk.RetrieveReportsRequest{
        ID: "id",
    }
client.Reports.Retrieve(
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

**id:** `string` — Report ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Reports.Delete(ID) -> *foru_ms_sdk.SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete a report.
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
request := &foru_ms_sdk.DeleteReportsRequest{
        ID: "id",
    }
client.Reports.Delete(
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

**id:** `string` — Report ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Reports.Update(ID, request) -> *foru_ms_sdk.UpdateReportsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing report. Only provided fields will be modified.
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
request := &foru_ms_sdk.UpdateReportsRequest{
        ID: "id",
    }
client.Reports.Update(
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

**id:** `string` — Report ID
    
</dd>
</dl>

<dl>
<dd>

**status:** `*string` — Report status (pending, reviewed, resolved, dismissed)
    
</dd>
</dl>

<dl>
<dd>

**description:** `*string` — Updated description or admin notes
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` — Custom extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Notifications
<details><summary><code>client.Notifications.List() -> *foru_ms_sdk.NotificationListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of notifications. Use cursor for pagination.
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
request := &foru_ms_sdk.ListNotificationsRequest{}
client.Notifications.List(
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

**limit:** `*int` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Cursor for pagination
    
</dd>
</dl>

<dl>
<dd>

**status:** `*foru_ms_sdk.ListNotificationsRequestStatus` — Filter by notification status
    
</dd>
</dl>

<dl>
<dd>

**userID:** `*string` — Filter by recipient user ID (admin only)
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Notifications.Create(request) -> *foru_ms_sdk.NotificationResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new notification.
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
request := &foru_ms_sdk.CreateNotificationsRequest{
        UserID: "userId",
        Type: "type",
    }
client.Notifications.Create(
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

**status:** `*foru_ms_sdk.CreateNotificationsRequestStatus` — Initial notification status
    
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

<details><summary><code>client.Notifications.Retrieve(ID) -> *foru_ms_sdk.NotificationResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a notification by ID or slug (if supported).
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
request := &foru_ms_sdk.RetrieveNotificationsRequest{
        ID: "id",
    }
client.Notifications.Retrieve(
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

**id:** `string` — Notification ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Notifications.Delete(ID) -> *foru_ms_sdk.SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete a notification.
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
request := &foru_ms_sdk.DeleteNotificationsRequest{
        ID: "id",
    }
client.Notifications.Delete(
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

**id:** `string` — Notification ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Notifications.Update(ID, request) -> *foru_ms_sdk.UpdateNotificationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing notification. Only provided fields will be modified.
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
request := &foru_ms_sdk.UpdateNotificationsRequest{
        ID: "id",
    }
client.Notifications.Update(
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

**id:** `string` — Notification ID
    
</dd>
</dl>

<dl>
<dd>

**status:** `*foru_ms_sdk.UpdateNotificationsRequestStatus` — Notification status
    
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
<details><summary><code>client.Webhooks.List() -> *foru_ms_sdk.WebhookListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of webhooks. Use cursor for pagination.

**Requires feature: webhooks**
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
request := &foru_ms_sdk.ListWebhooksRequest{}
client.Webhooks.List(
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

**limit:** `*int` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Cursor for pagination
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Webhooks.Create(request) -> *foru_ms_sdk.WebhookResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new webhook.

**Requires feature: webhooks**
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
request := &foru_ms_sdk.CreateWebhooksRequest{
        Name: "name",
        URL: "url",
        Events: []string{
            "events",
        },
    }
client.Webhooks.Create(
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

<dl>
<dd>

**active:** `*bool` — Whether webhook is active
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` — Custom extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Webhooks.Retrieve(ID) -> *foru_ms_sdk.WebhookResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a webhook by ID or slug (if supported).

**Requires feature: webhooks**
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
request := &foru_ms_sdk.RetrieveWebhooksRequest{
        ID: "id",
    }
client.Webhooks.Retrieve(
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
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Webhooks.Delete(ID) -> *foru_ms_sdk.SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete a webhook.

**Requires feature: webhooks**
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
request := &foru_ms_sdk.DeleteWebhooksRequest{
        ID: "id",
    }
client.Webhooks.Delete(
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
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Webhooks.Update(ID, request) -> *foru_ms_sdk.UpdateWebhooksResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing webhook. Only provided fields will be modified.

**Requires feature: webhooks**
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
request := &foru_ms_sdk.UpdateWebhooksRequest{
        ID: "id",
    }
client.Webhooks.Update(
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

**name:** `*string` — Webhook name
    
</dd>
</dl>

<dl>
<dd>

**url:** `*string` — Target URL
    
</dd>
</dl>

<dl>
<dd>

**events:** `[]string` — Event types to trigger on
    
</dd>
</dl>

<dl>
<dd>

**secret:** `*string` — New secret
    
</dd>
</dl>

<dl>
<dd>

**active:** `*bool` — Enable/disable webhook
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` — Custom extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Webhooks.ListDeliveries(ID) -> *foru_ms_sdk.WebhookDeliveryListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of deliveries for Webhook.

**Requires feature: webhooks**
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
request := &foru_ms_sdk.ListDeliveriesWebhooksRequest{
        ID: "id",
    }
client.Webhooks.ListDeliveries(
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

**limit:** `*int` — Items per page (max 75)
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Webhooks.RetrieveDelivery(ID, SubID) -> *foru_ms_sdk.RetrieveDeliveryWebhooksResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.RetrieveDeliveryWebhooksRequest{
        ID: "id",
        SubID: "subId",
    }
client.Webhooks.RetrieveDelivery(
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

<details><summary><code>client.Webhooks.DeleteDelivery(ID, SubID) -> *foru_ms_sdk.SuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &foru_ms_sdk.DeleteDeliveryWebhooksRequest{
        ID: "id",
        SubID: "subId",
    }
client.Webhooks.DeleteDelivery(
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
<details><summary><code>client.Integrations.List() -> *foru_ms_sdk.IntegrationListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of integrations. Use cursor for pagination.

**Requires feature: integrations**
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
request := &foru_ms_sdk.ListIntegrationsRequest{}
client.Integrations.List(
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

**limit:** `*int` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Cursor for pagination
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Integrations.Create(request) -> *foru_ms_sdk.IntegrationResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create an new integration.

**Requires feature: integrations**
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
request := &foru_ms_sdk.CreateIntegrationsRequest{
        Type: "type",
        Name: "name",
        Config: map[string]any{
            "key": "value",
        },
    }
client.Integrations.Create(
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

**type_:** `string` — Integration type (e.g. SLACK, DISCORD)
    
</dd>
</dl>

<dl>
<dd>

**name:** `string` — Integration name
    
</dd>
</dl>

<dl>
<dd>

**config:** `map[string]any` — JSON configuration
    
</dd>
</dl>

<dl>
<dd>

**active:** `*bool` — Whether integration is active
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` — Custom extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Integrations.Retrieve(ID) -> *foru_ms_sdk.IntegrationResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve an integration by ID or slug (if supported).

**Requires feature: integrations**
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
request := &foru_ms_sdk.RetrieveIntegrationsRequest{
        ID: "id",
    }
client.Integrations.Retrieve(
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

**id:** `string` — Integration ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Integrations.Delete(ID) -> *foru_ms_sdk.SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete an integration.

**Requires feature: integrations**
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
request := &foru_ms_sdk.DeleteIntegrationsRequest{
        ID: "id",
    }
client.Integrations.Delete(
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

**id:** `string` — Integration ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Integrations.Update(ID, request) -> *foru_ms_sdk.UpdateIntegrationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing integration. Only provided fields will be modified.

**Requires feature: integrations**
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
request := &foru_ms_sdk.UpdateIntegrationsRequest{
        ID: "id",
    }
client.Integrations.Update(
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

**id:** `string` — Integration ID
    
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

<dl>
<dd>

**extendedData:** `map[string]any` — Custom extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## SSOs
<details><summary><code>client.SsOs.List() -> *foru_ms_sdk.SSOListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of ssos. Use cursor for pagination.

**Requires feature: sso**
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
request := &foru_ms_sdk.ListSsOsRequest{}
client.SsOs.List(
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

**limit:** `*int` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `*string` — Cursor for pagination
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.SsOs.Create(request) -> *foru_ms_sdk.SSOResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create an new sso.

**Requires feature: sso**
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
request := &foru_ms_sdk.CreateSsOsRequest{
        Provider: foru_ms_sdk.CreateSsOsRequestProviderOkta,
        Domain: "domain",
        Config: map[string]any{
            "key": "value",
        },
    }
client.SsOs.Create(
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

**provider:** `*foru_ms_sdk.CreateSsOsRequestProvider` — SSO provider type
    
</dd>
</dl>

<dl>
<dd>

**domain:** `string` — Email domain to match (e.g. 'acme.com')
    
</dd>
</dl>

<dl>
<dd>

**config:** `map[string]any` — Provider configuration (clientId, issuer, etc.)
    
</dd>
</dl>

<dl>
<dd>

**active:** `*bool` — Whether SSO is active
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` — Custom extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.SsOs.Retrieve(ID) -> *foru_ms_sdk.SSOResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve an sso by ID or slug (if supported).

**Requires feature: sso**
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
request := &foru_ms_sdk.RetrieveSsOsRequest{
        ID: "id",
    }
client.SsOs.Retrieve(
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

**id:** `string` — SSO ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.SsOs.Delete(ID) -> *foru_ms_sdk.SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete an sso.

**Requires feature: sso**
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
request := &foru_ms_sdk.DeleteSsOsRequest{
        ID: "id",
    }
client.SsOs.Delete(
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

**id:** `string` — SSO ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.SsOs.Update(ID, request) -> *foru_ms_sdk.UpdateSsOsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing sso. Only provided fields will be modified.

**Requires feature: sso**
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
request := &foru_ms_sdk.UpdateSsOsRequest{
        ID: "id",
    }
client.SsOs.Update(
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

**id:** `string` — SSO ID
    
</dd>
</dl>

<dl>
<dd>

**provider:** `*foru_ms_sdk.UpdateSsOsRequestProvider` — SSO provider type
    
</dd>
</dl>

<dl>
<dd>

**domain:** `*string` — Email domain to match
    
</dd>
</dl>

<dl>
<dd>

**config:** `map[string]any` — Provider configuration
    
</dd>
</dl>

<dl>
<dd>

**active:** `*bool` — Enable/disable provider
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `map[string]any` — Custom extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Provisioning
<details><summary><code>client.Provisioning.List() -> *foru_ms_sdk.ListProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve all instances owned by the authenticated user. Use the `handle` query parameter to get a single instance with its API key.
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
request := &foru_ms_sdk.ListProvisioningRequest{
        ProvisioningKey: "x-provisioning-key",
    }
client.Provisioning.List(
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

**handle:** `*string` — Optional handle to get a single instance
    
</dd>
</dl>

<dl>
<dd>

**provisioningKey:** `string` — User provisioning key for platform-level instance management
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Provisioning.Create(request) -> *foru_ms_sdk.CreateProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new forum instance. Returns the instance details including the API key for accessing the forum API.
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
request := &foru_ms_sdk.CreateInstance{
        ProvisioningKey: "x-provisioning-key",
        Name: "name",
        Handle: "handle",
    }
client.Provisioning.Create(
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

**provisioningKey:** `string` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**name:** `string` — Display name for the instance
    
</dd>
</dl>

<dl>
<dd>

**handle:** `string` — URL-friendly identifier (slug)
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Provisioning.Update(request) -> *foru_ms_sdk.UpdateProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an instance's name or handle. The `handle` field identifies which instance to update.
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
request := &foru_ms_sdk.UpdateInstance{
        ProvisioningKey: "x-provisioning-key",
        Handle: "handle",
    }
client.Provisioning.Update(
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

**provisioningKey:** `string` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `string` — Current handle to identify the instance
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — New display name
    
</dd>
</dl>

<dl>
<dd>

**newHandle:** `*string` — New URL-friendly identifier
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Provisioning.Delete(request) -> *foru_ms_sdk.DeleteProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete an instance. This action cannot be undone.
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
request := &foru_ms_sdk.DeleteInstance{
        ProvisioningKey: "x-provisioning-key",
        Handle: "handle",
    }
client.Provisioning.Delete(
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

**provisioningKey:** `string` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `string` — Handle of the instance to delete
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Provisioning.GetBilling() -> *foru_ms_sdk.GetBillingProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve billing and subscription information for an instance.
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
request := &foru_ms_sdk.GetBillingProvisioningRequest{
        Handle: "handle",
        ProvisioningKey: "x-provisioning-key",
    }
client.Provisioning.GetBilling(
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

**handle:** `string` — Instance handle
    
</dd>
</dl>

<dl>
<dd>

**provisioningKey:** `string` — User provisioning key for platform-level instance management
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Provisioning.ChangePlan(request) -> *foru_ms_sdk.ChangePlanProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Change an instance's subscription plan. Returns a checkout URL for upgrades or a billing portal URL for downgrades.
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
request := &foru_ms_sdk.UpgradeInstance{
        ProvisioningKey: "x-provisioning-key",
        Handle: "handle",
        Plan: foru_ms_sdk.UpgradeInstancePlanFree,
    }
client.Provisioning.ChangePlan(
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

**provisioningKey:** `string` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `string` — Instance handle
    
</dd>
</dl>

<dl>
<dd>

**plan:** `*foru_ms_sdk.UpgradeInstancePlan` — Target plan
    
</dd>
</dl>

<dl>
<dd>

**isAnnual:** `*bool` — Use annual billing (default: true)
    
</dd>
</dl>

<dl>
<dd>

**returnURL:** `*string` — URL to return to after checkout/portal
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Provisioning.RegenerateAPIKey(request) -> *foru_ms_sdk.RegenerateAPIKeyProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Generate a new API key for the instance. The old key will be invalidated.
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
request := &foru_ms_sdk.RegenerateAPIKeyProvisioningRequest{
        ProvisioningKey: "x-provisioning-key",
        Handle: "handle",
    }
client.Provisioning.RegenerateAPIKey(
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

**provisioningKey:** `string` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Provisioning.GetUsage() -> *foru_ms_sdk.GetUsageProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve usage statistics for an instance including API requests, storage, and content counts.
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
request := &foru_ms_sdk.GetUsageProvisioningRequest{
        Handle: "handle",
        ProvisioningKey: "x-provisioning-key",
    }
client.Provisioning.GetUsage(
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

**handle:** `string` — Instance handle
    
</dd>
</dl>

<dl>
<dd>

**provisioningKey:** `string` — User provisioning key for platform-level instance management
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Provisioning.ListTeam() -> *foru_ms_sdk.ListTeamProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve all team members for an instance.
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
request := &foru_ms_sdk.ListTeamProvisioningRequest{
        Handle: "handle",
        ProvisioningKey: "x-provisioning-key",
    }
client.Provisioning.ListTeam(
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

**handle:** `string` — Instance handle
    
</dd>
</dl>

<dl>
<dd>

**provisioningKey:** `string` — User provisioning key for platform-level instance management
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Provisioning.InviteTeam(request) -> *foru_ms_sdk.InviteTeamProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Invite new team members to an instance.
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
request := &foru_ms_sdk.InviteTeamProvisioningRequest{
        ProvisioningKey: "x-provisioning-key",
        Handle: "handle",
        Members: []*foru_ms_sdk.InviteTeamProvisioningRequestMembersItem{
            &foru_ms_sdk.InviteTeamProvisioningRequestMembersItem{
                Email: "email",
            },
        },
    }
client.Provisioning.InviteTeam(
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

**provisioningKey:** `string` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**members:** `[]*foru_ms_sdk.InviteTeamProvisioningRequestMembersItem` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Provisioning.RemoveTeamMember(request) -> *foru_ms_sdk.RemoveTeamMemberProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Remove a team member from an instance.
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
request := &foru_ms_sdk.RemoveTeamMemberProvisioningRequest{
        ProvisioningKey: "x-provisioning-key",
        Handle: "handle",
        Email: "email",
    }
client.Provisioning.RemoveTeamMember(
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

**provisioningKey:** `string` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**email:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Provisioning.ListDomains() -> *foru_ms_sdk.ListDomainsProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve all custom domains for an instance.
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
request := &foru_ms_sdk.ListDomainsProvisioningRequest{
        Handle: "handle",
        ProvisioningKey: "x-provisioning-key",
    }
client.Provisioning.ListDomains(
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

**handle:** `string` — Instance handle
    
</dd>
</dl>

<dl>
<dd>

**provisioningKey:** `string` — User provisioning key for platform-level instance management
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Provisioning.AddDomain(request) -> *foru_ms_sdk.AddDomainProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a custom domain to an instance.
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
request := &foru_ms_sdk.AddDomainProvisioningRequest{
        ProvisioningKey: "x-provisioning-key",
        Handle: "handle",
        Name: "name",
    }
client.Provisioning.AddDomain(
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

**provisioningKey:** `string` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**name:** `string` — Domain name (e.g., forum.example.com)
    
</dd>
</dl>

<dl>
<dd>

**subdomain:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Provisioning.RemoveDomain(request) -> *foru_ms_sdk.RemoveDomainProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Remove a custom domain from an instance.
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
request := &foru_ms_sdk.RemoveDomainProvisioningRequest{
        ProvisioningKey: "x-provisioning-key",
        Handle: "handle",
        Name: "name",
    }
client.Provisioning.RemoveDomain(
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

**provisioningKey:** `string` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**name:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Provisioning.ExportData(request) -> *foru_ms_sdk.ExportDataProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from an instance including threads, posts, users, tags, etc.
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
request := &foru_ms_sdk.ExportDataProvisioningRequest{
        ProvisioningKey: "x-provisioning-key",
        Handle: "handle",
    }
client.Provisioning.ExportData(
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

**provisioningKey:** `string` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Provisioning.ListWebhooks() -> *foru_ms_sdk.ListWebhooksProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve all webhooks configured for an instance.
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
request := &foru_ms_sdk.ListWebhooksProvisioningRequest{
        Handle: "handle",
        ProvisioningKey: "x-provisioning-key",
    }
client.Provisioning.ListWebhooks(
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

**handle:** `string` — Instance handle
    
</dd>
</dl>

<dl>
<dd>

**provisioningKey:** `string` — User provisioning key for platform-level instance management
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Provisioning.CreateWebhook(request) -> *foru_ms_sdk.CreateWebhookProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new webhook for an instance.
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
request := &foru_ms_sdk.CreateWebhookProvisioningRequest{
        ProvisioningKey: "x-provisioning-key",
        Handle: "handle",
        URL: "url",
        Events: []string{
            "events",
        },
    }
client.Provisioning.CreateWebhook(
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

**provisioningKey:** `string` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**url:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**events:** `[]string` 
    
</dd>
</dl>

<dl>
<dd>

**secret:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**active:** `*bool` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Provisioning.UpdateWebhook(request) -> *foru_ms_sdk.UpdateWebhookProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing webhook.
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
request := &foru_ms_sdk.UpdateWebhookProvisioningRequest{
        ProvisioningKey: "x-provisioning-key",
        Handle: "handle",
        WebhookID: "webhookId",
    }
client.Provisioning.UpdateWebhook(
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

**provisioningKey:** `string` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**webhookID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**url:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**events:** `[]string` 
    
</dd>
</dl>

<dl>
<dd>

**secret:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**active:** `*bool` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Provisioning.DeleteWebhook(request) -> *foru_ms_sdk.DeleteWebhookProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a webhook from an instance.
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
request := &foru_ms_sdk.DeleteWebhookProvisioningRequest{
        ProvisioningKey: "x-provisioning-key",
        Handle: "handle",
        WebhookID: "webhookId",
    }
client.Provisioning.DeleteWebhook(
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

**provisioningKey:** `string` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**webhookID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Provisioning.GetOwnership() -> *foru_ms_sdk.GetOwnershipProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve owner and creator information for an instance.
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
request := &foru_ms_sdk.GetOwnershipProvisioningRequest{
        Handle: "handle",
        ProvisioningKey: "x-provisioning-key",
    }
client.Provisioning.GetOwnership(
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

**handle:** `string` — Instance handle
    
</dd>
</dl>

<dl>
<dd>

**provisioningKey:** `string` — User provisioning key for platform-level instance management
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Provisioning.TransferOwnership(request) -> *foru_ms_sdk.TransferOwnershipProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Transfer instance ownership to another user. Only the current owner can transfer ownership.
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
request := &foru_ms_sdk.TransferOwnershipProvisioningRequest{
        ProvisioningKey: "x-provisioning-key",
        Handle: "handle",
        NewOwnerEmail: "newOwnerEmail",
    }
client.Provisioning.TransferOwnership(
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

**provisioningKey:** `string` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**newOwnerEmail:** `string` — Email of the new owner
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Provisioning.Register(request) -> *foru_ms_sdk.RegisterProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new account and receive a provisioning key for API access. Use this key to create and manage instances.
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
request := &foru_ms_sdk.RegisterProvisioningRequest{
        Email: "email",
        Password: "password",
    }
client.Provisioning.Register(
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

**email:** `string` — Email address for the account
    
</dd>
</dl>

<dl>
<dd>

**password:** `string` — Password (minimum 8 characters)
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — Display name (optional)
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Provisioning.Login(request) -> *foru_ms_sdk.LoginProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Login with email and password to retrieve your provisioning key.
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
request := &foru_ms_sdk.LoginProvisioningRequest{
        Email: "email",
        Password: "password",
    }
client.Provisioning.Login(
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

**email:** `string` — Account email
    
</dd>
</dl>

<dl>
<dd>

**password:** `string` — Account password
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>
