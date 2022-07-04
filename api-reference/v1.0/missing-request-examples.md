---
title: "Define the /me as singleton"
description: "These are things I had to add in the docs to make sure the Markdown-Scanner"
ms.localizationpriority: medium
author: ""
ms.prod: ""
doc_type: conceptualPageType
---

# Helpers (examples that aren't included in the docs)

These are things I had to add in the docs to make sure the Markdown-Scanner
tool was able to properly handle the Graph docs.


## Define the /me as singleton


# [HTTP](#tab/http)
<!-- {"blockType": "request", "name": "get_current_user" } -->
```msgraph-interactive
GET https://graph.microsoft.com/v1.0/me
```

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/get-current-user-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


<!-- {"blockType": "response", "@odata.type": "microsoft.graph.user", truncated: true } -->
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
}
```


## Define drives as an queryable entityset

# [HTTP](#tab/http)
<!-- {"blockType": "request", "name": "get_drive_from_id" } -->
```msgraph-interactive
GET https://graph.microsoft.com/v1.0/drives/{drive-id}
```

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/get-drive-from-id-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


<!-- {"blockType": "response", "@odata.type": "microsoft.graph.drive", truncated: true } -->
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
}
```


## define users as an queryable entityset


# [HTTP](#tab/http)
<!-- {"blockType": "request", "name": "get_users_1" } -->
```msgraph-interactive
GET https://graph.microsoft.com/v1.0/users/{user-id}
```

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/get-users-1-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


<!-- {"blockType": "response", "@odata.type": "microsoft.graph.user", truncated: true } -->
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d73
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Missing Requests",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->
