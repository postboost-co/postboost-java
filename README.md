# PostBoost Java SDK

Official Java client for the [PostBoost API](https://postboost.co/docs/api).

## Install

**Maven:**

```xml
<repositories>
  <repository>
    <id>github</id>
    <url>https://maven.pkg.github.com/postboost-co/postboost-java</url>
  </repository>
</repositories>

<dependency>
  <groupId>com.postboost</groupId>
  <artifactId>postboost-java-sdk</artifactId>
  <version>1.5.0</version>
</dependency>
```

**Gradle:**

```groovy
repositories {
    maven { url 'https://maven.pkg.github.com/postboost-co/postboost-java' }
}
dependencies {
    implementation 'com.postboost:postboost-java-sdk:1.5.0'
}
```

| | |
|---|---|
| **GitHub Packages** | [github.com/postboost-co/postboost-java/packages](https://github.com/postboost-co/postboost-java/packages) |
| **GitHub** | [postboost-co/postboost-java](https://github.com/postboost-co/postboost-java) |
| **Docs** | [postboost.co/docs/api](https://postboost.co/docs/api) |
| **Version** | v1.5.0 |

## Quick start

```java
ApiClient client = new ApiClient();
client.setBearerToken(apiToken);

PostsApi api = new PostsApi(client);
List<Post> posts = api.listPosts("YOUR_WORKSPACE_UUID");
posts.forEach(p -> System.out.println(p.getUuid()));
```

---

## Documentation for API Endpoints

All URIs are relative to *https://postboost.co/app/api*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AccountsApi* | [**getAccount**](docs/AccountsApi.md#getAccount) | **GET** /{workspaceUuid}/accounts/{accountUuid} | Get account
*AccountsApi* | [**listAccounts**](docs/AccountsApi.md#listAccounts) | **GET** /{workspaceUuid}/accounts | List accounts
*AiApi* | [**blogToSocial**](docs/AiApi.md#blogToSocial) | **POST** /{workspaceUuid}/ai/blog-to-social | Generate social media captions from a blog post
*AiApi* | [**imageAltText**](docs/AiApi.md#imageAltText) | **POST** /{workspaceUuid}/ai/image-alt-text | Generate alt text for a media image using AI
*AiApi* | [**imageEdit**](docs/AiApi.md#imageEdit) | **POST** /{workspaceUuid}/ai/image-edit | Edit an existing media image using AI
*AiApi* | [**imageGenerate**](docs/AiApi.md#imageGenerate) | **POST** /{workspaceUuid}/ai/image-generate | Generate social media images from a caption
*AiApi* | [**imagePrompt**](docs/AiApi.md#imagePrompt) | **POST** /{workspaceUuid}/ai/image-prompt | Build an optimized image prompt from a social media caption
*AiApi* | [**imageVariations**](docs/AiApi.md#imageVariations) | **POST** /{workspaceUuid}/ai/image-variations | Generate variations of an existing media image
*MediaApi* | [**abortChunkedUpload**](docs/MediaApi.md#abortChunkedUpload) | **DELETE** /{workspaceUuid}/media/chunked/{uploadUuid} | Abort chunked upload
*MediaApi* | [**completeChunkedUpload**](docs/MediaApi.md#completeChunkedUpload) | **POST** /{workspaceUuid}/media/chunked/{uploadUuid}/complete | Complete chunked upload
*MediaApi* | [**deleteMediaBulk**](docs/MediaApi.md#deleteMediaBulk) | **DELETE** /{workspaceUuid}/media | Delete media (bulk)
*MediaApi* | [**getMedia**](docs/MediaApi.md#getMedia) | **GET** /{workspaceUuid}/media/{mediaUuid} | Get media
*MediaApi* | [**getRemoteUploadStatus**](docs/MediaApi.md#getRemoteUploadStatus) | **GET** /{workspaceUuid}/media/remote/{downloadId}/status | Get remote upload status
*MediaApi* | [**initiateChunkedUpload**](docs/MediaApi.md#initiateChunkedUpload) | **POST** /{workspaceUuid}/media/chunked/initiate | Initiate chunked upload
*MediaApi* | [**initiateRemoteUpload**](docs/MediaApi.md#initiateRemoteUpload) | **POST** /{workspaceUuid}/media/remote/initiate | Initiate remote upload
*MediaApi* | [**listMedia**](docs/MediaApi.md#listMedia) | **GET** /{workspaceUuid}/media | List media
*MediaApi* | [**updateMedia**](docs/MediaApi.md#updateMedia) | **PUT** /{workspaceUuid}/media/{mediaUuid} | Update media
*MediaApi* | [**uploadChunk**](docs/MediaApi.md#uploadChunk) | **POST** /{workspaceUuid}/media/chunked/{uploadUuid}/upload | Upload a chunk
*MediaApi* | [**uploadMedia**](docs/MediaApi.md#uploadMedia) | **POST** /{workspaceUuid}/media | Upload media (binary)
*PostsApi* | [**addPostToQueue**](docs/PostsApi.md#addPostToQueue) | **POST** /{workspaceUuid}/posts/add-to-queue/{postUuid} | Add post to queue
*PostsApi* | [**approvePost**](docs/PostsApi.md#approvePost) | **POST** /{workspaceUuid}/posts/approve/{postUuid} | Approve post
*PostsApi* | [**createPost**](docs/PostsApi.md#createPost) | **POST** /{workspaceUuid}/posts | Create post
*PostsApi* | [**deletePost**](docs/PostsApi.md#deletePost) | **DELETE** /{workspaceUuid}/posts/{postUuid} | Delete post
*PostsApi* | [**deletePostsBulk**](docs/PostsApi.md#deletePostsBulk) | **DELETE** /{workspaceUuid}/posts | Delete posts (bulk)
*PostsApi* | [**getPost**](docs/PostsApi.md#getPost) | **GET** /{workspaceUuid}/posts/{postUuid} | Get post
*PostsApi* | [**listPosts**](docs/PostsApi.md#listPosts) | **GET** /{workspaceUuid}/posts | List posts
*PostsApi* | [**schedulePost**](docs/PostsApi.md#schedulePost) | **POST** /{workspaceUuid}/posts/schedule/{postUuid} | Schedule post
*PostsApi* | [**updatePost**](docs/PostsApi.md#updatePost) | **PUT** /{workspaceUuid}/posts/{postUuid} | Update post
*ReceiptsApi* | [**createReceipt**](docs/ReceiptsApi.md#createReceipt) | **POST** /panel/receipts | Create receipt
*ReceiptsApi* | [**deleteReceipt**](docs/ReceiptsApi.md#deleteReceipt) | **DELETE** /panel/receipts/{receiptUuid} | Delete receipt
*ReceiptsApi* | [**deleteReceiptsBulk**](docs/ReceiptsApi.md#deleteReceiptsBulk) | **DELETE** /panel/receipts | Delete receipts (bulk)
*ReceiptsApi* | [**getReceipt**](docs/ReceiptsApi.md#getReceipt) | **GET** /panel/receipts/{receiptUuid} | Get receipt
*ReceiptsApi* | [**listReceipts**](docs/ReceiptsApi.md#listReceipts) | **GET** /panel/receipts | List receipts
*ReceiptsApi* | [**updateReceipt**](docs/ReceiptsApi.md#updateReceipt) | **PUT** /panel/receipts/{receiptUuid} | Update receipt
*SubscriptionsApi* | [**addGenericSubscription**](docs/SubscriptionsApi.md#addGenericSubscription) | **POST** /panel/workspaces/{workspaceUuid}/subscription/generic | Add generic subscription
*SubscriptionsApi* | [**cancelSubscription**](docs/SubscriptionsApi.md#cancelSubscription) | **POST** /panel/workspaces/{workspaceUuid}/subscription/cancel | Cancel subscription
*SubscriptionsApi* | [**changeSubscriptionPlan**](docs/SubscriptionsApi.md#changeSubscriptionPlan) | **PUT** /panel/workspaces/{workspaceUuid}/subscription/change-plan | Change subscription plan
*SubscriptionsApi* | [**checkoutSubscription**](docs/SubscriptionsApi.md#checkoutSubscription) | **POST** /panel/workspaces/{workspaceUuid}/subscription/new | New subscription checkout
*SubscriptionsApi* | [**createSubscription**](docs/SubscriptionsApi.md#createSubscription) | **POST** /panel/workspaces/{workspaceUuid}/subscription | Create subscription
*SubscriptionsApi* | [**deleteSubscription**](docs/SubscriptionsApi.md#deleteSubscription) | **DELETE** /panel/workspaces/{workspaceUuid}/subscription | Delete subscription
*SubscriptionsApi* | [**getSubscription**](docs/SubscriptionsApi.md#getSubscription) | **GET** /panel/workspaces/{workspaceUuid}/subscription | Get subscription
*SubscriptionsApi* | [**removeGenericSubscription**](docs/SubscriptionsApi.md#removeGenericSubscription) | **DELETE** /panel/workspaces/{workspaceUuid}/subscription/generic | Remove generic subscription
*SubscriptionsApi* | [**resumeSubscription**](docs/SubscriptionsApi.md#resumeSubscription) | **POST** /panel/workspaces/{workspaceUuid}/subscription/resume | Resume subscription
*SubscriptionsApi* | [**updateSubscription**](docs/SubscriptionsApi.md#updateSubscription) | **PUT** /panel/workspaces/{workspaceUuid}/subscription | Update subscription
*TagsApi* | [**createTag**](docs/TagsApi.md#createTag) | **POST** /{workspaceUuid}/tags | Create tag
*TagsApi* | [**deleteTag**](docs/TagsApi.md#deleteTag) | **DELETE** /{workspaceUuid}/tags/{tagUuid} | Delete tag
*TagsApi* | [**getTag**](docs/TagsApi.md#getTag) | **GET** /{workspaceUuid}/tags/{tagUuid} | Get tag
*TagsApi* | [**listTags**](docs/TagsApi.md#listTags) | **GET** /{workspaceUuid}/tags | List tags
*TagsApi* | [**updateTag**](docs/TagsApi.md#updateTag) | **PUT** /{workspaceUuid}/tags/{tagUuid} | Update tag
*UsersApi* | [**createUser**](docs/UsersApi.md#createUser) | **POST** /panel/users | Create user
*UsersApi* | [**deleteUser**](docs/UsersApi.md#deleteUser) | **DELETE** /panel/users/{userId} | Delete user
*UsersApi* | [**deleteUsersBulk**](docs/UsersApi.md#deleteUsersBulk) | **DELETE** /panel/users | Delete users (bulk)
*UsersApi* | [**getUser**](docs/UsersApi.md#getUser) | **GET** /panel/users/{userId} | Get user
*UsersApi* | [**listUsers**](docs/UsersApi.md#listUsers) | **GET** /panel/users | List users
*UsersApi* | [**updateUser**](docs/UsersApi.md#updateUser) | **PUT** /panel/users/{userId} | Update user
*WorkspacesApi* | [**addUserToWorkspace**](docs/WorkspacesApi.md#addUserToWorkspace) | **POST** /panel/workspaces/{workspaceUuid}/users | Add user to workspace
*WorkspacesApi* | [**createWorkspace**](docs/WorkspacesApi.md#createWorkspace) | **POST** /panel/workspaces | Create workspace
*WorkspacesApi* | [**deleteWorkspace**](docs/WorkspacesApi.md#deleteWorkspace) | **DELETE** /panel/workspaces/{workspaceUuid} | Delete workspace
*WorkspacesApi* | [**deleteWorkspacesBulk**](docs/WorkspacesApi.md#deleteWorkspacesBulk) | **DELETE** /panel/workspaces | Delete workspaces (bulk)
*WorkspacesApi* | [**getWorkspace**](docs/WorkspacesApi.md#getWorkspace) | **GET** /panel/workspaces/{workspaceUuid} | Get workspace
*WorkspacesApi* | [**listWorkspaces**](docs/WorkspacesApi.md#listWorkspaces) | **GET** /panel/workspaces | List workspaces
*WorkspacesApi* | [**removeUserFromWorkspace**](docs/WorkspacesApi.md#removeUserFromWorkspace) | **DELETE** /panel/workspaces/{workspaceUuid}/users | Remove user from workspace
*WorkspacesApi* | [**updateWorkspace**](docs/WorkspacesApi.md#updateWorkspace) | **PUT** /panel/workspaces/{workspaceUuid} | Update workspace
*WorkspacesApi* | [**updateWorkspaceUser**](docs/WorkspacesApi.md#updateWorkspaceUser) | **PUT** /panel/workspaces/{workspaceUuid}/users | Update user role in workspace
