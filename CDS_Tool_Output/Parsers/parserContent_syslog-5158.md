#### Parser Content
```Java
{
Name = syslog-5158
  Vendor = Microsoft
  Product = Windows
  Lms = Direct
  DataType = "process-network-bind"
  TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
  Conditions = [ """5158""", """The Windows Filtering Platform has permitted a bind to a local port""" ]
  Fields = [
    """\w+ \d+ \d\d:\d\d:\d\d ({host}[\w\-.]+)""",
    """({time}\w+ \w+ \d\d \d\d:\d\d:\d\d \d\d\d\d)\s+""",
    """({event_code}5158)""",
    """\WComputer\\*=({host}[\w\-.]+)""",
    """Computer(Name)?\s*\\*"?(=|:|>)\s*"*({host}[\w\.-]+)(\s|,|"|</Computer>|$)""",
    """({event_name}The Windows Filtering Platform has permitted a bind to a local port)""",
    """Process ID:\s*({pid}\d+)""",
    """Application Name:\s*({process}({directory}.+)[\\\/]({process_name}.+?))\s*Network Information:""",
    """Source Address:\s*(0\.0\.0\.0|({dest_ip}(?!::)[a-fA-F:\d.]+))?.+?\s*Source Port:\s*({dest_port}\d*)""",
    """Protocol:\s*({ms_protocol_num}\d*)""",
    """Layer Name:\s*({layer_name}.*?)\s*Layer Run-Time ID"""
  ]
  DupFields = [ "host->dest_host" ]
}
```