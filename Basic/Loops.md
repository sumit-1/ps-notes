# Loops
For loop
```powershell
PS C:\Users\user1> for($i=0;$i -lt 5;$i++){$i}
0
1
2
3
4
```

For-each loop
```powershell
PS C:\User\user1> $arr = @("var1","var2","var3")
PS C:\Users\user1> foreach ($item in $arr) {$item}
var1
var2
var3
```

While loop
```powershell
PS C:\User\user1> $i=0
PS C:\User\user1> while($i -le 5){$i;$i++}
0
1
2
3
4
5
```

Do while loop
```powershell
PS C:\User\user1> $i=0
PS C:\User\user1> do {$i; $i++}while($i -lt 5)
0
1
2
3
4
```