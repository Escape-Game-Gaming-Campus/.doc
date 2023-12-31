# Pusher

## DEV



### **helloWorld**

Envoie un message Hello World aux clients

- __Input__: Aucun
- __Output__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | message | string | The hello world message | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "message": "string"
}
```
  </tab>
</tabs>



### **notesChange**

Envoie les notes de l'équipe à jour

- __Input__: Aucun
- __Output__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | notes | string | Envoie aux clients la dernière note à jour | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "notes": "string"
}
```
  </tab>
</tabs>

## INVENTORY



### **updateInventory**

Envoye la liste des objets de l'inventaire à jour

- __Input__: Aucun
- __Output__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | [ ] | list [ ] |  |  |
| ↳ | [ ] | object { } |  |  |
| │↳ | name | string | Nom de l'objet | false |
| │↳ | UUID | number | UUID de l'objet | false |
| │↳ | texture | string | Lien pour accéder à la texture de l'objet (utiliser de préférence AppConfig.json pour obtenir le lien quand il est set) | false |

  </tab><tab group-key="Json" title="JSON">

```json
[
  {
    "name": "string",
    "UUID": "number",
    "texture": "string"
  }
]
```
  </tab>
</tabs>

## ENIGMS



### **ddust2TryPsd**

Envoie aux clients si le password a été entrée correctement, mais uniquement si l'état de découverte du password a changé (possibiliter de forcer l'envoie avec le paramètre force)

- __Input__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | psdValid | boolean | Si le password a été entrée avec succès par un client, envoyer true ici | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "psdValid": "boolean"
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
| ↳ | valid | boolean | Renvoie aux clients si le password a été entrée correctement | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "valid": "boolean"
}
```
  </tab>
</tabs>



### **hallWay2TryPsd**

Envoie aux clients si le password a été entrée correctement, mais uniquement si l'état de découverte du password a changé (possibiliter de forcer l'envoie avec le paramètre force)

- __Input__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | { } | object { } |  |  |
| ↳ | psdValid | boolean | Si le password a été entrée avec succès par un client, envoyer true ici | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "psdValid": "boolean"
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
| ↳ | valid | boolean | Renvoie aux clients si le password a été entrée correctement | false |

  </tab><tab group-key="Json" title="JSON">

```json
{
  "valid": "boolean"
}
```
  </tab>
</tabs>

## PLAYERS



### **updatePlayers**

Met à jour les players pour les clients

- __Input__: Aucun
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

## LIGHTBULBS



### **updateLightbulbs**

Envoie la liste des ampoules à jour

- __Input__: Aucun
- __Output__: 

<tabs group="JsonOrTable">
  <tab group-key="Table" title="Tableau">

| | Nom | Type | Description | optional |
| --- | --- | --- | --- | --- |
|  | [ ] | list [ ] |  |  |
| ↳ | [ ] | object { } |  |  |
| │↳ | place | boolean | Si l'ampoule est placer | false |
| │↳ | lightColor | number[ ] | Couleur de la lumière (en vect3) | false |
| │↳ | valid | boolean | Si l'ampoule est valide | false |

  </tab><tab group-key="Json" title="JSON">

```json
[
  {
    "place": "boolean",
    "lightColor": "number[]",
    "valid": "boolean"
  }
]
```
  </tab>
</tabs>

