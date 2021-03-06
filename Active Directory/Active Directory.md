# Active Directory

Users with name starts with Tim
```powershell
PS C:\Users\Administrator> Get-ADUser -Filter {Name -like 'Tim*'}

DistinguishedName	: CN=Tim,OU=clients,OU=office,DC=stella,dc=local
Enabled				: True
GivenName			: Tim

...
```

