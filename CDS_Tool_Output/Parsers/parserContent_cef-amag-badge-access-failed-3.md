#### Parser Content
```Java
{
Name = cef-amag-badge-access-failed-3
  Product = AMAG
    Conditions = [ """badge '""", """', u'Wrong Hand Template', u'""" ]
  }

 {
   Name = cef-ccure-badge-access
   Vendor = CCURE
   Product = CCURE
   Lms = ArcSight
   DataType = "physical-access"
   TimeFormat = "epoch"
   Conditions = ["""CEF:""", """|CCURE|ACS|""", """flexNumber1="""]
   Fields = [
     """\sdvc=({host}[^\s]+)""",
     """\sdvchost=({host}[^\s]+)""",
     """(?:([^\|]*\|)){5}({outcome}[^\|]+)"""
     """\srt=({time}\d+)""",
     """\ssuser=(?:N\/A|({user}.+?))\s(\w+=|$)""",
     """\scs1=({first_name}.+?)\s(\w+=|$)""",
     """\scs2=({last_name}.+?)\s(\w+=|$)""",
     """\sflexNumber1=({badge_id}\d+)""",
     """\scs4=({department}.+?)\s(\w+=|$)""",
     """\scs5=({company}.+?)\s(\w+=|$)""",
     """\smsg=({location_door}.+?)\s(\w+=|$)"""
   ]
 }
```