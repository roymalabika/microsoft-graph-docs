---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewEducationOutcome()
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.educationPointsOutcome", 
points := graphmodels.New()
"@odata.type" := "#microsoft.graph.educationAssignmentPointsGrade"
points.Set"@odata.type"(&"@odata.type") 
points := int32(85.0)
points.SetPoints(&points) 
	requestBody.SetPoints(points)
}
requestBody.SetAdditionalData(additionalData)

graphClient.Education().ClassesById("educationClass-id").AssignmentsById("educationAssignment-id").SubmissionsById("educationSubmission-id").OutcomesById("educationOutcome-id").Patch(requestBody)


```