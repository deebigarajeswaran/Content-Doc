#### Parser Content
```Java
{
Name = rs2-badge-access
  Vendor = RS2 Technologies
  Product = RS2 Technologies
  Lms = Syslog
  DataType = "physical-access"
  TimeFormat = "yyyy-MM-dd HH:mm:ss.S"
  Conditions = [ """CardNumber=""", """SiteName=""", """EventLocation=""" ]
  Fields = [
    """exabeam_host=({host}[\w.\-]+)""",
    """\sEventDate="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d)""",
    """\sSiteName="({location_building}[^"]+)""",
    """\sEventLocation="({location_door}[^"]+)""",
    """\sEventDescription="({outcome}[^"]+)""",
    """\sEID="({user}[^"]+)""",
    """\sCardNumber="({badge_id}[^"]+)""",
    """\sFirstName="\s*({first_name}[^"]+?)\s*"""",
    """\sLastName="\s*({last_name}[^"]+?)\s*"""",
  ]
}
```