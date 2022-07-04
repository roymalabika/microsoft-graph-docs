---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewChannel()
displayName := "UpdateChannelModeration"
requestBody.SetDisplayName(&displayName) 
description := "Update channel moderation."
requestBody.SetDescription(&description) 
additionalData := map[string]interface{}{
moderationSettings := graphmodels.New()
userNewMessageRestriction := "moderators"
moderationSettings.SetUserNewMessageRestriction(&userNewMessageRestriction) 
replyRestriction := "everyone"
moderationSettings.SetReplyRestriction(&replyRestriction) 
	allowNewMessageFromBots := true
moderationSettings.SetAllowNewMessageFromBots(&allowNewMessageFromBots) 
	allowNewMessageFromConnectors := true
moderationSettings.SetAllowNewMessageFromConnectors(&allowNewMessageFromConnectors) 
	requestBody.SetModerationSettings(moderationSettings)
}
requestBody.SetAdditionalData(additionalData)

graphClient.TeamsById("team-id").ChannelsById("channel-id").Patch(requestBody)


```