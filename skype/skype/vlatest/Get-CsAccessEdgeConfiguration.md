---
applicable: Lync Server 2010, Lync Server 2013, Skype for Business Server 2015
schema: 2.0.0
---

# Get-CsAccessEdgeConfiguration

## SYNOPSIS
**Below Content Applies To:** Lync Server 2010

Returns information about the configuration settings for computers running the Access Edge service in your organization (also known as Access Edge servers).
Access Edge servers provide a way for users outside your internal network to communicate with users inside your internal network.

**Below Content Applies To:** Lync Server 2013, Skype for Business Server 2015

Returns information about the configuration settings for computers running the Access Edge service in your organization (also known as Access Edge servers).
Access Edge servers provide a way for users outside your internal network to communicate with users inside your internal network.
This cmdlet was introduced in Lync Server 2010.



## SYNTAX

### Identity
```
Get-CsAccessEdgeConfiguration [[-Identity] <XdsIdentity>] [-LocalStore] [<CommonParameters>]
```

### Filter
```
Get-CsAccessEdgeConfiguration [-Filter <String>] [-LocalStore] [<CommonParameters>]
```

## DESCRIPTION
**Below Content Applies To:** Lync Server 2010

Access Edge servers (also known as access proxy servers) provide a way for you to extend the capabilities of Microsoft Lync Server 2010 to people who are not logged on to your internal network.
For example, if you have remote users -- authenticated users who log on to Lync Server 2010 over the Internet rather than through the internal network -- you will need to set up an Access Edge server.
Additionally, Edge Servers are required if you want to establish federation with another organization or if you want to give your users the right to communicate with people who have accounts with a public instant messaging service such as Yahoo!, AOL, or MSN.
Access Edge servers sit on the perimeter network, and are used to make and validate SIP connections between users inside and outside of your internal network.

In Lync Server, the Access Edge servers are managed by using a single, global collection of configuration settings.
The Get-CsAccessEdgeConfiguration cmdlet enables you to return information about these global settings.
Note that the property values returned by Get-CsAccessEdgeConfiguration will vary depending on the type of routing you have configured for your Edge Servers.
For details, see the Set-CsAccessEdgeConfiguration Help topic.

Who can run this cmdlet: By default, members of the following groups are authorized to run the Get-CsAccessEdgeConfiguration cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins.
To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:

Get-CsAdminRole | Where-Object  {$_.Cmdlets -match "Get-CsAccessEdgeConfiguration"}

**Below Content Applies To:** Lync Server 2013

Access Edge servers (also known as access proxy servers) provide a way for you to extend the capabilities of Lync Server to people who are not logged on to your internal network.
For example, if you have remote users -- authenticated users who log on to Lync Server over the Internet rather than through the internal network -- you will need to set up an Access Edge server.
Additionally, Edge Servers are required if you want to establish federation with another organization or if you want to give your users the right to communicate with people who have accounts with a public instant messaging service such as Yahoo!, AOL, or MSN.
Access Edge servers sit on the perimeter network, and are used to make and validate SIP connections between users inside and outside of your internal network.

In Lync Server, the Access Edge servers are managed by using a single, global collection of configuration settings.
The Get-CsAccessEdgeConfiguration cmdlet enables you to return information about these global settings.
Note that the property values returned by Get-CsAccessEdgeConfiguration will vary depending on the type of routing you have configured for your Edge Servers.
For details, see the Set-CsAccessEdgeConfiguration Help topic.

Who can run this cmdlet: By default, members of the following groups are authorized to run the Get-CsAccessEdgeConfiguration cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins.
To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:

Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsAccessEdgeConfiguration"}

**Below Content Applies To:** Skype for Business Server 2015

Access Edge servers (also known as access proxy servers) provide a way for you to extend the capabilities of Skype for Business Server 2015 to people who are not logged on to your internal network.
For example, if you have remote users -- authenticated users who log on to Skype for Business Server 2015 over the Internet rather than through the internal network -- you will need to set up an Access Edge server.
Additionally, Edge Servers are required if you want to establish federation with another organization or if you want to give your users the right to communicate with people who have accounts with a public instant messaging service such as Yahoo!, AOL, or MSN.
Access Edge servers sit on the perimeter network, and are used to make and validate SIP connections between users inside and outside of your internal network.

