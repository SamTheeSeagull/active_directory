# Installing the Domain Controller

1. Used `SConfig` to:
    - Change the hostname
    - Change the IP address to a static address
    - Change the DNS server to our own IP address

2. Install the Active Directory Windows Feature

```shell
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
```

3. Enter commands as follows:

```Import-Module ADDSDeployment
Install-ADDSForest```

