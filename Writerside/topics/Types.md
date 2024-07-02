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