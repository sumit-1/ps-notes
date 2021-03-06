# Filesystem

List all files in a directory
```powershell
PS C:\Users\user1\Downloads> dir


    Directory: C:\Users\user1\Downloads


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
-a----         6/3/2021   6:01 AM       45481560 Git-2.30.1-32-bit.exe
-a----         6/3/2021   5:56 AM       57579728 Obsidian.0.9.17-32.exe
-a----         7/3/2020   7:43 AM      284429936 PBIDesktopSetup.exe
```

Show only creation time of files
```powershell
PS C:\Users\user1\Downloads> (dir).CreationTime

Saturday, 6 March 2021 6:00:33 AM
Saturday, 6 March 2021 5:56:03 AM
Saturday, 7 March 2020 7:43:19 AM
```

Find files greater than 10MB with file write time
```powershell
PS C:\Windows> Get-ChildItem System32 | Where-Object {$_.Length -gt 10MB} | Select @{Name="Size (MB)";Expression={$_.Length/1MB}}, Name, {$_.LastWriteTime}

       Size (MB) Name                 $_.LastWriteTime
       --------- ----                 ----------------
  15.05419921875 DDORes.dll           10/7/2015 4:24:38 PM
  17.93505859375 edgehtml.dll         27/8/2015 1:16:03 PM
  10.74072265625 ieframe.dll          27/8/2015 1:09:25 PM
  44.07373046875 imageres.dll         10/7/2015 4:25:06 PM
125.922271728516 MRT.exe              27/8/2015 9:36:06 AM
  18.42919921875 mshtml.dll           27/8/2015 1:23:14 PM
19.8915939331055 shell32.dll          20/8/2015 1:16:27 PM
  12.42138671875 Windows.UI.Xaml.dll  11/8/2015 4:57:51 PM
26.7821731567383 WindowsCodecsRaw.dll 10/7/2015 4:25:56 PM
    12.005859375 wmp.dll              22/7/2015 11:11:49 AM
```

Slightly better displayed column name
```powershell
PS C:\Windows> Get-ChildItem System32 | Where-Object {$_.Length -gt 10MB} | Select @{Name="Size (MB)";Expression={$_.Length/1MB}}, Name, @{Name="Last Write Time";Expression={$_.LastWriteTime}}

       Size (MB) Name                 Last Write Time
       --------- ----                 ---------------
  15.05419921875 DDORes.dll           10/7/2015 4:24:38 PM
  17.93505859375 edgehtml.dll         27/8/2015 1:16:03 PM
  10.74072265625 ieframe.dll          27/8/2015 1:09:25 PM
  44.07373046875 imageres.dll         10/7/2015 4:25:06 PM
125.922271728516 MRT.exe              27/8/2015 9:36:06 AM
  18.42919921875 mshtml.dll           27/8/2015 1:23:14 PM
19.8915939331055 shell32.dll          20/8/2015 1:16:27 PM
  12.42138671875 Windows.UI.Xaml.dll  11/8/2015 4:57:51 PM
26.7821731567383 WindowsCodecsRaw.dll 10/7/2015 4:25:56 PM
    12.005859375 wmp.dll              22/7/2015 11:11:49 AM

```


### Tree Implementation
[[tree]]