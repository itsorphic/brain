___


## Failed Login Attempts
[4625 - Failed logon attempt on a Windows system](https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/event.aspx?eventid=4625)

**Disabled Accounts**
```KQL
event.code:4625 AND winlog.event_data.SubStatus:0xC0000072
```

```KQL
event.code:4625 AND winlog.event_data.SubStatus:0xC0000072 AND @timestamp >= "2023-03-03T00:00:00.000Z" AND @timestamp <= "2023-03-06T23:59:59.999Z"
```

**Admin**
```KQL
event.code:4625 AND user.name:admin*
```



## Successful RDP Logon Related to Service Accounts
[4624 - An account was successfully logged on](https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/event.aspx?eventid=4624)

```KQL
event.code:4624 AND winlog.logon.type:RemoteInteractive
```



## Users Added/Removed From A Local Group (Timeframe)
[4732 - A member was added to a security-enabled local group](https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/event.aspx?eventid=4732)
[4733 - A member was removed from a security-enabled local group](https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/event.aspx?eventid=4733)

```KQL
event.code: is one of 4732, 4733 AND group.name: administrators
```


