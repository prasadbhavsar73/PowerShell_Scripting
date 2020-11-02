#Software Installed.

$Servers = Get-Content C:\Servers\Servers.txt

$results= foreach($server in $Servers) {

Write-Host "Processing Server: $server"

Get-WmiObject -Class win32_Product -ComputerName $server | select Name, Version, vendor -ErrorAction SilentlyContinue

}

$results | Export-Csv -Path C:\Servers\Softwares_172.16.140.51.csv
