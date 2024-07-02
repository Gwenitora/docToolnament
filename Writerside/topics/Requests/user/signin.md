## Signin `POST` `/connect`
Command à executer pour récupérer un token de connection

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
        <td>emailOrPseudo</td><td>string</td><td>Vous pouvez choisir de vous connecter avec un mail, ou un pseudo</td><td></td><td></td>
    </tr>
    <tr>
        <td>password</td><td>string</td><td>Votre mot de passe, il sera comparer à la version hasher</td><td></td><td></td>
    </tr>
    <tr>
        <td>a2f</td><td>string</td><td>Si activer sur le compte, l'authentification à double facteur</td><td>true</td><td></td>
    </tr>
</table>
    </tab>
    <tab title="Json Full" group-key="jsonfull">
<code-block xml:lang="json" xml:space="preserve">
{
    "emailOrPseudo": "",
    "password": "",
    "a2f": ""
}
</code-block>
    </tab>
    <tab title="Json Min" group-key="jsonmin">
<code-block xml:lang="json" xml:space="preserve">
{
    "emailOrPseudo": "",
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
        <td>needA2f</td><td>boolean</td><td>Si l'a2f est nécessaire ou éroner, return true</td><td></td>
    </tr>
    <tr>
        <td>token</td><td>string</td><td>Token de connection<br/>Obligatoire si needA2f === false, sinon, n'apparaîtera pas</td><td>true</td>
    </tr>
</table>
    </tab>
    <tab title="Json Full" group-key="jsonfull">
<code-block xml:lang="json" xml:space="preserve">
{
    "needA2f": false,
    "token": ""
}
</code-block>
    </tab>
    <tab title="Json Min" group-key="jsonmin">
<code-block xml:lang="json" xml:space="preserve">
{
    "needA2f": true
}
</code-block>
    </tab>
</tabs>
</chapter>