# create-entra-app

script to create M365 Entra Apps.<br>
Needs an "permission.json" like the exmaples and creates an "auth_credentials.json" with ID´s and the ClientSecret.<br>
Also has some features to get the IDs needed.

## Usage

### Create an Entra APP
`.\create-entra-app.ps1 [-PermissionFilePath .\permissions-emailrelay.json] [-CredentialOutputPath .\auth_credentials.json]`

### Get Permission ID´s (config supports name)

Get permission ID(s), if multiple seperated by comma (",")<br>
`.\create-entra-app.ps1 -GetEntraPermissionID "SMTP.SendAsApp,POP.AccessAsApp" -ResourceID 00000002-0000-0ff1-ce00-000000000000`

Get resource ID<br>
`.\create-entra-app.ps1 -GetEntraPermissionID SMTP.SendAsApp -ResourceID 00000002-0000-0ff1-ce00-000000000000`

Get both resource and permission ID(s), if multiple seperated by comma (",")<br>
`.\create-entra-app.ps1 -GetEntraPermissionID "SMTP.SendAsApp,POP.AccessAsApp" -GetEntraResourceID "Office 365 Exchange Online"`
