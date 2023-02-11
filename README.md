<<<<<<< HEAD
# Cfbytes

Small powershell class to convert bytes 

```powershell
# Options
# ------------------
# max round deceimal point
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
=======
# CFBytes Class

A simple class written in PowerShell to convert a byte array to human-readable form.

:floppy_disk: Methods
- `convert`: Converts the number of bytes to the specified unit and rounds the result to one decimal place (default). The method also has the capability of adding a caption to the result.
- `ConvertAuto`: Converts the number of bytes to the most appropriate unit and rounds the result to one decimal place (default) without adding a caption to the result.

:scroll: Variables
- `$round`: Specifies the number of decimal places to round the result.
- `$caption`: Specifies whether to add a caption to the result.
- `$bytes_in_KB`, `$bytes_in_MB`, `$bytes_in_GB`, `$bytes_in_TB`, `$bytes_in_PB`: Represent the number of bytes in each unit.

:pencil: Example

```powershell
# Import CFBytes class
. .\CFBytes.ps1

# Convert 1024 bytes to KB
$result = [CFBytes]::convert(1024, "KB")
Write-Host $result

# Output: 1 KB

# Convert 1000000000 bytes to GB with caption
[CFBytes]::$caption = $true
$result = [CFBytes]::convert(1000000000, "GB")
Write-Host $result

# Output: 1 GB

# Convert 1000000000 bytes to the most appropriate unit
$result = [CFBytes]::ConvertAuto(1000000000)
Write-Host $result

# Output: 0.93 GB
>>>>>>> c411db72a41a06478046b8db581cb35657c8bfe3
