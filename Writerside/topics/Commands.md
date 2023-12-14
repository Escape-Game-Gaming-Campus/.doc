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

- __Utilisation de Pusher__: [helloWorld](Pusher.md#helloworld) [notesChange](Pusher.md#noteschange) [updateInventory](Pusher.md#updateinventory) [ddust2TryPsd](Pusher.md#ddust2trypsd)
## POST



### **Try PasswordPC**

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
