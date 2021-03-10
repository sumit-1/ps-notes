## File I/O
Create and Write content into file
```powershell
PS C:\Users\user1> New-Item test_read.txt -ItemType File
PS C:\Users\user1> Set-Content test_read.txt "Hello"
```

Append content into file
```powershell
PS C:\Users\user1> Add-Content test_read.txt "World!"
```

Read text file
```powershell
PS C:\Users\user1> Get-Content test_read.txt
Hello
World!
```
