---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

// Code snippets are only available for the latest version. Current version is 5.x

// Dependencies
using Microsoft.Graph.Models;

var requestBody = new Subscription
{
	ChangeType = "created,updated",
	NotificationUrl = "https://webhook.azurewebsites.net/api/resourceNotifications",
	Resource = "/teams/{id}/channels/{id}/messages",
	IncludeResourceData = true,
	EncryptionCertificate = "{base64encodedCertificate}",
	EncryptionCertificateId = "{customId}",
	ExpirationDateTime = DateTimeOffset.Parse("2019-09-19T11:00:00.0000000Z"),
	ClientState = "{secretClientState}",
};

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=csharp
var result = await graphClient.Subscriptions.PostAsync(requestBody);


```