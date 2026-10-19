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
  <version>1.57.1</version>
</dependency>
```

**Gradle:**

```groovy
repositories {
    maven { url 'https://maven.pkg.github.com/postboost-co/postboost-java' }
}
dependencies {
    implementation 'com.postboost:postboost-java-sdk:1.57.1'
}
```

| | |
|---|---|
| **GitHub Packages** | [github.com/postboost-co/postboost-java/packages](https://github.com/postboost-co/postboost-java/packages) |
| **GitHub** | [postboost-co/postboost-java](https://github.com/postboost-co/postboost-java) |
| **Docs** | [postboost.co/docs/api](https://postboost.co/docs/api) |
| **Version** | v1.57.1 |

## Quick start

```java
import com.postboost.ApiClient;
import com.postboost.api.PostsApi;
import com.postboost.model.ListPosts200Response;
import java.util.UUID;

ApiClient client = new ApiClient();
client.setBearerToken(apiToken);

PostsApi api = new PostsApi(client);
ListPosts200Response resp = api.listPosts(UUID.fromString("YOUR_WORKSPACE_UUID"), null);
resp.getData().forEach(p -> System.out.println(p.getUuid()));
```

---

## Documentation for API Endpoints

All URIs are relative to *https://postboost.co/app/api*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AccountGroupsApi* | [**createAccountGroup**](docs/AccountGroupsApi.md#createAccountGroup) | **POST** /{workspaceUuid}/account-groups | Create an account group
*AccountGroupsApi* | [**deleteAccountGroup**](docs/AccountGroupsApi.md#deleteAccountGroup) | **DELETE** /{workspaceUuid}/account-groups/{accountGroupUuid} | Delete an account group
*AccountGroupsApi* | [**getAccountGroup**](docs/AccountGroupsApi.md#getAccountGroup) | **GET** /{workspaceUuid}/account-groups/{accountGroupUuid} | Get an account group
*AccountGroupsApi* | [**listAccountGroups**](docs/AccountGroupsApi.md#listAccountGroups) | **GET** /{workspaceUuid}/account-groups | List account groups
*AccountGroupsApi* | [**updateAccountGroup**](docs/AccountGroupsApi.md#updateAccountGroup) | **PUT** /{workspaceUuid}/account-groups/{accountGroupUuid} | Update an account group
*AccountsApi* | [**connectChannel**](docs/AccountsApi.md#connectChannel) | **POST** /{workspaceUuid}/accounts/connect/{provider} | Connect a Telegram, Discord or Slack channel
*AccountsApi* | [**createConnectLink**](docs/AccountsApi.md#createConnectLink) | **POST** /{workspaceUuid}/accounts/connect-links | Create a connect link
*AccountsApi* | [**createReconnectLink**](docs/AccountsApi.md#createReconnectLink) | **POST** /{workspaceUuid}/accounts/{accountUuid}/reconnect-links | Create a reconnect link
*AccountsApi* | [**getAccount**](docs/AccountsApi.md#getAccount) | **GET** /{workspaceUuid}/accounts/{accountUuid} | Get account
*AccountsApi* | [**getAccountHealth**](docs/AccountsApi.md#getAccountHealth) | **GET** /{workspaceUuid}/account-health | Account health
*AccountsApi* | [**listAccounts**](docs/AccountsApi.md#listAccounts) | **GET** /{workspaceUuid}/accounts | List accounts
*ActivityApi* | [**listApiActivity**](docs/ActivityApi.md#listApiActivity) | **GET** /{workspaceUuid}/activity | List API activity
*AgentsApi* | [**approveAgentProposal**](docs/AgentsApi.md#approveAgentProposal) | **POST** /{workspaceUuid}/agent-proposals/{proposalUuid}/approve | Approve and apply an agent proposal
*AgentsApi* | [**createAgent**](docs/AgentsApi.md#createAgent) | **POST** /{workspaceUuid}/agents | Switch on a background agent
*AgentsApi* | [**deleteAgent**](docs/AgentsApi.md#deleteAgent) | **DELETE** /{workspaceUuid}/agents/{agentUuid} | Delete a background agent
*AgentsApi* | [**getAgentRun**](docs/AgentsApi.md#getAgentRun) | **GET** /{workspaceUuid}/agent-runs/{runUuid} | Get an agent run with its proposals
*AgentsApi* | [**listAgentProposals**](docs/AgentsApi.md#listAgentProposals) | **GET** /{workspaceUuid}/agent-proposals | List agent proposals (approval queue)
*AgentsApi* | [**listAgentRuns**](docs/AgentsApi.md#listAgentRuns) | **GET** /{workspaceUuid}/agents/{agentUuid}/runs | Run history of an agent
*AgentsApi* | [**listAgents**](docs/AgentsApi.md#listAgents) | **GET** /{workspaceUuid}/agents | List background agents
*AgentsApi* | [**rejectAgentProposal**](docs/AgentsApi.md#rejectAgentProposal) | **POST** /{workspaceUuid}/agent-proposals/{proposalUuid}/reject | Reject an agent proposal
*AgentsApi* | [**runAgent**](docs/AgentsApi.md#runAgent) | **POST** /{workspaceUuid}/agents/{agentUuid}/run | Run a background agent now
*AgentsApi* | [**updateAgent**](docs/AgentsApi.md#updateAgent) | **PUT** /{workspaceUuid}/agents/{agentUuid} | Update a background agent
*AiApi* | [**blogToSocial**](docs/AiApi.md#blogToSocial) | **POST** /{workspaceUuid}/ai/blog-to-social | Generate social media captions from a blog post
*AiApi* | [**deleteBrandVoice**](docs/AiApi.md#deleteBrandVoice) | **DELETE** /{workspaceUuid}/brand-voice | Delete the brand voice
*AiApi* | [**getAIUsage**](docs/AiApi.md#getAIUsage) | **GET** /{workspaceUuid}/usage/ai | AI credit usage
*AiApi* | [**getBrandVoice**](docs/AiApi.md#getBrandVoice) | **GET** /{workspaceUuid}/brand-voice | Get the brand voice
*AiApi* | [**getRepurposeRun**](docs/AiApi.md#getRepurposeRun) | **GET** /{workspaceUuid}/ai/repurpose/runs/{runId} | Get a repurpose run
*AiApi* | [**imageAltText**](docs/AiApi.md#imageAltText) | **POST** /{workspaceUuid}/ai/image-alt-text | Generate alt text for a media image using AI
*AiApi* | [**imageEdit**](docs/AiApi.md#imageEdit) | **POST** /{workspaceUuid}/ai/image-edit | Edit an existing media image using AI
*AiApi* | [**imageGenerate**](docs/AiApi.md#imageGenerate) | **POST** /{workspaceUuid}/ai/image-generate | Generate social media images from a caption
*AiApi* | [**imagePrompt**](docs/AiApi.md#imagePrompt) | **POST** /{workspaceUuid}/ai/image-prompt | Build an optimized image prompt from a social media caption
*AiApi* | [**imageVariations**](docs/AiApi.md#imageVariations) | **POST** /{workspaceUuid}/ai/image-variations | Generate variations of an existing media image
*AiApi* | [**learnBrandVoice**](docs/AiApi.md#learnBrandVoice) | **POST** /{workspaceUuid}/brand-voice/learn | Learn a brand voice from past posts
*AiApi* | [**repurposeContent**](docs/AiApi.md#repurposeContent) | **POST** /{workspaceUuid}/ai/repurpose | Repurpose long-form content into a draft post set with a carousel
*AiApi* | [**updateBrandVoice**](docs/AiApi.md#updateBrandVoice) | **PUT** /{workspaceUuid}/brand-voice | Create or update the brand voice
*AnalyticsApi* | [**createReportExport**](docs/AnalyticsApi.md#createReportExport) | **POST** /{workspaceUuid}/reports/exports | Create a report export
*AnalyticsApi* | [**downloadReportExport**](docs/AnalyticsApi.md#downloadReportExport) | **GET** /{workspaceUuid}/reports/exports/{exportUuid}/download | Download a report file
*AnalyticsApi* | [**getAccountAnalytics**](docs/AnalyticsApi.md#getAccountAnalytics) | **GET** /{workspaceUuid}/analytics/accounts/{accountUuid} | Get account analytics
*AnalyticsApi* | [**getAnalyticsSummary**](docs/AnalyticsApi.md#getAnalyticsSummary) | **GET** /{workspaceUuid}/analytics | Get analytics summary
*AnalyticsApi* | [**getBestPostingTimes**](docs/AnalyticsApi.md#getBestPostingTimes) | **GET** /{workspaceUuid}/analytics/best-times | Get best posting times
*AnalyticsApi* | [**getPostAnalytics_0**](docs/AnalyticsApi.md#getPostAnalytics_0) | **GET** /{workspaceUuid}/posts/{postUuid}/analytics | Get post analytics
*AnalyticsApi* | [**getPostingTimes**](docs/AnalyticsApi.md#getPostingTimes) | **GET** /{workspaceUuid}/analytics/posting-times | Get posting times heatmap
*AnalyticsApi* | [**getReportBranding**](docs/AnalyticsApi.md#getReportBranding) | **GET** /{workspaceUuid}/report-branding | Get the report branding
*AnalyticsApi* | [**getReportExport**](docs/AnalyticsApi.md#getReportExport) | **GET** /{workspaceUuid}/reports/exports/{exportUuid} | Get a report export
*AnalyticsApi* | [**listReportExports**](docs/AnalyticsApi.md#listReportExports) | **GET** /{workspaceUuid}/reports/exports | List report exports
*AnalyticsApi* | [**updateReportBranding**](docs/AnalyticsApi.md#updateReportBranding) | **PUT** /{workspaceUuid}/report-branding | Update the report branding
*AnalyticsApi* | [**uploadReportBrandingLogo**](docs/AnalyticsApi.md#uploadReportBrandingLogo) | **POST** /{workspaceUuid}/report-branding/logo | Upload the report logo
*CompetitorsApi* | [**addCompetitor**](docs/CompetitorsApi.md#addCompetitor) | **POST** /{workspaceUuid}/competitors | Track a competitor
*CompetitorsApi* | [**deleteCompetitor**](docs/CompetitorsApi.md#deleteCompetitor) | **DELETE** /{workspaceUuid}/competitors/{competitorId} | Stop tracking a competitor
*CompetitorsApi* | [**getCompetitor**](docs/CompetitorsApi.md#getCompetitor) | **GET** /{workspaceUuid}/competitors/{competitorId} | Get a competitor
*CompetitorsApi* | [**listCompetitors**](docs/CompetitorsApi.md#listCompetitors) | **GET** /{workspaceUuid}/competitors | List competitors
*FreeToolsApi* | [**buildHashtagGroups**](docs/FreeToolsApi.md#buildHashtagGroups) | **POST** /tools/hashtag-group-builder | Clean, dedupe and split hashtags into groups that fit a network&#39;s hashtag cap
*FreeToolsApi* | [**buildUtmUrl**](docs/FreeToolsApi.md#buildUtmUrl) | **POST** /tools/utm-builder | Build a UTM-tagged campaign URL
*FreeToolsApi* | [**calculateAspectRatio**](docs/FreeToolsApi.md#calculateAspectRatio) | **POST** /tools/aspect-ratio-calculator | Calculate an aspect ratio, or the missing side of an image at a given ratio
*FreeToolsApi* | [**calculateCarouselSlices**](docs/FreeToolsApi.md#calculateCarouselSlices) | **POST** /tools/instagram-carousel-splitter | Split a wide image into seamless Instagram carousel slides
*FreeToolsApi* | [**calculateCrop**](docs/FreeToolsApi.md#calculateCrop) | **POST** /tools/social-media-image-sizes/crop | Calculate the crop box that fits an image to a social media size
*FreeToolsApi* | [**calculateEngagementRate**](docs/FreeToolsApi.md#calculateEngagementRate) | **POST** /tools/engagement-rate-calculator | Calculate an engagement rate
*FreeToolsApi* | [**calculateInfluencerRate**](docs/FreeToolsApi.md#calculateInfluencerRate) | **POST** /tools/influencer-rate-calculator | Estimate an influencer&#39;s rate for one sponsored deliverable
*FreeToolsApi* | [**calculateSmmPricing**](docs/FreeToolsApi.md#calculateSmmPricing) | **POST** /tools/social-media-manager-pricing-calculator | Estimate social media manager pricing
*FreeToolsApi* | [**calculateSocialRoi**](docs/FreeToolsApi.md#calculateSocialRoi) | **POST** /tools/social-media-roi-calculator | Calculate social media ROI
*FreeToolsApi* | [**calculateXApiCost**](docs/FreeToolsApi.md#calculateXApiCost) | **POST** /tools/x-api-cost-calculator | Calculate the monthly X API cost
*FreeToolsApi* | [**checkLinkPreview**](docs/FreeToolsApi.md#checkLinkPreview) | **POST** /tools/link-preview-checker | Check how a link previews on X, LinkedIn, Facebook and chat apps (Open Graph and Twitter card tags)
*FreeToolsApi* | [**checkPost**](docs/FreeToolsApi.md#checkPost) | **POST** /tools/social-media-post-checker | Check a post against each network&#39;s publishing rules
*FreeToolsApi* | [**checkReadability**](docs/FreeToolsApi.md#checkReadability) | **POST** /tools/post-readability-checker | Check the readability of a post: Flesch scores, long sentences and passive hints
*FreeToolsApi* | [**checkYoutubeThumbnail**](docs/FreeToolsApi.md#checkYoutubeThumbnail) | **POST** /tools/youtube-thumbnail-size-checker | Check a YouTube thumbnail&#39;s ratio, width, file size and format against YouTube&#39;s requirements
*FreeToolsApi* | [**cleanText**](docs/FreeToolsApi.md#cleanText) | **POST** /tools/ai-text-cleaner | Clean AI-written text: dashes, quotes, invisible characters, markdown
*FreeToolsApi* | [**countCharacters**](docs/FreeToolsApi.md#countCharacters) | **POST** /tools/social-media-character-counter | Count characters as each network counts them
*FreeToolsApi* | [**findAutomationRecipes**](docs/FreeToolsApi.md#findAutomationRecipes) | **GET** /tools/social-media-automation-recipes | Find n8n, Zapier and Make recipes that automate social media posting through the PostBoost API
*FreeToolsApi* | [**formatInstagramCaption**](docs/FreeToolsApi.md#formatInstagramCaption) | **POST** /tools/instagram-line-break-generator | Keep blank lines in an Instagram caption with spacer lines, and count it
*FreeToolsApi* | [**formatLinkedInPost**](docs/FreeToolsApi.md#formatLinkedInPost) | **POST** /tools/linkedin-post-formatter | Format a LinkedIn post with bold, italic and lists
*FreeToolsApi* | [**generateAltText**](docs/FreeToolsApi.md#generateAltText) | **POST** /tools/alt-text-generator | Write alt text for an image with AI (needs a token, spends AI credits)
*FreeToolsApi* | [**generateBio**](docs/FreeToolsApi.md#generateBio) | **POST** /tools/instagram-bio-generator | Write five profile bios with AI (needs a token, spends AI credits)
*FreeToolsApi* | [**generateCaption**](docs/FreeToolsApi.md#generateCaption) | **POST** /tools/instagram-caption-generator | Write three post captions for a topic with AI (needs a token, spends AI credits)
*FreeToolsApi* | [**generateFancyText**](docs/FreeToolsApi.md#generateFancyText) | **POST** /tools/fancy-text-generator | Convert text to fancy Unicode styles
*FreeToolsApi* | [**generateHashtags**](docs/FreeToolsApi.md#generateHashtags) | **POST** /tools/instagram-hashtag-generator | Generate hashtags for a post topic with AI (needs a token, spends AI credits)
*FreeToolsApi* | [**generateHooks**](docs/FreeToolsApi.md#generateHooks) | **POST** /tools/hook-generator | Generate hooks (opening lines) for a social media post with AI (needs a token, spends AI credits)
*FreeToolsApi* | [**generateLinkedInHeadline**](docs/FreeToolsApi.md#generateLinkedInHeadline) | **POST** /tools/linkedin-headline-generator | Write five LinkedIn profile headlines with AI (needs a token, spends AI credits)
*FreeToolsApi* | [**generateQrCode**](docs/FreeToolsApi.md#generateQrCode) | **POST** /tools/qr-code-generator | Generate a QR code (SVG) for a link or text, with optional UTM tags
*FreeToolsApi* | [**generateSocialPostsFromBlog**](docs/FreeToolsApi.md#generateSocialPostsFromBlog) | **POST** /tools/blog-to-social-media | Turn a blog post (URL or text) into one social post per network with AI (needs a token, spends AI credits)
*FreeToolsApi* | [**generateUsernames**](docs/FreeToolsApi.md#generateUsernames) | **POST** /tools/social-media-username-generator | Generate social media usernames
*FreeToolsApi* | [**generateYoutubeDescription**](docs/FreeToolsApi.md#generateYoutubeDescription) | **POST** /tools/youtube-description-generator | Write three YouTube video descriptions with AI (needs a token, spends AI credits)
*FreeToolsApi* | [**generateYoutubeTitles**](docs/FreeToolsApi.md#generateYoutubeTitles) | **POST** /tools/youtube-title-generator | Write five YouTube video titles with AI (needs a token, spends AI credits)
*FreeToolsApi* | [**getBestTimesToPost**](docs/FreeToolsApi.md#getBestTimesToPost) | **GET** /tools/best-time-to-post | Get the best times to post per network from published studies, with sources
*FreeToolsApi* | [**getGlossary**](docs/FreeToolsApi.md#getGlossary) | **GET** /tools/social-media-glossary | Look up social media terms: plain-language definitions by category, with sources and related terms
*FreeToolsApi* | [**getHookTemplates**](docs/FreeToolsApi.md#getHookTemplates) | **GET** /tools/hook-generator/library | Get free hook templates for social media posts, filtered by style and network
*FreeToolsApi* | [**getImageSizes**](docs/FreeToolsApi.md#getImageSizes) | **GET** /tools/social-media-image-sizes | Get social media image sizes per network, each with its source
*FreeToolsApi* | [**getSafeZones**](docs/FreeToolsApi.md#getSafeZones) | **POST** /tools/safe-zone-checker | Get the TikTok, Instagram Reels or YouTube Shorts safe zones for a vertical frame
*FreeToolsApi* | [**getVideoSpecs**](docs/FreeToolsApi.md#getVideoSpecs) | **GET** /tools/social-media-video-specs | Get social media video ratios, resolutions, lengths and file size limits per network, with sources
*FreeToolsApi* | [**listAwarenessDays**](docs/FreeToolsApi.md#listAwarenessDays) | **GET** /tools/social-media-holiday-calendar | List public holidays, awareness days and social media days by date, country, type and topic, with sources
*FreeToolsApi* | [**listFreeTools**](docs/FreeToolsApi.md#listFreeTools) | **GET** /tools | List the free tools
*FreeToolsApi* | [**pickSocialMediaTool**](docs/FreeToolsApi.md#pickSocialMediaTool) | **POST** /tools/social-media-tool-picker | Match your needs against social media management tools and see what each one misses
*FreeToolsApi* | [**planContentCalendar**](docs/FreeToolsApi.md#planContentCalendar) | **POST** /tools/social-media-content-calendar-generator | Plan a social media content calendar and get it as CSV and ICS
*FreeToolsApi* | [**planPostingFrequency**](docs/FreeToolsApi.md#planPostingFrequency) | **POST** /tools/posting-frequency-planner | Plan how often to post on each network
*FreeToolsApi* | [**previewPost**](docs/FreeToolsApi.md#previewPost) | **POST** /tools/social-media-post-preview | Preview where a post folds and when its image is cropped on Instagram, X, LinkedIn and Facebook
*FreeToolsApi* | [**scoreSocialAudit**](docs/FreeToolsApi.md#scoreSocialAudit) | **POST** /tools/social-media-audit-template | Score a social media audit checklist and get the top fixes
*FreeToolsApi* | [**searchEmoji**](docs/FreeToolsApi.md#searchEmoji) | **POST** /tools/social-media-emoji-picker | Search emoji by name or keyword, to copy and paste into a post
*FreeToolsApi* | [**splitThread**](docs/FreeToolsApi.md#splitThread) | **POST** /tools/x-thread-maker | Split long text into a thread
*FreeToolsApi* | [**summarizeReport**](docs/FreeToolsApi.md#summarizeReport) | **POST** /tools/social-media-report-generator | Summarize social media post metrics into a report
*FreeToolsApi* | [**verifyWebhookSignature**](docs/FreeToolsApi.md#verifyWebhookSignature) | **POST** /tools/webhook-signature-verifier | Verify an HMAC webhook signature
*HashtagGroupsApi* | [**createHashtagGroup**](docs/HashtagGroupsApi.md#createHashtagGroup) | **POST** /{workspaceUuid}/hashtag-groups | Create a hashtag group
*HashtagGroupsApi* | [**deleteHashtagGroup**](docs/HashtagGroupsApi.md#deleteHashtagGroup) | **DELETE** /{workspaceUuid}/hashtag-groups/{hashtagGroupId} | Delete a hashtag group
*HashtagGroupsApi* | [**getHashtagGroup**](docs/HashtagGroupsApi.md#getHashtagGroup) | **GET** /{workspaceUuid}/hashtag-groups/{hashtagGroupId} | Get a hashtag group
*HashtagGroupsApi* | [**listHashtagGroups**](docs/HashtagGroupsApi.md#listHashtagGroups) | **GET** /{workspaceUuid}/hashtag-groups | List hashtag groups
*HashtagGroupsApi* | [**updateHashtagGroup**](docs/HashtagGroupsApi.md#updateHashtagGroup) | **PUT** /{workspaceUuid}/hashtag-groups/{hashtagGroupId} | Update a hashtag group
*InboxApi* | [**approveInboxReplyDraft**](docs/InboxApi.md#approveInboxReplyDraft) | **POST** /{workspaceUuid}/inbox/drafts/{draftId}/approve | Approve and send a reply draft
*InboxApi* | [**createInboxReplyDraft**](docs/InboxApi.md#createInboxReplyDraft) | **POST** /{workspaceUuid}/inbox/conversations/{conversationId}/drafts | Draft a reply
*InboxApi* | [**deleteInboxReplyDraft**](docs/InboxApi.md#deleteInboxReplyDraft) | **DELETE** /{workspaceUuid}/inbox/drafts/{draftId} | Withdraw a reply draft
*InboxApi* | [**getInboxConversation**](docs/InboxApi.md#getInboxConversation) | **GET** /{workspaceUuid}/inbox/conversations/{conversationId} | Get an inbox conversation
*InboxApi* | [**getInboxReplyDraft**](docs/InboxApi.md#getInboxReplyDraft) | **GET** /{workspaceUuid}/inbox/drafts/{draftId} | Get a reply draft
*InboxApi* | [**listInboxConversations**](docs/InboxApi.md#listInboxConversations) | **GET** /{workspaceUuid}/inbox/conversations | List inbox conversations
*InboxApi* | [**listInboxReplyDrafts**](docs/InboxApi.md#listInboxReplyDrafts) | **GET** /{workspaceUuid}/inbox/drafts | List reply drafts
*InboxApi* | [**rejectInboxReplyDraft**](docs/InboxApi.md#rejectInboxReplyDraft) | **POST** /{workspaceUuid}/inbox/drafts/{draftId}/reject | Reject a reply draft
*InboxApi* | [**updateInboxConversation**](docs/InboxApi.md#updateInboxConversation) | **PATCH** /{workspaceUuid}/inbox/conversations/{conversationId} | Update an inbox conversation
*InboxApi* | [**updateInboxReplyDraft**](docs/InboxApi.md#updateInboxReplyDraft) | **PUT** /{workspaceUuid}/inbox/drafts/{draftId} | Edit a reply draft
*MediaApi* | [**abortChunkedUpload**](docs/MediaApi.md#abortChunkedUpload) | **DELETE** /{workspaceUuid}/media/chunked/{uploadUuid} | Abort chunked upload
*MediaApi* | [**completeChunkedUpload**](docs/MediaApi.md#completeChunkedUpload) | **POST** /{workspaceUuid}/media/chunked/{uploadUuid}/complete | Complete chunked upload
*MediaApi* | [**createMediaFolder**](docs/MediaApi.md#createMediaFolder) | **POST** /{workspaceUuid}/media/folders | Create media folder
*MediaApi* | [**deleteMediaBulk**](docs/MediaApi.md#deleteMediaBulk) | **DELETE** /{workspaceUuid}/media | Delete media (bulk)
*MediaApi* | [**deleteMediaFolder**](docs/MediaApi.md#deleteMediaFolder) | **DELETE** /{workspaceUuid}/media/folders/{folderUuid} | Delete media folder
*MediaApi* | [**getMedia**](docs/MediaApi.md#getMedia) | **GET** /{workspaceUuid}/media/{mediaUuid} | Get media
*MediaApi* | [**getRemoteUploadStatus**](docs/MediaApi.md#getRemoteUploadStatus) | **GET** /{workspaceUuid}/media/remote/{downloadId}/status | Get remote upload status
*MediaApi* | [**initiateChunkedUpload**](docs/MediaApi.md#initiateChunkedUpload) | **POST** /{workspaceUuid}/media/chunked/initiate | Initiate chunked upload
*MediaApi* | [**initiateRemoteUpload**](docs/MediaApi.md#initiateRemoteUpload) | **POST** /{workspaceUuid}/media/remote/initiate | Initiate remote upload
*MediaApi* | [**listMedia**](docs/MediaApi.md#listMedia) | **GET** /{workspaceUuid}/media | List media
*MediaApi* | [**listMediaFolders**](docs/MediaApi.md#listMediaFolders) | **GET** /{workspaceUuid}/media/folders | List media folders
*MediaApi* | [**updateMedia**](docs/MediaApi.md#updateMedia) | **PUT** /{workspaceUuid}/media/{mediaUuid} | Update media
*MediaApi* | [**updateMediaFolder**](docs/MediaApi.md#updateMediaFolder) | **PUT** /{workspaceUuid}/media/folders/{folderUuid} | Update media folder
*MediaApi* | [**uploadChunk**](docs/MediaApi.md#uploadChunk) | **POST** /{workspaceUuid}/media/chunked/{uploadUuid}/upload | Upload a chunk
*MediaApi* | [**uploadMedia**](docs/MediaApi.md#uploadMedia) | **POST** /{workspaceUuid}/media | Upload media (binary)
*MediaApi* | [**uploadMediaBase64**](docs/MediaApi.md#uploadMediaBase64) | **POST** /{workspaceUuid}/media/base64 | Upload media (base64 JSON)
*MentionsApi* | [**createMention**](docs/MentionsApi.md#createMention) | **POST** /{workspaceUuid}/mentions | Create mention
*MentionsApi* | [**deleteMention**](docs/MentionsApi.md#deleteMention) | **DELETE** /{workspaceUuid}/mentions/{mentionId} | Delete mention
*MentionsApi* | [**getMention**](docs/MentionsApi.md#getMention) | **GET** /{workspaceUuid}/mentions/{mentionId} | Get mention
*MentionsApi* | [**listMentions**](docs/MentionsApi.md#listMentions) | **GET** /{workspaceUuid}/mentions | List mentions
*MentionsApi* | [**updateMention**](docs/MentionsApi.md#updateMention) | **PUT** /{workspaceUuid}/mentions/{mentionId} | Update mention
*PostingScheduleApi* | [**getPostingSchedule**](docs/PostingScheduleApi.md#getPostingSchedule) | **GET** /{workspaceUuid}/posting-schedule | Get the posting schedule
*PostingScheduleApi* | [**getRecommendedPostingTimes**](docs/PostingScheduleApi.md#getRecommendedPostingTimes) | **GET** /{workspaceUuid}/posting-schedule/recommended | Get recommended posting times
*PostingScheduleApi* | [**listQueueSlots**](docs/PostingScheduleApi.md#listQueueSlots) | **GET** /{workspaceUuid}/queue/slots | List upcoming queue slots
*PostingScheduleApi* | [**resetAccountPostingSchedule**](docs/PostingScheduleApi.md#resetAccountPostingSchedule) | **DELETE** /{workspaceUuid}/posting-schedule/{accountId} | Reset an account schedule
*PostingScheduleApi* | [**updatePostingSchedule**](docs/PostingScheduleApi.md#updatePostingSchedule) | **PUT** /{workspaceUuid}/posting-schedule | Set the posting schedule
*PostsApi* | [**addPostToQueue**](docs/PostsApi.md#addPostToQueue) | **POST** /{workspaceUuid}/posts/add-to-queue/{postUuid} | Add post to queue
*PostsApi* | [**approvePost**](docs/PostsApi.md#approvePost) | **POST** /{workspaceUuid}/posts/approve/{postUuid} | Approve post
*PostsApi* | [**createPost**](docs/PostsApi.md#createPost) | **POST** /{workspaceUuid}/posts | Create post
*PostsApi* | [**createRecyclingRule**](docs/PostsApi.md#createRecyclingRule) | **POST** /{workspaceUuid}/recycling-rules | Create a recycling rule
*PostsApi* | [**createRssFeed**](docs/PostsApi.md#createRssFeed) | **POST** /{workspaceUuid}/rss-feeds | Add an RSS feed
*PostsApi* | [**deletePost**](docs/PostsApi.md#deletePost) | **DELETE** /{workspaceUuid}/posts/{postUuid} | Delete post
*PostsApi* | [**deletePostsBulk**](docs/PostsApi.md#deletePostsBulk) | **DELETE** /{workspaceUuid}/posts | Delete posts (bulk)
*PostsApi* | [**deleteRecyclingRule**](docs/PostsApi.md#deleteRecyclingRule) | **DELETE** /{workspaceUuid}/recycling-rules/{ruleUuid} | Delete a recycling rule
*PostsApi* | [**deleteRssFeed**](docs/PostsApi.md#deleteRssFeed) | **DELETE** /{workspaceUuid}/rss-feeds/{feedUuid} | Delete an RSS feed
*PostsApi* | [**getPost**](docs/PostsApi.md#getPost) | **GET** /{workspaceUuid}/posts/{postUuid} | Get post
*PostsApi* | [**getPostAnalytics**](docs/PostsApi.md#getPostAnalytics) | **GET** /{workspaceUuid}/posts/{postUuid}/analytics | Get post analytics
*PostsApi* | [**getRecyclingRule**](docs/PostsApi.md#getRecyclingRule) | **GET** /{workspaceUuid}/recycling-rules/{ruleUuid} | Get a recycling rule
*PostsApi* | [**getRssFeed**](docs/PostsApi.md#getRssFeed) | **GET** /{workspaceUuid}/rss-feeds/{feedUuid} | Get an RSS feed
*PostsApi* | [**listPosts**](docs/PostsApi.md#listPosts) | **GET** /{workspaceUuid}/posts | List posts
*PostsApi* | [**listRecyclingRules**](docs/PostsApi.md#listRecyclingRules) | **GET** /{workspaceUuid}/recycling-rules | List recycling rules
*PostsApi* | [**listRecyclingRuns**](docs/PostsApi.md#listRecyclingRuns) | **GET** /{workspaceUuid}/recycling-rules/{ruleUuid}/runs | List a recycling rule&#39;s runs
*PostsApi* | [**listRssFeeds**](docs/PostsApi.md#listRssFeeds) | **GET** /{workspaceUuid}/rss-feeds | List RSS feeds
*PostsApi* | [**pollRssFeed**](docs/PostsApi.md#pollRssFeed) | **POST** /{workspaceUuid}/rss-feeds/{feedUuid}/poll | Check an RSS feed now
*PostsApi* | [**recyclePost**](docs/PostsApi.md#recyclePost) | **POST** /{workspaceUuid}/posts/{postUuid}/recycle | Recycle a post on an interval
*PostsApi* | [**retryPostAccount**](docs/PostsApi.md#retryPostAccount) | **POST** /{workspaceUuid}/posts/retry/{postUuid}/{accountUuid} | Retry publishing to one account
*PostsApi* | [**schedulePost**](docs/PostsApi.md#schedulePost) | **POST** /{workspaceUuid}/posts/schedule/{postUuid} | Schedule post
*PostsApi* | [**updatePost**](docs/PostsApi.md#updatePost) | **PUT** /{workspaceUuid}/posts/{postUuid} | Update post
*PostsApi* | [**updateRecyclingRule**](docs/PostsApi.md#updateRecyclingRule) | **PUT** /{workspaceUuid}/recycling-rules/{ruleUuid} | Update, pause or resume a recycling rule
*PostsApi* | [**updateRssFeed**](docs/PostsApi.md#updateRssFeed) | **PUT** /{workspaceUuid}/rss-feeds/{feedUuid} | Update, pause or resume an RSS feed
*PostsApi* | [**validatePost**](docs/PostsApi.md#validatePost) | **POST** /{workspaceUuid}/posts/validate | Validate post (dry run)
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
*TemplatesApi* | [**createTemplate**](docs/TemplatesApi.md#createTemplate) | **POST** /{workspaceUuid}/templates | Create a template
*TemplatesApi* | [**deleteTemplate**](docs/TemplatesApi.md#deleteTemplate) | **DELETE** /{workspaceUuid}/templates/{templateId} | Delete a template
*TemplatesApi* | [**getTemplate**](docs/TemplatesApi.md#getTemplate) | **GET** /{workspaceUuid}/templates/{templateId} | Get a template
*TemplatesApi* | [**listTemplates**](docs/TemplatesApi.md#listTemplates) | **GET** /{workspaceUuid}/templates | List templates
*TemplatesApi* | [**updateTemplate**](docs/TemplatesApi.md#updateTemplate) | **PUT** /{workspaceUuid}/templates/{templateId} | Update a template
*UsersApi* | [**createUser**](docs/UsersApi.md#createUser) | **POST** /panel/users | Create user
*UsersApi* | [**deleteUser**](docs/UsersApi.md#deleteUser) | **DELETE** /panel/users/{userId} | Delete user
*UsersApi* | [**deleteUsersBulk**](docs/UsersApi.md#deleteUsersBulk) | **DELETE** /panel/users | Delete users (bulk)
*UsersApi* | [**getUser**](docs/UsersApi.md#getUser) | **GET** /panel/users/{userId} | Get user
*UsersApi* | [**listUsers**](docs/UsersApi.md#listUsers) | **GET** /panel/users | List users
*UsersApi* | [**updateUser**](docs/UsersApi.md#updateUser) | **PUT** /panel/users/{userId} | Update user
*WebhooksApi* | [**createWebhookSubscription**](docs/WebhooksApi.md#createWebhookSubscription) | **POST** /{workspaceUuid}/webhooks/subscriptions | Subscribe a webhook
*WebhooksApi* | [**deleteWebhookSubscription**](docs/WebhooksApi.md#deleteWebhookSubscription) | **DELETE** /{workspaceUuid}/webhooks/subscriptions/{subscriptionUuid} | Unsubscribe a webhook
*WebhooksApi* | [**listWebhookSubscriptions**](docs/WebhooksApi.md#listWebhookSubscriptions) | **GET** /{workspaceUuid}/webhooks/subscriptions | List webhook subscriptions
*WorkspacesApi* | [**addUserToWorkspace**](docs/WorkspacesApi.md#addUserToWorkspace) | **POST** /panel/workspaces/{workspaceUuid}/users | Add user to workspace
*WorkspacesApi* | [**createApiKey**](docs/WorkspacesApi.md#createApiKey) | **POST** /{workspaceUuid}/api-keys | Create a scoped API key
*WorkspacesApi* | [**createResellerClient**](docs/WorkspacesApi.md#createResellerClient) | **POST** /{workspaceUuid}/clients | Create a client workspace
*WorkspacesApi* | [**createWorkspace**](docs/WorkspacesApi.md#createWorkspace) | **POST** /panel/workspaces | Create workspace
*WorkspacesApi* | [**deleteApiKey**](docs/WorkspacesApi.md#deleteApiKey) | **DELETE** /{workspaceUuid}/api-keys/{apiKeyId} | Revoke a scoped API key
*WorkspacesApi* | [**deleteWorkspace**](docs/WorkspacesApi.md#deleteWorkspace) | **DELETE** /panel/workspaces/{workspaceUuid} | Delete workspace
*WorkspacesApi* | [**deleteWorkspacesBulk**](docs/WorkspacesApi.md#deleteWorkspacesBulk) | **DELETE** /panel/workspaces | Delete workspaces (bulk)
*WorkspacesApi* | [**getWorkspace**](docs/WorkspacesApi.md#getWorkspace) | **GET** /panel/workspaces/{workspaceUuid} | Get workspace
*WorkspacesApi* | [**getWorkspaceAICredits**](docs/WorkspacesApi.md#getWorkspaceAICredits) | **GET** /panel/workspaces/{workspaceUuid}/ai-credits | Get workspace AI credits
*WorkspacesApi* | [**getXUsage**](docs/WorkspacesApi.md#getXUsage) | **GET** /{workspaceUuid}/usage/x | X (Twitter) usage
*WorkspacesApi* | [**listApiKeys**](docs/WorkspacesApi.md#listApiKeys) | **GET** /{workspaceUuid}/api-keys | List scoped API keys
*WorkspacesApi* | [**listMyWorkspaces**](docs/WorkspacesApi.md#listMyWorkspaces) | **GET** /workspaces | List my workspaces
*WorkspacesApi* | [**listResellerClients**](docs/WorkspacesApi.md#listResellerClients) | **GET** /{workspaceUuid}/clients | List client workspaces
*WorkspacesApi* | [**listWorkspaces**](docs/WorkspacesApi.md#listWorkspaces) | **GET** /panel/workspaces | List workspaces
*WorkspacesApi* | [**removeUserFromWorkspace**](docs/WorkspacesApi.md#removeUserFromWorkspace) | **DELETE** /panel/workspaces/{workspaceUuid}/users | Remove user from workspace
*WorkspacesApi* | [**updateWorkspace**](docs/WorkspacesApi.md#updateWorkspace) | **PUT** /panel/workspaces/{workspaceUuid} | Update workspace
*WorkspacesApi* | [**updateWorkspaceUser**](docs/WorkspacesApi.md#updateWorkspaceUser) | **PUT** /panel/workspaces/{workspaceUuid}/users | Update user role in workspace

---

## Links

- Docs and quick start: https://postboost.co/docs/quickstart
- API reference: https://postboost.co/docs/api
- MCP server for AI agents: https://postboost.co/docs/mcp
- All PostBoost open-source projects: https://github.com/postboost-co
- Awesome PostBoost: https://github.com/postboost-co/awesome-postboost

## Authentication

Create an API token in PostBoost under **Settings → Access Tokens** and pass it as a Bearer token. Never commit tokens; read them from an environment variable such as `POSTBOOST_API_TOKEN`.

## Contributing

This Java SDK is generated from the [PostBoost OpenAPI spec](https://postboost.co/docs/api). Bugs and feature requests: open an issue in [postboost-java](https://github.com/postboost-co/postboost-java/issues). Generated code is overwritten on every release, so fixes usually land in the spec or the generator templates; see [CONTRIBUTING.md](CONTRIBUTING.md).

Security issues: see [SECURITY.md](SECURITY.md). Questions: hi@postboost.co.

## License

MIT, see [LICENSE](LICENSE).

---

## Links

- Docs and quick start: https://postboost.co/docs/quickstart
- API reference: https://postboost.co/docs/api
- MCP server for AI agents: https://postboost.co/docs/mcp
- All PostBoost open-source projects: https://github.com/postboost-co
- Awesome PostBoost: https://github.com/postboost-co/awesome-postboost

## Authentication

Create an API token in PostBoost under **Settings → Access Tokens** and pass it as a Bearer token. Never commit tokens; read them from an environment variable such as `POSTBOOST_API_TOKEN`.

## Contributing

This Java SDK is generated from the [PostBoost OpenAPI spec](https://postboost.co/docs/api). Bugs and feature requests: open an issue in [postboost-java](https://github.com/postboost-co/postboost-java/issues). Generated code is overwritten on every release, so fixes usually land in the spec or the generator templates; see [CONTRIBUTING.md](CONTRIBUTING.md).

Security issues: see [SECURITY.md](SECURITY.md). Questions: hi@postboost.co.

## License

MIT, see [LICENSE](LICENSE).
