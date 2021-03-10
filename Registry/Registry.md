## Registry

Set registry value (adding calc to autorun)
 ```powershell
PS C:\Users\user1> Set-Itemproperty -path 'HKCU:\SOFTWARE\Microsoft\Windows\CurrentVersion\Run' -Name '(Default)' -value 'C:\Windows\System32\calc.exe'
 ```
 
 Create registry key
 ```powershell
 PS C:\Users\user1> New-Item -Path "HKCU:\Software\Classes\ms-settings\shell\open\" -Name command -force 
 ```

Create new parameter
```powershell
PS C:\Users\user1> New-ItemProperty -Path "HKCU:\Software\Classes\ms-settings\shell\open\command" -Name 'DelegateExecute' -Value ''
```
![[Pasted image 20210308125834.png]]
 
Renaming key or parameter
```powershell
PS C:\Users\user1> Rename-ItemProperty -Path "HKCU:\Software\Classes\ms-settings\shell\open\command" -Name "DelegateExecute" -NewName "newDelegateExecute"
```

Deleting registry key (Delete all subkyes until ms-settings)
 ```powershell
PS C:\Users\user1> Remove-Item -Path "HKCU:\Software\Classes\ms-settings\*" -Recurse
```
