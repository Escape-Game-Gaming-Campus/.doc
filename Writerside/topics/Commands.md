# Commands

## GET



### **Hello world**

Renvoie "Hello world!"

- __Path__: [/helloWorld](http://localhost:3001/helloWorld)
- __Input__: Aucun
- __Output__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | message | string | Retourne "Hello world!" | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "message": "string"
}
```
  </tab>
</tabs>

- __Utilisation de Pusher__: [helloWorld](Pusher.md#helloworld)


### **Get players**

Get tout les players ou un player en particulier

- __Path__: [/players/get](http://localhost:3001/players/get)
- __Input__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | ID | number | L'id du player à get | true |
| ↳ | name | string | Le nom du player à get | true |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "ID": "number",
  "name": "string"
}
```
  </tab>
</tabs>

- __Output__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | players | list [ ] |  |  |
| │↳ | [ ] | object { } |  |  |
| ││↳ | ID | number | L'id du player get | false |
| ││↳ | name | string | le nom du player | false |
| ││↳ | position | number[ ] | Liste de 3 valeurs tels un Vect3 correspondant au positions du joueur | false |
| ↳ | message | string | message d'erreur/de succès | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "players": [
    {
      "ID": "number",
      "name": "string",
      "position": "number[]"
    }
  ],
  "message": "string"
}
```
  </tab>
</tabs>

- __Utilisation de Pusher__: [updatePlayers](Pusher.md#updateplayers)


### **Update**

Met à jour les clients (lancer à chaque fois qu'un client se (re)connecte, et au lancement de l'API)

- __Path__: [/update](http://localhost:3001/update)
- __Input__: Aucun
- __Output__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | message | string | message d'erreur/de succès | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "message": "string"
}
```
  </tab>
</tabs>

