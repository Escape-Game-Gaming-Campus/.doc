# Lifx

Exemple de changement de light:

```Typescript
    const GCLight = lights.getLight({label: "GC light"});
    GCLight?.setState({power: "on", brightness: 1.0}, () => {
        console.log(GCLight?.Power)
    });
```

à partir d'un group:

```Typescript
    const GCLight = lights.getGroup({name: "Bedroom"});
    GCLight?.setState({power: "on", brightness: 1.0}, (res) => {
        console.log(GCLight.getLight({label: "GC light"})?.Power)
    });
```

à partir d'une location:

```Typescript
    const GCLight = lights.getLocation({name: "Home"});
    GCLight?.setState({power: "on", brightness: 1.0}, (res) => {
        console.log(GCLight.getLight({label: "GC light"})?.Power)
    });
```

parmis toute les lampes:

```Typescript
    lights.setStates({power: "on", brightness: 1.0}, (res) => {
        console.log(lights.getLight({label: "GC light"})?.Power)
    });
```

Possibilité d'ajouter un **callback** au setState()  
Puis possibilité d'ajouter un autre paramètre nommer **random** au setStates(), un _boolean_ (après le **callback**, laisser le **callback** vide si besoin) qui permet de dire s'il faut séléctionner **une light aléatoire** (`true`) ou s'il faut **toutes les séléctionner** (`false`), impossible si le setState() se fait sur une seul lampe précise comme c'est le cas avec le tout premier exemple
