---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewAccessReviewScheduleDefinition()
displayName := "Group Multi-stage Access Review"
requestBody.SetDisplayName(&displayName) 
descriptionForAdmins := "New scheduled access review"
requestBody.SetDescriptionForAdmins(&descriptionForAdmins) 
descriptionForReviewers := "If you have any questions, contact jerry@contoso.com"
requestBody.SetDescriptionForReviewers(&descriptionForReviewers) 
scope := graphmodels.NewAccessReviewScope()
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.accessReviewQueryScope", 
	"query" : "/groups/02f3bafb-448c-487c-88c2-5fd65ce49a41/transitiveMembers", 
	"queryType" : "MicrosoftGraph", 
}
scope.SetAdditionalData(additionalData)
requestBody.SetScope(scope)
settings := graphmodels.NewAccessReviewScheduleSettings()
mailNotificationsEnabled := true
settings.SetMailNotificationsEnabled(&mailNotificationsEnabled) 
reminderNotificationsEnabled := true
settings.SetReminderNotificationsEnabled(&reminderNotificationsEnabled) 
justificationRequiredOnApproval := true
settings.SetJustificationRequiredOnApproval(&justificationRequiredOnApproval) 
defaultDecisionEnabled := false
settings.SetDefaultDecisionEnabled(&defaultDecisionEnabled) 
defaultDecision := "None"
settings.SetDefaultDecision(&defaultDecision) 
instanceDurationInDays := int32(4)
settings.SetInstanceDurationInDays(&instanceDurationInDays) 
recurrence := graphmodels.NewPatternedRecurrence()
pattern := graphmodels.NewRecurrencePattern()
type := graphmodels.WEEKLY_RECURRENCEPATTERNTYPE 
pattern.SetType(&type) 
interval := int32(1)
pattern.SetInterval(&interval) 
recurrence.SetPattern(pattern)
range := graphmodels.NewRecurrenceRange()
type := graphmodels.NOEND_RECURRENCERANGETYPE 
range.SetType(&type) 
startDate := "2020-09-08T12:02:30.667Z"
range.SetStartDate(&startDate) 
recurrence.SetRange(range)
settings.SetRecurrence(recurrence)
additionalData := map[string]interface{}{
	decisionHistoriesForReviewersEnabled := true
settings.SetDecisionHistoriesForReviewersEnabled(&decisionHistoriesForReviewersEnabled) 
}
settings.SetAdditionalData(additionalData)
requestBody.SetSettings(settings)
additionalData := map[string]interface{}{


 := graphmodels.New()
stageId := "1"
.SetStageId(&stageId) 
durationInDays := int32(2)
.SetDurationInDays(&durationInDays) 
recommendationsEnabled := false
.SetRecommendationsEnabled(&recommendationsEnabled) 
decisionsThatWillMoveToNextStage := []String {
	"NotReviewed",
	"Approve",

}
.SetDecisionsThatWillMoveToNextStage(decisionsThatWillMoveToNextStage)


 := graphmodels.New()
query := "/users/398164b1-5196-49dd-ada2-364b49f99b27"
.SetQuery(&query) 
queryType := "MicrosoftGraph"
.SetQueryType(&queryType) 

reviewers := []graphmodels.Objectable {
	,

}
.SetReviewers(reviewers)
 := graphmodels.New()
stageId := "2"
.SetStageId(&stageId) 
dependsOn := []String {
	"1",

}
.SetDependsOn(dependsOn)
durationInDays := int32(2)
.SetDurationInDays(&durationInDays) 
recommendationsEnabled := true
.SetRecommendationsEnabled(&recommendationsEnabled) 


 := graphmodels.New()
query := "./manager"
.SetQuery(&query) 
queryType := "MicrosoftGraph"
.SetQueryType(&queryType) 
queryRoot := "decisions"
.SetQueryRoot(&queryRoot) 

reviewers := []graphmodels.Objectable {
	,

}
.SetReviewers(reviewers)


 := graphmodels.New()
query := "/groups/072ac5f4-3f13-4088-ab30-0a276f3e6322/transitiveMembers"
.SetQuery(&query) 
queryType := "MicrosoftGraph"
.SetQueryType(&queryType) 

fallbackReviewers := []graphmodels.Objectable {
	,

}
.SetFallbackReviewers(fallbackReviewers)

	stageSettings := []graphmodels.Objectable {
		,
		,

	}
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.IdentityGovernance().AccessReviews().Definitions().Post(requestBody)


```