# Swagger ToDo
This is a sample ToDo server.  

## Version: 1.0.0

### Terms of service
<http://swagger.io/terms/>

**Contact information:**  
apiteam@swagger.io  

**License:** [Apache 2.0](http://www.apache.org/licenses/LICENSE-2.0.html)

### /Items/postItem/{itemId}

#### POST
##### Summary

Adds an item

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| itemName | body | item that needs to be added | Yes | string |
| desc | body | description of the item | No | string |
| due | body | due date of the item | Yes | string |


##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Successful! |
| 400 | Invalid input |
| 500 | Internal Server Error |

### /Items/findByStatus

#### GET
##### Summary

Finds items by status

##### Description

Multiple status values can be provided with comma separated strings

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| status | query | Status values that need to be considered for filter | Yes | [ string ] |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Successful! |
| 400 | Invalid status |
| 404 | Item not found |
| 500 | Internal Server Error |

### /ToDo/upadteItem

#### PUT
##### Summary

Update an existing item

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| itemId | path | item that needs to be updated | Yes | string |
| desc | body | Updated description of the item | No | string |
| due | body | Updated due date of the item | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Successful! |
| 400 | Invalid ID supplied |
| 404 | Item not found |
| 500 | Internal Server Error |

### /Items/deleteItem/{itemId}

#### DELETE
##### Summary

Deletes an item

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| itemId | path | Item to delete | Yes | long |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Successful! |
| 400 | Invalid ID supplied |
| 404 | Item not found |
| 500 | Internal Server Error |