In Skype for Business Server 2015, the Access Edge servers are managed by using a single, global collection of configuration settings.
The Get-CsAccessEdgeConfiguration cmdlet enables you to return information about these global settings.
Note that the property values returned by the Get-CsAccessEdgeConfiguration cmdlet will vary depending on the type of routing you have configured for your Edge Servers.
For details, see the Set-CsAccessEdgeConfiguration Help topic.



## EXAMPLES

### -------------------------- Example 1 ------------------------ (Lync Server 2010)
```
Get-CsAccessEdgeConfiguration
```

Example 1 demonstrates the basic use of Get-CsAccessEdgeConfiguration: calling the cmdlet without any additional parameters returns all the property values for your Access Edge server implementation.
Note that there is no need to include the Identity or Filter parameters; that's because there is only one set of Access Edge server configuration data.

### -------------------------- EXAMPLE 1 -------------------------- (Lync Server 2013)
```

```

Example 1 demonstrates the basic use of Get-CsAccessEdgeConfiguration: calling the cmdlet without any additional parameters returns all the property values for your Access Edge server implementation.
Note that there is no need to include the Identity or Filter parameters; that's because there is only one set of Access Edge server configuration data.

Get-CsAccessEdgeConfiguration

### -------------------------- EXAMPLE 1 -------------------------- (Skype for Business Server 2015)
```

```

Example 1 demonstrates the basic use of the Get-CsAccessEdgeConfiguration cmdlet: calling the cmdlet without any additional parameters returns all the property values for your Access Edge server implementation.
Note that there is no need to include the Identity or Filter parameters; that's because there is only one set of Access Edge server configuration data.

Get-CsAccessEdgeConfiguration

### -------------------------- Example 2 ------------------------ (Lync Server 2010)
```
Get-CsAccessEdgeConfiguration | Select-Object Allow*
```

The preceding command returns just three property values for your Access Edge server configuration: AllowAnonymousUsers; AllowFederatedUsers; and AllowOutsideUsers.
To do this, the command first uses Get-CsAccessEdgeConfiguration to return all the Access Edge server property values.
This information is then piped to the Select-Object cmdlet, which picks out only those properties that start with the string value "Allow".
In turn, those are the only property values displayed on the screen.

### -------------------------- EXAMPLE 2 -------------------------- (Lync Server 2013)
```

```

Example 2 returns just three property values for your Access Edge server configuration: AllowAnonymousUsers; AllowFederatedUsers; and AllowOutsideUsers.
To do this, the command first uses Get-CsAccessEdgeConfiguration to return all the Access Edge server property values.
This information is then piped to the Select-Object cmdlet, which picks out only those properties that start with the string value "Allow".
In turn, those are the only property values displayed on the screen.

Get-CsAccessEdgeConfiguration | Select-Object Allow*

### -------------------------- EXAMPLE 2 -------------------------- (Skype for Business Server 2015)
```

```

Example 2 returns just three property values for your Access Edge server configuration: AllowAnonymousUsers; AllowFederatedUsers; and AllowOutsideUsers.
To do this, the command first uses the Get-CsAccessEdgeConfiguration cmdlet to return all the Access Edge server property values.
This information is then piped to the Select-Object cmdlet, which picks out only those properties that start with the string value "Allow".
In turn, those are the only property values displayed on the screen.

Get-CsAccessEdgeConfiguration | Select-Object Allow*

### -------------------------- Example 3 ------------------------ (Lync Server 2010)
```
(Get-CsAccessEdgeConfiguration).EnablePartnerDiscovery
```

The command shown in Example 3 returns the value of a single Access Edge server configuration property: EnablePartnerDiscovery.
To do this, Get-CsAccessEdgeConfiguration is first called in order to return all the Access Edge server configuration property values.
The call to Get-CsAccessEdgeConfiguration is enclosed in parentheses; this ensures that Windows PowerShell completes this command before doing anything else.
After all the property values have been returned, standard "dot notation" (the object name followed by a period followed by a property name) is used to display the value of a single property: EnablePartnerDiscovery.

### -------------------------- EXAMPLE 3 -------------------------- (Lync Server 2013)
```

```

