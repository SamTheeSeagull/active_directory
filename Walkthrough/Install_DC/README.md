# Installing the Domain Controller

1. Used `SConfig` to:
    - Change the hostname
    - Change the IP address to a static address
    - Change the DNS server to our own IP address

2. Install the Active Directory Windows Feature

```shell
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
```

3. Entered commands as follows:

```Import-Module ADDSDeployment```

```Install-ADDSForest```

- Set the DomainName to the name of the desired domain.

- Set ```SafeModeAdministratorPassword``` to the same as our server login password.

4. Setting DNS Client Server Address

Checked for your current DNS Client Server Address with:

```
Get-DNSClientServerAddress
```

By default, it's set to our loopback address: ```127.0.0.1```

We changed this to match our server's IP address:

```
Get-DNSClientServerAddress -InterfaceIndex [Interface Index Listed from the Get command earlier] -ServerAddresses [Server IP Address]
```




