# Working with Date

Getting current datetime in format
```powershell
PS C:\Users\user1> Get-Date -Format "dddd MM/dd/yyyy HH:mm K"
Monday 03/08/2021 09:58 +08:00
```

Setting datetime
```powershell
PS C:\Users\user1> $T = Get-Date
PS C:\Users\user1> Set-Date -Date $T
```
