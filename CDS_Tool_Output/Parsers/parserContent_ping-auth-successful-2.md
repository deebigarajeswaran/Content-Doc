#### Parser Content
```Java
{
Name = ping-auth-successful-2
  DataType = "authentication-successful"
  Conditions = [ """|OAuth|""", """success|""" ]
}

${PingParserTemplates.ping-events}{
  Name = ping-auth-failed-2
  DataType = "authentication-failed"
  Conditions = [ """|OAuth|""", """failure|""" ]
  Fields = ${PingParserTemplates.ping-events.Fields} [
    """(\|\s*(AUTHN_ATTEMPT|OAuth|SSO)\s*\|)\s*([^\|]*\|){9}\s*(|({failure_reason}[^\|]*?))\s*\|""",
  ]
}

${PingParserTemplates.ping-events}{
  Name = ping-app-login
  DataType = "app-login"
  Conditions = [ """|SSO|""", """success|""" ]
}

{
  Name=raw-protectwise-alert
  Vendor = ProtectWise
  Product = NDR
  Lms = Direct
  DataType = "alert"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ protectwise-emitter[""" ]
  Fields = [
    """({time}\d{1,4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}.[^\s.]+)""",
    """\d\d:\d\d:\d\d\s({host}[^=]+?).\s<""",
    """src\s-\s({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """dst\s-\s({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """classification:\s({alert_type}[^,]*)""",
    """description:\s({alert_name}[^,]*)""",
  ]
 }
```