- __Utilisation de Pusher__: [helloWorld](Pusher.md#helloworld) [notesChange](Pusher.md#noteschange) [updatePlayers](Pusher.md#updateplayers) [updateInventory](Pusher.md#updateinventory) [hallWay2TryPsd](Pusher.md#hallway2trypsd) [ddust2TryPsd](Pusher.md#ddust2trypsd) [updateLightbulbs](Pusher.md#updatelightbulbs)
## POST



### **Try PasswordPC DDust2**

Permet de vérifier si le mot de passe pour débloquer Totoro est bon

- __Path__: [/ddust2/tryPsd](http://localhost:3001/ddust2/tryPsd)
- __Input__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | psd | string | Mot de passe a essayer | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "psd": "string"
}
```
  </tab>
</tabs>

- __Output__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | message | string | message d'erreur/de succès | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "message": "string"
}
```
  </tab>
</tabs>

- __Utilisation de Pusher__: [ddust2TryPsd](Pusher.md#ddust2trypsd)


### **Try PasswordPC HallWay2**

Enigme scene de crime pour avoir une ampoule rouge

- __Path__: [/hallWay2/tryPsd](http://localhost:3001/hallWay2/tryPsd)
- __Input__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | psd | string | Mot de passe a essayer | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "psd": "string"
}
```
  </tab>
</tabs>

- __Output__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | message | string | message d'erreur/de succès | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "message": "string"
}
```
  </tab>
</tabs>

- __Utilisation de Pusher__: [updateInventory](Pusher.md#updateinventory) [hallWay2TryPsd](Pusher.md#hallway2trypsd)


### **Add to inventory**

Ajoute un objet à l'inventaire

- __Path__: [/inv/add](http://localhost:3001/inv/add)
- __Input__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | objs | list [ ] |  |  |
| │↳ | [ ] | object { } |  |  |
| ││↳ | name | string | Nom de l'objet à ajouter (facultatif si utilise le UUID) | false |
| ││↳ | uuid | number | UUID de l'objet à ajouter (facultatif si utilise le nom) | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "objs": [
    {
      "name": "string",
      "uuid": "number"
    }
  ]
}
```
  </tab>
</tabs>

- __Output__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | message | string | message d'erreur/de succès | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "message": "string"
}
```
  </tab>
</tabs>

- __Utilisation de Pusher__: [updateInventory](Pusher.md#updateinventory)


### **Add Bulb to list**

Ajoute une ampoule à la liste

- __Path__: [/lightbulbs/add](http://localhost:3001/lightbulbs/add)
- __Input__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | objs | list [ ] |  |  |
| │↳ | [ ] | object { } |  |  |
| ││↳ | name | string | Nom de l'ampoule à poser (facultatif si utilise le UUID) | false |
| ││↳ | uuid | number | UUID de l'ampoule à poser (facultatif si utilise le nom) | false |
| ││↳ | base | number | numéro du socle sur lequel est l'ampoule (0 | 1 | 2) | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "objs": [
    {
      "name": "string",
      "uuid": "number",
      "base": "number"
    }
  ]
}
```
  </tab>
</tabs>

- __Output__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | message | string | message d'erreur/de succès | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "message": "string"
}
```
  </tab>
</tabs>

- __Utilisation de Pusher__: [updateLightbulbs](Pusher.md#updatelightbulbs)


### **Switch on a lightbulb**

Allumer une ampoule

- __Path__: [/lightbulbs/switchon](http://localhost:3001/lightbulbs/switchon)
- __Input__: Aucun
- __Output__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | message | string | message d'erreur/de succès | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "message": "string"
}
```
  </tab>
</tabs>

- __Utilisation de Pusher__: Non


### **Notes changes**

Change les notes de l'équipe

- __Path__: [/notesChanges](http://localhost:3001/notesChanges)
- __Input__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | notes | string | La nouvelle note de l'équipe | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "notes": "string"
}
```
  </tab>
</tabs>

- __Output__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | message | string | message d'erreur/de succès | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "message": "string"
}
```
  </tab>
</tabs>

- __Utilisation de Pusher__: [notesChange](Pusher.md#noteschange)


### **Delete players**

Supprime des joueurs (par leur nom ou leur id)

- __Path__: [/players/delete](http://localhost:3001/players/delete)
- __Input__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | players | list [ ] |  |  |
| │↳ | [ ] | object { } |  |  |
| ││↳ | ID | number | L'id du player à détruire (facultatif si utilise le name) | false |
| ││↳ | name | string | Le nom du player à détruire (facultatif si utilise l'id) | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "players": [
    {
      "ID": "number",
      "name": "string"
    }
  ]
}
```
  </tab>
</tabs>

- __Output__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | message | string | message d'erreur/de succès | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "message": "string"
}
```
  </tab>
</tabs>

- __Utilisation de Pusher__: [updatePlayers](Pusher.md#updateplayers)


### **New players**

Ajoute des joueurs (par leur nom ou leur id)

- __Path__: [/players/add](http://localhost:3001/players/add)
- __Input__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | players | list [ ] |  |  |
| │↳ | [ ] | object { } |  |  |
| ││↳ | ID | number | L'id du player à détruire (facultatif si utilise le name) | false |
| ││↳ | name | string | Le nom du player à détruire (facultatif si utilise l'id) | false |
| ││↳ | position | number[ ] | 3 nombres tels un vect3 qui définissent la position du joueur | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "players": [
    {
      "ID": "number",
      "name": "string",
      "position": "number[]"
    }
  ]
}
```
  </tab>
</tabs>

- __Output__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | message | string | message d'erreur/de succès | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "message": "string"
}
```
  </tab>
</tabs>

- __Utilisation de Pusher__: [updatePlayers](Pusher.md#updateplayers)


### **Update player**

Met à jour un joueur (par son nom ou son id)

- __Path__: [/players/update](http://localhost:3001/players/update)
- __Input__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | players | list [ ] |  |  |
| │↳ | [ ] | object { } |  |  |
| ││↳ | ID | number | L'id du player à détruire (facultatif si utilise le name) | false |
| ││↳ | name | string | Le nom du player à détruire (facultatif si utilise l'id) | false |
| ││↳ | position | number[ ] | 3 nombres tels un vect3 qui définissent la position du joueur | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "players": [
    {
      "ID": "number",
      "name": "string",
      "position": "number[]"
    }
  ]
}
```
  </tab>
</tabs>

- __Output__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | message | string | message d'erreur/de succès | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "message": "string"
}
```
  </tab>
</tabs>

- __Utilisation de Pusher__: [updatePlayers](Pusher.md#updateplayers)
## DELETE



### **Remove to inventory**

Retire un objet de l'inventaire

- __Path__: [/inv/remove](http://localhost:3001/inv/remove)
- __Input__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | objs | list [ ] |  |  |
| │↳ | [ ] | object { } |  |  |
| ││↳ | name | string | Nom de l'objet à ajouter (facultatif si utilise le UUID) | false |
| ││↳ | uuid | number | UUID de l'objet à ajouter (facultatif si utilise le nom) | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "objs": [
    {
      "name": "string",
      "uuid": "number"
    }
  ]
}
```
  </tab>
</tabs>

- __Output__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | message | string | message d'erreur/de succès | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "message": "string"
}
```
  </tab>
</tabs>

- __Utilisation de Pusher__: [updateInventory](Pusher.md#updateinventory)


### **Remove Bulb to list**

Retire une ampoule à la liste

- __Path__: [/lightbulbs/remove](http://localhost:3001/lightbulbs/remove)
- __Input__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | bases | number[ ] | Numéro de la/les base(s) à vider | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "bases": "number[]"
}
```
  </tab>
</tabs>

- __Output__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | message | string | message d'erreur/de succès | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "message": "string"
}
```
  </tab>
</tabs>

- __Utilisation de Pusher__: [updateLightbulbs](Pusher.md#updatelightbulbs)
