$rootPath = "C:\Program Files\MongoDB"
$cfgPath = Get-ChildItem -Recurse -Filter "mongod.cfg" -path $rootPath
$ip = Get-NetIPAddress -PrefixOrigin Dhcp -AddressFamily IPv4 | select -ExpandProperty IPAddress
(Get-Content $cfgPath.FullName) -Replace '127.0.0.1', $ip | Set-Content ($cfgPath.FullName + "bak") 
