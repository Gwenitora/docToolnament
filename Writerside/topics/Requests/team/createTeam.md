## Create team `POST` `/teams/new`
Commande pour créer une équipe

<chapter title="CAN USE COMMAND">
<p>
    user
</p>
</chapter>

<chapter title="BODY">
<tabs group="Lang">
    <tab title="Tableau" group-key="tab">
<table>
    <tr>
        <td>Name</td><td>Type</td><td>Description</td><td>Facultative</td><td>Default</td>
    </tr>
    <tr>
        <td>logo</td><td><a href="Types.md#image">Image</a></td><td>Logo de l'équipe</td><td>true</td><td>Une des images par défaut pour les équipes</td>
    </tr>
    <tr>
        <td>team_picture</td><td><a href="Types.md#image">Image</a></td><td>Une photo de l'équipe</td><td>true</td><td></td>
    </tr>
    <tr>
        <td>name</td><td>string</td><td>Nom de l'équipe<br/>en camelcase</td><td></td><td></td>
    </tr>
    <tr>
        <td>tag</td><td>string</td><td>Tag de l'équipe<br/>en uppercase entre 2 & 4 charactères</td><td></td><td></td>
    </tr>
    <tr>
        <td>game</td><td>number</td><td>L'id du jeu de l'équipe dans la bdd</td><td></td><td></td>
    </tr>
    <tr>
        <td>colors</td><td><a href="Types.md#colors">colorsTemplate</a>[ ]</td><td>La liste des couleurs représantant l'équipe</td><td>true</td><td>[ ]</td>
    </tr>
    <tr>
        <td>description</td><td>string</td><td>Description de l'équipe en markdown</td><td>true</td><td></td>
    </tr>
</table>
    </tab>
    <tab title="Json Full" group-key="jsonfull">
<code-block xml:lang="json" xml:space="preserve">
{
    "name": "",
    "tag": "",
    "game": 0,
    "colors": [
        256,
        "#fff",
        "#fff0",
        "#ffffff",
        "#ffffff00"
    ],
    "description": ""
}
</code-block>
    </tab>
    <tab title="Json Min" group-key="jsonmin">
<code-block xml:lang="json" xml:space="preserve">
{
    "name": "",
    "tag": "",
    "game": 0,
    "colors": [
        256,
        "#fff",
        "#fff0",
        "#ffffff",
        "#ffffff00"
    ],
    "description": ""
}
</code-block>
    </tab>
</tabs>
</chapter>