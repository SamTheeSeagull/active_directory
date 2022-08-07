1. Created a new workstation with our template.

2. Set the DNS address on our new workstation:

```Get-DnsClientServerAddress```

Grab the Interface Index #

```Set-DnsClientServerAddress -Interface [Interface Index#] -ServerAddresses [IP for our Server]```

3a. On the new workstation, search for domain.

  - Add work or school account
  
  - Join this device to a local AD Domain

  - Search for the domain name we made earlier

  - Enter credentials for the domain

3b. Or, you can do it via powershell command line with:

```
Add-Computer -DomainName [Domain's Name] -Credential [domain]\Administrator -Force -Restart
```

Enter the credentials we used for the domain setup earlier and the system restarts.

Now, once you you try to log in, you will have the option to log in as our Admin account, or a new one (Other User) on the domain.
