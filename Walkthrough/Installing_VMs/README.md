# 00 - Install and Set up VMs

1. Downloaded and installed Windows Server 2022, and Windows 11. Windows Server 2022 is used on VMware Workstation 16, and the Windows 11 client is on Oracle VirtualBox.
2. Cloned the fresh installs so that we always have a fresh install to go back to in case we break something.
3. Made test account for Microsoft to gain access to Windows 11 installation.
4. Enabled PSRemoting by doing the following on the Windows 11 Machine:
    - ```Start-Sevice WinRM```
    - ```set-item wsman:\localhost\Client\TrustedHosts -value [address of windows server 2022 machine]```
    - To open a session for our workstation to access the server: ```New-PSSession -ComputerName [Server IP] -Credential (Get-Credential)```
    - Finally, to access the server, ```Enter-PSSession [session id]```
5. We're finally done here, and can move on to setting up Active Directory and the Domain Controller
