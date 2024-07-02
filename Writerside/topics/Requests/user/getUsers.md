## Get user `GET` `/users/:id`
Command à executer pour récupérer un token de connection

<chapter title="CAN USE COMMAND">
<p>
    user-only-if_Id=me<br/>(si :id === 'me', alors les droits sont user, sinon les droits sont Everyone)
</p>
</chapter>

<chapter title="LINK VAR">
<tabs group="LangNoJson">
    <tab title="Tableau" group-key="tab">
<table>
    <tr>
        <td>Name</td><td>Type</td><td>Description</td>
    </tr>
    <tr>
        <td>:id</td><td>string | number</td><td>id du user à chercher, 'all' pour tous, et 'me' pour soit même</td>
    </tr>
</table>
    </tab>
</tabs>
</chapter>

<chapter title="RETURN AS LIST (si utilisation du 'me')">
<tabs group="Lang">
    <tab title="Tableau" group-key="tab">
<table>
    <tr>
        <td>Name</td><td>Type</td><td>Description</td><td>Facultative</td>
    </tr>
    <tr>
        <td>id</td><td>number</td><td>l'id du user dans la bdd</td><td></td>
    </tr>
    <tr>
        <td>pseudo</td><td>string</td><td>le pseudo correspondant</td><td></td>
    </tr>
    <tr>
        <td>profil_picture</td><td>string</td><td>lien d'accès à la photo de profil</td><td>true</td>
    </tr>
    <tr>
        <td>description</td><td><a href="Types.md#mdtemplate">mdTemplate</a></td><td>la description de l'utilisateur</td><td></td>
    </tr>
    <tr>
        <td>last_name</td><td>string</td><td>le nom de famille de l'utilisateur</td><td></td>
    </tr>
    <tr>
        <td>first_name</td><td>string</td><td>le prénom de l'utilisateur</td><td></td>
    </tr>
    <tr>
        <td>birth</td><td>string | number</td><td>la date de naissance de l'utilisateur</td><td></td>
    </tr>
    <tr>
        <td>email</td><td>string</td><td>l'email de l'utilisateur</td><td></td>
    </tr>
    <tr>
        <td>phone_region</td><td>number</td><td>la région du numéro de téléphone de l'utilisateur</td><td>true</td>
    </tr>
    <tr>
        <td>phone</td><td>number</td><td>le numéro de téléphone de l'utilisateur</td><td>true</td>
    </tr>
</table>
    </tab>
    <tab title="Json Full" group-key="jsonfull">
<code-block xml:lang="json" xml:space="preserve">
{
    "id": 0,
    "pseudo": "",
    "profil_picture": "",
    "description": {
        "md": "",
        "html": "",
    },
    "last_name": "",
    "first_name": "",
    "birth": 0,
    "email": "",
    "phone_region": 0,
    "phone": 0
}
</code-block>
    </tab>
    <tab title="Json Min" group-key="jsonmin">
<code-block xml:lang="json" xml:space="preserve">
{
    "id": 0,
    "pseudo": "",
    "description": {
        "md": "",
        "html": "",
    },
    "last_name": "",
    "first_name": "",
    "birth": 0,
    "email": ""
}
</code-block>
    </tab>
</tabs>
</chapter>

<chapter title="RETURN AS LIST (si non utilisation du 'me')">
<tabs group="Lang">
    <tab title="Tableau" group-key="tab">
<table>
    <tr>
        <td>Name</td><td>Type</td><td>Description</td><td>Facultative</td>
    </tr>
    <tr>
        <td>id</td><td>number</td><td>l'id du user dans la bdd</td><td></td>
    </tr>
    <tr>
        <td>pseudo</td><td>string</td><td>le pseudo correspondant</td><td></td>
    </tr>
    <tr>
        <td>profil_picture</td><td>string</td><td>lien d'accès à la photo de profil</td><td>true</td>
    </tr>
    <tr>
        <td>description</td><td><a href="Types.md#mdtemplate">mdTemplate</a></td><td>la description de l'utilisateur</td><td></td>
    </tr>
</table>
    </tab>
    <tab title="Json Full" group-key="jsonfull">
<code-block xml:lang="json" xml:space="preserve">
{
    "id": 0,
    "pseudo": "",
    "profil_picture": "",
    "description": {
        "md": "",
        "html": "",
    }
}
</code-block>
    </tab>
    <tab title="Json Min" group-key="jsonmin">
<code-block xml:lang="json" xml:space="preserve">
{
    "id": 0,
    "pseudo": "",
    "description": {
        "md": "",
        "html": "",
    }
}
</code-block>
    </tab>
</tabs>
</chapter>