---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewChannel()
displayName := "TestChannelModeration"
requestBody.SetDisplayName(&displayName) 
description := "Test channel moderation."
requestBody.SetDescription(&description) 
membershipType := graphmodels.STANDARD_CHANNELMEMBERSHIPTYPE 
requestBody.SetMembershipType(&membershipType) 
additionalData := map[string]interface{}{
moderationSettings := graphmodels.New()
userNewMessageRestriction := "everyoneExceptGuests"
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

result, err := graphClient.TeamsById("team-id").Channels().Post(requestBody)


```