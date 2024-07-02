## Signup `POST` `/signup`
Command à executer pour créer un compte

<chapter title="CAN USE COMMAND">
<p>
    Everyone
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
        <td>profil_picture</td><td><a href="Types.md#image">Image</a></td><td>Photo de profil l'utilisateur</td><td>true</td><td>Une des images par défaut pour les users</td>
    </tr>
    <tr>
        <td>pseudo</td><td>string</td><td>Pseudo de l'utilisateur<br/>Unique en bdd</td><td></td><td></td>
    </tr>
    <tr>
        <td>last_name</td><td>string</td><td>Nom de famille de l'utilisateur<br/>Transfomer en uppercase automatiquement</td><td></td><td></td>
    </tr>
    <tr>
        <td>first_name</td><td>string</td><td>Prénom de l'utilisateur<br/>Transfomer en camelcase automatiquement</td><td></td><td></td>
    </tr>
    <tr>
        <td>description</td><td>string</td><td>Description publique de l'utilisateur<br/>Markdown possible</td><td>true</td><td></td>
    </tr>
    <tr>
        <td>birth</td><td>string | number</td><td>Date de naissance de l'utilisateur<br/>Si number, timestamp. Si string, voir format lissible par la class Date()</td><td></td><td></td>
    </tr>
    <tr>
        <td>email</td><td>string</td><td>Email de l'utilisateur<br/>Unique en bdd, et format de mail nécessaire</td><td></td><td></td>
    </tr>
    <tr>
        <td>phone_region</td><td>number</td><td>Region de téléphone de l'utilisateur<br/>Si définis, nécessite phone</td><td>true</td><td></td>
    </tr>
    <tr>
        <td>phone</td><td>number</td><td>Numéro de téléphone de l'utilisateur<br/>Si définis, nécessite phone_region</td><td>true</td><td></td>
    </tr>
    <tr>
        <td>password</td><td>number</td><td>Mot de passe de l'utilisateur<br/>Sera hasher, nécessite au moins 1 majuscule, 1 minuscule, 1 chiffre, 1 charactère spécial, et une longueur minimum de 8 charactères</td><td></td><td></td>
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
    "birth": 0,
    "email": "",
    "phone_region": 0,
    "phone": 0,
    "password": ""
}
</code-block>
    </tab>
    <tab title="Json Min" group-key="jsonmin">
<code-block xml:lang="json" xml:space="preserve">
{
    "pseudo": "",
    "last_name": "",
    "first_name": "",
    "birth": 0,
    "email": "",
    "password": ""
}
</code-block>
    </tab>
</tabs>
</chapter>

<chapter title="RETURN">
<tabs group="Lang">
    <tab title="Tableau" group-key="tab">
<table>
    <tr>
        <td>Name</td><td>Type</td><td>Description</td><td>Facultative</td>
    </tr>
    <tr>
        <td>all</td><td>string</td><td>'Another account already exist'</td><td>true</td>
    </tr>
    <tr>
        <td>pseudo</td><td>string</td><td>'Pseudo already used'</td><td>true</td>
    </tr>
    <tr>
        <td>last_name</td><td>string</td><td>'Last name too short'</td><td>true</td>
    </tr>
    <tr>
        <td>first_name</td><td>string</td><td>'First name too short'</td><td>true</td>
    </tr>
    <tr>
        <td>birth</td><td>string</td><td>'Invalid date'<br/>'Your age is too little'<br/>'Your age is too high'</td><td>true</td>
    </tr>
    <tr>
        <td>email</td><td>string</td><td>'Invalid email'<br/>'Email already used'</td><td>true</td>
    </tr>
    <tr>
        <td>phone</td><td>string</td><td>'Invalid phone number'<br/>'Phone number already used'</td><td>true</td>
    </tr>
    <tr>
        <td>password</td><td>string</td><td>'Password need 1 minuscule letter, 1 majuscule letter, 1 number and 1 special character'<br/>'Password too short (8 chars minimum)'</td><td>true</td>
    </tr>
</table>
    </tab>
    <tab title="Json Full" group-key="jsonfull">
<code-block xml:lang="json" xml:space="preserve">
{
    "all": "",
    "pseudo": "",
    "last_name": "",
    "first_name": "",
    "birth": 0,
    "email": "",
    "phone": 0,
    "password": ""
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