#### Parser Content
```Java
{
Name = s-crowdstrike-app-login-1
  Conditions = [ """"eventType":""", """"AuthActivityAuditEvent"""", """"OperationName":""", """"userAuthenticate"""" ]
}

${CrowdStrikeParserTemplates.s-crowdstrike-app-login}{
  Name = s-crowdstrike-app-login-2
  Conditions = [ """"eventType":""", """"AuthActivityAuditEvent"""", """"OperationName":""", """"validateEntitlementsHmac"""" ]
}

${CrowdStrikeParserTemplates.s-crowdstrike-app-login}{
  Name = s-crowdstrike-app-login-3
  Conditions = [ """"eventType":""", """"AuthActivityAuditEvent"""", """"OperationName":""", """"saml2Assert"""" ]
}

${CrowdStrikeParserTemplates.s-crowdstrike-app-login}{
  Name = s-crowdstrike-app-login-4
  Conditions = [ """"eventType":""", """"AuthActivityAuditEvent"""", """"OperationName":""", """"selfAcceptEula"""" ]
}

${CrowdStrikeParserTemplates.s-crowdstrike-app-login}{
  Name = s-crowdstrike-app-login-5
  Conditions = [ """"eventType":""", """"RemoteResponseSessionStartEvent"""", """UserName""" ]
  Fields = ${CrowdStrikeParserTemplates.s-crowdstrike-app-login.Fields} [
    """"UserName":\s*"({user_email}[^"@]+@[^"@]+)"""",
    """"UserName":\s*"({user}[^"@]+)"""",
    """"HostnameField":\s*"({host}[^"@]+)"""",
    """destinationServiceName=({app}.+?)\s(\w+=|$)"""
  ]
}
${CrowdStrikeParserTemplates.s-crowdstrike-app-login}{
  Name = s-crowdstrike-app-login-6
  Conditions = [ """"eventType":""", """"AuthActivityAuditEvent"""", """"OperationName":""", """"CreateAPIClient"""" ]
  Fields =  ${CrowdStrikeParserTemplates.s-crowdstrike-app-login.Fields} [
    """"eventCreationTime":({time}\d+)""",
    """exabeam_host=([^=]+@\s*)?({host}\S+)""",
    """"eventCreationTime":\s*({time}\d+)""",
    """"UserId":\s*"({user_email}[^"@]+@[^"@]+)"""",
    """"UserId":\s*"({user}[^"@]+)"""",
    """"UserIp":\s*"({src_ip}[^"]+)""",
    """"ServiceName":\s*"({app}[^"]+)""",
    """"Success":\s*({outcome}[^",]+)""",
    """"OperationName":"({event_name}[^"]+)"""
 ]
}
```