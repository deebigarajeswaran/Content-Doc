#### Parser Content
```Java
{
Name = cef-netskope-app-login-2
  DataType = "app-login"
  Conditions = [ """CEF:""", """|Skyformation|""", """Login Successful"""", """destinationServiceName=Netskope""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-failed-app-login
  DataType = "failed-app-login"
  Conditions = [ """CEF:""", """|Skyformation|""", """"activity":"Login Failed"""", """destinationServiceName=Netskope""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-dlp-email-alert-1
  DataType = "dlp-email-alert"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"object_type":"Mail"""", """"activity":"Send"""" ]
  Fields = ${NetskopeParserTemplates.cef-netskope-activity.Fields} [
    """"from_user":"({sender}[^"\s@]+@[^"\s@]+)""",
    """"to_user":"({recipients}({recipient}[^"\s@;,]+@({external_domain}[^"\s@,]+))[^"]*)""",
  ]
  DupFields = [ "object->file_name", "recipient->external_address" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-file-operation-1
  DataType = "file-operations"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Browse"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-file-operation-2
  DataType = "file-operations"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Introspection Scan"""", """"object_type":"File"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-file-operation-3
  DataType = "file-operations"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Create"""", """"object_type":"File"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-file-operation-4
  DataType = "file-operations"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Delete"""", """"object_type":"File"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-file-operation-5
  DataType = "file-operations"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Download"""", """"object_type":"File"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-file-operation-6
  DataType = "file-operations"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Edit"""", """"object_type":"File"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-file-operation-9
  DataType = "file-operations"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Move"""", """"object_type":"File"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-file-operation-11
  DataType = "file-operations"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Preview"""", """"object_type":"File"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-file-operation-12
  DataType = "file-operations"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Share"""", """"object_type":"File"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-file-operation-13
  DataType = "file-operations"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Upload"""", """"object_type":"File"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-file-operation-14
  DataType = "file-operations"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"View"""", """"object_type":"File"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-file-operation-15
  DataType = "file-operations"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"View All"""", """"object_type":"File"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-file-operation-16
  DataType = "file-operations"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"FileAccessedExtended"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-file-operation-17
  DataType = "file-operations"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"FileModifiedExtended"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-file-operation-18
  DataType = "file-operations"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"ListUpdated"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-file-operation-19
  DataType = "file-operations"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"ListColumnCreated"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-file-operation-20
  DataType = "file-operations"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"ListCreated"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-file-operation-21
  DataType = "file-operations"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"ListItemDeleted"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-file-operation-22
  DataType = "file-operations"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"ListItemUpdated"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-file-operation-23
  DataType = "file-operations"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"FileDeleted""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-file-operation-24
  DataType = "file-operations"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"FolderDeleted""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-file-operation-25
  DataType = "file-operations"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"PageViewedExtended"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-1
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Dislike"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-2
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Like"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-3
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Power Ups"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-4
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Follow"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-5
  DataType = "file-operations"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Post"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-6
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Terminate"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-7
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Receive"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-8
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Send"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-9
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Approve"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-10
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Create"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-11
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Delete"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-12
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Download"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-13
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Edit"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-14
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Invite"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-15
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Move"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-16
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Share"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-17
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Upload"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = json-netskope-app-activity-17
  DataType = "app-activity"
  Conditions = [ """"nsdeviceuid": """", """"type": """", """"activity": "Upload"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-18
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"View"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-19
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"View All"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-20
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Mark"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-21
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Rename"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-22
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"SiteColumnCreated"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-23
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Delete application password for user"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-24
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Disable Strong Authentication"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-25
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"SearchQueryPerformed"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-26
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Update StsRefreshTokenValidFrom Timestamp"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-41
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"ALERT_CENTER_GET_SIT_LINK"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-42
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"ALERT_CENTER_LIST_CHANGE"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-43
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"ALERT_CENTER_LIST_FEEDBACK"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-44
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"ALERT_CENTER_LIST_RELATED_ALERTS"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-27
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"ALERT_CENTER_VIEW"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-28
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"ARCHIVE_USER"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-29
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"CHANGE_GMAIL_SETTING"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-30
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"CREATE_ACCESS_LEVEL_V2"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-31
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"CREATE_GMAIL_SETTING"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-32
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"DELETE_ACCESS_LEVEL_V2"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-33
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"DELETE_GMAIL_SETTING"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-34
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"DRIVE_DATA_RESTORE"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-35
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"EMAIL_LOG_SEARCH"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-36
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"GROUP_MEMBERS_DOWNLOAD"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-37
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"Request Data Transfer"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-38
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"SECURITY_INVESTIGATION_QUERY"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-39
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"UPDATE_ACCESS_LEVEL_V2"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-40
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"UPDATE_GROUP_MEMBER"""" ]
  DupFields = [ "activity->accesses", "object->file_name" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-45
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"PutObject"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-46
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"CopyObject"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-47
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"CreateMultipartUpload"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-48
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"UploadPart"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-49
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"DeleteObject"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-50
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":"CompleteMultipartUpload"""" ]
}

${NetskopeParserTemplates.cef-netskope-activity}{
  Name = cef-netskope-app-activity-51
  DataType = "app-activity"
  Conditions = [ """CEF:""", """|Skyformation|""", """"type":"""", """destinationServiceName=Netskope""", """"activity":""""]
}

{
  Name = cef-netskope-alert-anomaly
  Vendor = Netskope
  Product = Netskope Active Platform
  Lms = Direct
  DataType = "alert"
  TimeFormat = "epoch_sec"
  Conditions = [ """CEF:""", """|Skyformation|""", """"alert_type":"anomaly"""", """destinationServiceName=Netskope""", """|security-threat-detected|""" ]
 Fields = [
    """({host}[\w\-.]+)\s+Skyformation""",
    """"timestamp":({time}\d+)""",
    """"user":"(({user_email}[^@"\s]+@[^@"\s]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[^"@\\\/\s]+))"""",
    """"app":"({process}[^"]+)""",
    """"dstip":"({dest_ip}[A-Fa-f:\d.]+)""",
    """"srcip":"({src_ip}[A-Fa-f:\d.]+)""",
    """"_id":"({alert_id}[^"]+)""",
    """"category":"({threat_category}[^"]+)""",
    """"alert_name":"({alert_name}[^"]+)""",
    """"alert_type":"({alert_type}[^"]+)""",
    """"url":"({malware_url}[^"]+)""",
    """"risk_level":"({alert_severity}[^"]+)""",
    """"hostname":"({src_host}[^"]+)""",
  ]
  DupFields = ["process->process_name"]
}
```