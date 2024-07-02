# Types

## Image
C'est défini avec les données d'un form, vous pouvez utiliser le générateur de forms pour transformer toutes vos données en form, et ajouter une image aux données envoyées
```Typescript
// Front
import { Utils } from 'Utils'

const formDataExample : FormData = Utils.FormDataCreator(datas);
```

## mdTemplate
C'est un type qui permet de stocker un string sous 2 formats: en markdown et en html.
Mais les données sont les mêmes, simplement écrite différement
```json
{
    "md": "",
    "html": ""
}
```
```Typescript
// Back
import Types from "utils/types";

const mdTemplateExample : Types.mdTemplateType = Types.mdTemplate;
```

## Colors
Lorsqu'une couleurs est ajouter à la bdd, un nom lui est associer en fonctions de l'ordre des variables, il peux donc être nécessaire d'obtenir sont nom.
```json
{
    "name": "",
    "color": ""
}
```
```Typescript
// Back
import Types from "utils/types";

const colorsTemplateExample : Types.colorsType = Types.colorsTemplate;
```

## PlayersInfoReduce
Voici les infos de base d'un user, souvent utiliser dans les teams/structure, expliquant le mot "players"

`profil_picture is facultative`
```json
{
    "id": 0,
    "pseudo": "",
    "profil_picture": "",
    "status": ""
}
```
```Typescript
// Back
import Types from "utils/types";

const playersInfoReduceTemplateExample : Types.playersInfoReduceType = Types.playersInfoReduceTemplate;
```