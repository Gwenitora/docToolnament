## Get team `GET` `/teams/:id`
Commande pour récupérer la liste des teams ("all"), ou 1 team spécifique avec son id

<chapter title="CAN USE COMMAND">
<p>
    Everyone
</p>
</chapter>

<chapter title="RETURN AS LIST">
<tabs group="Lang">
    <tab title="Tableau" group-key="tab">
<table>
    <tr>
        <td>Name</td><td>Type</td><td>Description</td><td>Facultative</td>
    </tr>
    <tr>
        <td>id</td><td>number</td><td>Id de l'équipe</td><td></td>
    </tr>
    <tr>
        <td>logo</td><td>string</td><td>Lien du logo de l'équipe</td><td>true</td>
    </tr>
    <tr>
        <td>team_picture</td><td>string</td><td>Lien de la photo de l'équipe</td><td>true</td>
    </tr>
    <tr>
        <td>name</td><td>string</td><td>Nom de l'équipe<br/>en camelcase</td><td></td>
    </tr>
    <tr>
        <td>tag</td><td>string</td><td>Tag de l'équipe<br/>en uppercase entre 2 & 4 charactères</td><td></td>
    </tr>
    <tr>
        <td>game_id</td><td>number</td><td>L'id du jeu de l'équipe dans la bdd</td><td></td>
    </tr>
    <tr>
        <td>colors</td><td><a href="Types.md#colors">colorsTemplate</a>[ ]</td><td>La liste des couleurs représantant l'équipe</td><td></td>
    </tr>
    <tr>
        <td>description</td><td>string</td><td>Description de l'équipe en markdown</td><td></td>
    </tr>
    <tr>
        <td>players</td><td><a href="Types.md#playersinforeduce">PlayersInfoReduce</a>[ ]</td><td>Liste tout les joueurs de l'équipe (avec quelque datas comme si tu avais fait la commande <a href="User.md#get-user-get-users-id"></a>)</td><td></td>
    </tr>
</table>
    </tab>
    <tab title="Json Full" group-key="jsonfull">
<code-block xml:lang="json" xml:space="preserve">
{
    "name": "",
    "logo": "",
    "team_picture": "",
    "tag": "",
    "game": 0,
    "colors": [
        256,
        "#fff",
        "#fff0",
        "#ffffff",
        "#ffffff00"
    ],
    "description": "",
    "players": {
        "id": 0,
        "pseudo": "",
        "profil_picture": "",
        "status": ""
    }
}
</code-block>
    </tab>
    <tab title="Json Min" group-key="jsonmin">
<code-block xml:lang="json" xml:space="preserve">
{
    "name": "",
    "tag": "",
    "game": 0,
    "colors": [],
    "description": "",
    "players": {
        "id": 0,
        "pseudo": "",
        "status": ""
    }
}
</code-block>
    </tab>
</tabs>
</chapter>