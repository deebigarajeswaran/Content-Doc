#### Parser Content
```Java
{
Name = cef-digitalguardian-file-operation
  Vendor = Digital Guardian
  Product = Digital Guardian Endpoint Protection
  Lms = ArcSight
  DataType = "file-operations"
  IsHVF = true
  TimeFormat = "epoch"
  Conditions = [ """|Digital Guardian|Digital Guardian|""" ]
  Fields = [
    """\srt=({time}\d+)""",
    """\ssrc=({host}\S+)""",
    """\ssrc=({dest_host}\S+)""",
    """\sshost=(([^\/\\=]+)[\/\\]+)?({host}\S+)""",
    """\sshost=(([^\/\\=]+)[\/\\]+)?({dest_host}\S+)""",
    """\sdst=({host}\S+)""",
    """\sdhost=(([^\/\\=]+)[\/\\]+)?({host}\S+)""",
    """\sdvc=({host}\S+)""",
    """\sdvc=({dest_host}\S+)""",
    """\sdvchost=(([^\/\\=]+)[\/\\]+)?({host}\S+)""",
    """\sdvchost=(([^\/\\=]+)[\/\\]+)?({dest_host}\S+)""",
    """\ssrc=({src_ip}\S+)""",
    """\sshost=(([^\/\\=]+)[\/\\]+)?({src_host}\S+)""",
    """\sdst=({dest_host}\S+)""",
    """\sdhost=(([^\/\\=]+)[\/\\]+)?({dest_host}\S+)""",
    """\ssuser=(({domain}[^\/\\=]+)[\/\\]+)?({user}[^=]+?)\s+(ad\.\S+=|\w+=|$)""",
    """\ssproc=({process_name}.+?)\s+(ad\.\S+=|\w+=|$)""",
    """\|Digital Guardian\|(.*?\|){2}({event_code}.+?)\|""",
    """\soldFilePath=(|\?:\\+|({src_file_dir}.+?))\\*\s+(ad\.\S+=|\w+=|$)""",   
    """\sfilePath=(|\?:\\+|({file_parent}.+?))\\*\s+(ad\.\S+=|\w+=|$)""",
    """\soldFileName=(|({src_file_name}.+?))\s+(ad\.\S+=|\w+=|$)""",
    """\sfname=(|({file_name}.+?(\.({file_ext}[^\.]+?))?))\s+(ad\.\S+=|\w+=|$)""",
    """\sfileType=(|({file_ext}.+?))\s+(ad\.\S+=|\w+=|$)""",
    """\|(File Recycle|File Delete)\|.*\soldFilePath=(|({file_parent}.+?))\\*\s+(ad\.\S+=|\w+=|$)""",
    """\|(File Recycle|File Delete)\|.*\soldFileName=(|({file_name}.+?(\.({file_ext}[^\.]+?))?))\s+(ad\.\S+=|\w+=|$)""",
    """\sad\.DG__ProductName=(|({app}.+?))\s+(ad\.\S+=|\w+=|$)""",
    """\sad\.DG__BytesWritten=(0|({bytes}\d+))\s+(ad\.\S+=|\w+=|$)""",
  ]
}
```