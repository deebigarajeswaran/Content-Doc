#### Parser Content
```Java
{
Name = s-viscount-badge-access
  Vendor = Viscount
  Product = Viscount
  Lms = Splunk
  DataType = "physical-access"
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """, activitytype="""", """, portname="""", """, devicename="""" ]
  Fields = [
    """exabeam_host=([^=]+?@\s*)?({host}[\w\.-]+)""",
    """logtime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
    """info="(Unknown Card|({user_fullname}[^:]+?))(:|-)\s*({badge_id}\d+)""",
    """devicename="({location_door}[^"]+)""",
    """info=".*?Area:({location_door}[^"]+)""",
    """lastname="(Unknown Card|({last_name}[^"\s]+))""",
    """firstname="({first_name}[^"\s]+)""",
    """cardnumber="({badge_id}\d+)""",
    """result="({outcome}[^"]+)""",
  ]
}
```