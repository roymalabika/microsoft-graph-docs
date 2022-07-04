---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

headers := map[string]string{
	"Prefer": "outlook.timezone=\"Pacific Standard Time\"",
}
configuration := &graphconfig.FindMeetingTimesRequestBuilderPostRequestConfiguration{
	Headers: headers,
}
requestBody := graphmodels.NewFindMeetingTimesPostRequestBody()


attendeeBase := graphmodels.NewAttendeeBase()
additionalData := map[string]interface{}{
	"type" : "required", 
emailAddress := graphmodels.New()
name := "Alex Wilbur"
emailAddress.SetName(&name) 
address := "alexw@contoso.onmicrosoft.com"
emailAddress.SetAddress(&address) 
	attendeeBase.SetEmailAddress(emailAddress)
}
attendeeBase.SetAdditionalData(additionalData)

attendees := []graphmodels.AttendeeBaseable {
	attendeeBase,

}
requestBody.SetAttendees(attendees)
locationConstraint := graphmodels.NewLocationConstraint()
isRequired := "false"
locationConstraint.SetIsRequired(&isRequired) 
suggestLocation := "false"
locationConstraint.SetSuggestLocation(&suggestLocation) 


locationConstraintItem := graphmodels.NewLocationConstraintItem()
additionalData := map[string]interface{}{
	"resolveAvailability" : "false", 
	"displayName" : "Conf room Hood", 
}
locationConstraintItem.SetAdditionalData(additionalData)

locations := []graphmodels.LocationConstraintItemable {
	locationConstraintItem,

}
locationConstraint.SetLocations(locations)
requestBody.SetLocationConstraint(locationConstraint)
timeConstraint := graphmodels.NewTimeConstraint()
activityDomain := graphmodels.WORK_ACTIVITYDOMAIN 
timeConstraint.SetActivityDomain(&activityDomain) 


timeSlot := graphmodels.NewTimeSlot()
start := graphmodels.NewDateTimeTimeZone()
dateTime := "2019-04-16T09:00:00"
start.SetDateTime(&dateTime) 
timeZone := "Pacific Standard Time"
start.SetTimeZone(&timeZone) 
timeSlot.SetStart(start)
end := graphmodels.NewDateTimeTimeZone()
dateTime := "2019-04-18T17:00:00"
end.SetDateTime(&dateTime) 
timeZone := "Pacific Standard Time"
end.SetTimeZone(&timeZone) 
timeSlot.SetEnd(end)

timeSlots := []graphmodels.TimeSlotable {
	timeSlot,

}
timeConstraint.SetTimeSlots(timeSlots)
requestBody.SetTimeConstraint(timeConstraint)
isOrganizerOptional := "false"
requestBody.SetIsOrganizerOptional(&isOrganizerOptional) 
meetingDuration := "PT1H"
requestBody.SetMeetingDuration(&meetingDuration) 
returnSuggestionReasons := "true"
requestBody.SetReturnSuggestionReasons(&returnSuggestionReasons) 
minimumAttendeePercentage := graphmodels.100_ 
requestBody.SetMinimumAttendeePercentage(&minimumAttendeePercentage) 

result, err := graphClient.Me().FindMeetingTimes().PostWithRequestConfigurationAndResponseHandler(requestBody, configuration, nil)


```