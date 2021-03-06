
```powershell
PS C:\Users\user1\Downloads> $a=10
PS C:\Users\user1\Downloads> $b=12
PS C:\Users\user1\Downloads> ($a -gt $b) -and (($a -lt 20) -or ($b -lt 20))
False
PS C:\Users\user1\Downloads> $a -gt $b
False
PS C:\Users\user1\Downloads> $a -lt $b
True
PS C:\Users\user1\Downloads> ($a -lt $b) -and (($a -lt 20) -or ($b -lt 20))
True
```


Supported operators
- and
- or
- xor
- not (!)