The command shown in Example 3 returns the value of a single Access Edge server configuration property: EnablePartnerDiscovery.
To do this, Get-CsAccessEdgeConfiguration is first called in order to return all the Access Edge server configuration property values.
The call to Get-CsAccessEdgeConfiguration is enclosed in parentheses; this ensures that Windows PowerShell completes this command before doing anything else.
After all the property values have been returned, standard "dot notation" (the object name followed by a period followed by a property name) is used to display the value of a single property: EnablePartnerDiscovery.

(Get-CsAccessEdgeConfiguration).EnablePartnerDiscovery

### -------------------------- EXAMPLE 3 -------------------------- (Skype for Business Server 2015)
```

```

The command shown in Example 3 returns the value of a single Access Edge server configuration property: EnablePartnerDiscovery.
To do this, the Get-CsAccessEdgeConfiguration cmdlet is first called in order to return all the Access Edge server configuration property values.
The call to the Get-CsAccessEdgeConfiguration cmdlet is enclosed in parentheses; this ensures that Windows PowerShell completes this command before doing anything else.
After all the property values have been returned, standard "dot notation" (the object name followed by a period followed by a property name) is used to display the value of a single property: EnablePartnerDiscovery.

(Get-CsAccessEdgeConfiguration).EnablePartnerDiscovery

## PARAMETERS

### -Identity
**Below Content Applies To:** Lync Server 2010, Lync Server 2013

Unique identifier of the Access Edge configuration settings to be returned.
Because you can only have a single, global instance of these settings, you do not have to include the Identity when calling Get-CsAccessEdgeConfiguration.
However, you can use the following syntax to retrieve the global settings: -Identity global.



**Below Content Applies To:** Skype for Business Server 2015

Unique identifier of the Access Edge configuration settings to be returned.
Because you can only have a single, global instance of these settings, you do not have to include the Identity when calling the Get-CsAccessEdgeConfiguration cmdlet.
However, you can use the following syntax to retrieve the global settings: -Identity global.



```yaml
Type: XdsIdentity
Parameter Sets: Identity
Aliases: 
Applicable: Lync Server 2010, Lync Server 2013, Skype for Business Server 2015

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filter
Enables you to use wildcards when specifying the Access Edge configuration settings to be returned.
Because you can only have a single, global instance of these settings there is little reason to use the Filter parameter.
However, if you prefer, you can use syntax similar to this to retrieve the global settings: -Identity "g*".

```yaml
Type: String
Parameter Sets: Filter
Aliases: 
Applicable: Lync Server 2010, Lync Server 2013, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalStore
Retrieves the Access Edge configuration data from the local replica of the Central Management store rather than from the Central Management store itself.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2010, Lync Server 2013, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

###  
None.
Get-CsAccessEdgeConfiguration does not accept pipelined input.

###  
None.
The Get-CsAccessEdgeConfiguration cmdlet does not accept pipelined input.

## OUTPUTS

###  
Get-CsAccessEdgeConfiguration returns instances of the Microsoft.Rtc.Management.WritableConfig.Settings.Edge.DisplayAccessEdgeSettingsDnsSrvRouting object or the Microsoft.Rtc.Management.WritableConfig.Settings.Edge.DisplayAccessEdgeSettingsDefaultRoute object.

###  
The Get-CsAccessEdgeConfiguration cmdlet returns instances of the Microsoft.Rtc.Management.WritableConfig.Settings.Edge.DisplayAccessEdgeSettingsDnsSrvRouting object or the Microsoft.Rtc.Management.WritableConfig.Settings.Edge.DisplayAccessEdgeSettingsDefaultRoute object.

## NOTES

## RELATED LINKS

[Online Version](http://technet.microsoft.com/EN-US/library/75a8a7e9-728f-4abd-87e9-593713ae39ee(OCS.14).aspx)

[Set-CsAccessEdgeConfiguration]()

[Online Version](http://technet.microsoft.com/EN-US/library/75a8a7e9-728f-4abd-87e9-593713ae39ee(OCS.15).aspx)

[Online Version](http://technet.microsoft.com/EN-US/library/75a8a7e9-728f-4abd-87e9-593713ae39ee(OCS.16).aspx)
