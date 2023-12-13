# Pusher

## DEV



### **helloWorld**

Sends a hello world message to the client

- __Input__: Aucune
- __Output__: 

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | message | string | The hello world message | false |


### **notesChange**

Change notes informations from players

- __Input__: Aucune
- __Output__: 

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | notes | string | The notes of the team | false |
## INVENTORY



### **updateInventory**

Sends the updated inventory to the client

- __Input__: Aucune
- __Output__: 

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | [ ] | list [ ] |  |  |
| ↳ | [ ] | object { } |  |  |
| │↳ | name | string | The name of the object | false |
| │↳ | UUID | number | The UUID of the object | false |
| │↳ | texture | string | The texture of the object | false |
## ENIGMS



### **ddust2TryPsd**

Try a password to unlock Totoro

- __Input__: 

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | psdValid | boolean | Envoie si le password a été entrée correctement | false |
- __Output__: 

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | valid | boolean | Retourne si le password a été entrée correctement | false |
