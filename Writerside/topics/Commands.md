# Commands

## GET



### **Hello world**

Sends a hello world message to the client

- __Path__: [/helloWorld](http://localhost:3001/helloWorld)
- __Input__: Aucune
- __Output__: 

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | message | string | Retourne "Hello world!" | false |


### **Update**

Updates the client

- __Path__: [/update](http://localhost:3001/update)
- __Input__: 

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
- __Output__: 

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
## POST



### **Try PasswordPC**

Try a password to unlock Totoro

- __Path__: [/ddust2/tryPsd](http://localhost:3001/ddust2/tryPsd)
- __Input__: 

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | psd | string | The password to try | false |
- __Output__: 

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | message | string | The message to display | false |


### **Add to inventory**

Adds an item to the inventory

- __Path__: [/inv/add](http://localhost:3001/inv/add)
- __Input__: 

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | objs | list [ ] |  |  |
| │↳ | [ ] | object { } |  |  |
| ││↳ | name | string | The name of the object to add | true |
| ││↳ | uuid | number | The uuid of the object to add | true |
- __Output__: 

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | success | boolean | If the item was added | false |
| ↳ | message | string | The message to display | true |


### **Notes changes**

Change notes informations from players

- __Path__: [/notesChanges](http://localhost:3001/notesChanges)
- __Input__: 

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
- __Output__: 

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
## DELETE



### **Remove to inventory**

Removes an item to the inventory

- __Path__: [/inv/remove](http://localhost:3001/inv/remove)
- __Input__: 

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
- __Output__: 

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
