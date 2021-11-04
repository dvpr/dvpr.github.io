## Ansible

> 远程运维工具

### Windows 客户机配置

### Windows Guides

##### 确认PowerShell(>=3.0)和.Net(>=4.0)版本

##### Ansible requires PowerShell 3.0 or newer and at least .NET 4.0 to be installed on the Windows host.

```powershell
# PowerShell
$psversiontable
```

##### 配置ansible脚本

##### The script for config Ansible

```powershell
# PowerShell
cd c:\
Invoke-WebRequest -Uri https://dvpr.me/assets/windows/ConfigureRemotingForAnsible.ps1 -OutFile ConfigureRemotingForAnsible.ps1
set-ExecutionPolicy RemoteSigned 
# set-ExecutionPolicy -ExecutionPolicy UNRESTRICTED # 可选
.\ConfigureRemotingForAnsible.ps1 -SkipNetworkProfileCheck
rm .\ConfigureRemotingForAnsible.ps1
```

##### 打开5985端口

##### Open port 5985

```powershell
# PowerShell
netsh advfirewall firewall add rule name="Win-RM-HTTP" dir=in localport=5985 protocol=TCP action=allow
```
