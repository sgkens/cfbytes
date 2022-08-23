# Cfbytes

Small powershell class to convert bytes 

```powershell
# Options
# ------------------
# max round deceimmal point
[cfbytes]::round = 1

# display "KB|MB|GB|TB|PB"
[cfbytes]::caption = $true 

```



```powershell
# Conversion
# ------------------
# Convert with unit tag attached eg: 26 MB
[cfbytes]::convertAuto(170001555344)
# Convert to specified unit
[cfbytes]::convert(170001555344, 'mb')
```