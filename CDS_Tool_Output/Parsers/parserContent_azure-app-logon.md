#### Parser Content
```Java
{
Name = azure-app-logon
  Vendor = Microsoft
  Product = Microsoft Windows
  Lms = Direct
  DataType = "app-logon"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"operationName":"Sign-in activity"""", """"conditionalAccessStatus":"""", """"tokenIssuerType":"""" ]
  Fields = [
    """exabeam_host=([^=@]+@\s*)?({host}\S+)""",
    """"time":"({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """"callerIpAddress":"({src_ip}[A-Fa-f:\d.]+)"""",
    """"identity":"({user_lastname}[^",]+?)\s*,\s*({user_firstname}[^",]+)"""",
    """"userPrincipalName":"({user_email}[^"\s@]+@[^"\s@]+)"""",
    """"browser":"({browser}[^"]+)"""",
    """"operatingSystem":"({os}[^"]+)"""",
    """"conditionalAccessStatus":"({outcome}[^"]+)"""",
    """"tokenIssuerType":"({app}[^"]+)"""",
  ]
}
```