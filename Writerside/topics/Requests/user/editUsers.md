## Edit user `POST` `/user/edit`
Command pour editer sont propre profil

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
        <td>profil_picture</td><td><a href="Types.md#image">Image</a></td><td>Photo de profil l'utilisateur</td><td>true</td><td></td>
    </tr>
    <tr>
        <td>pseudo</td><td>string</td><td>Pseudo de l'utilisateur<br/>Unique en bdd</td><td>true</td><td></td>
    </tr>
    <tr>
        <td>last_name</td><td>string</td><td>Nom de famille de l'utilisateur<br/>Transfomer en uppercase automatiquement</td><td>true</td><td></td>
    </tr>
    <tr>
        <td>first_name</td><td>string</td><td>Prénom de l'utilisateur<br/>Transfomer en camelcase automatiquement</td><td>true</td><td></td>
    </tr>
    <tr>
        <td>description</td><td>string</td><td>Description publique de l'utilisateur<br/>Markdown possible</td><td>true</td><td></td>
    </tr>
    <tr>
        <td>email</td><td>string</td><td>Email de l'utilisateur<br/>Unique en bdd, et format de mail nécessaire</td><td>true</td><td></td>
    </tr>
    <tr>
        <td>phone_region</td><td>number</td><td>Region de téléphone de l'utilisateur<br/>Si définis, nécessite phone</td><td>true</td><td></td>
    </tr>
    <tr>
        <td>phone</td><td>number</td><td>Numéro de téléphone de l'utilisateur<br/>Si définis, nécessite phone_region</td><td>true</td><td></td>
    </tr>
</table>
    </tab>
    <tab title="Json Full" group-key="jsonfull">
<code-block xml:lang="json" xml:space="preserve">
{
    "pseudo": "",
    "last_name": "",
    "first_name": "",
    "description": "",
    "email": "",
    "phone_region": 0,
    "phone": 0
}
</code-block>
    </tab>
    <tab title="Json Min" group-key="jsonmin">
<code-block xml:lang="json" xml:space="preserve">
{}
</code-block>
    </tab>
</tabs>
</chapter>