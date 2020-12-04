Vendor: Symantec
================
Product: Symantec CloudSOC
--------------------------
|                                 Use-Case                                  | Activity Types                                                                                                                                                                                                            | Event Types/Parsers                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | MITRE TTP                                                                                                                                                                                                                                                                              | Content                    |
|:-------------------------------------------------------------------------:| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------- |
| [Compromised Credentials](../UseCases/usecase_compromised_credentials.md) | - Activity Time  and Type<br>- Application Activity<br>- Asset Logon and Access<br>- Critical System Activity<br>- Email Activity<br>- File Activity<br>- Network zones and Location Access<br>- Service Account Activity |  app-activity<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> app-login<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> dlp-alert<br> -- [symantec-cloud-dlp-alert](../Parsers/parserContent_symantec-cloud-dlp-alert.md)<br><br> failed-app-login<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> file-delete<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> file-download<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> file-upload<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br> | T1078 - Valid Accounts<br>T1083 - File and Directory Discovery<br>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions<br>T1133 - External Remote Services<br>                                                                                                        |  - 45 Rules<br> - 7 Models |
|       [Data Exfiltration](../UseCases/usecase_data_exfiltration.md)       | - Data Loss Prevention<br>- Email Activity<br>- File Activity                                                                                                                                                             |  app-activity<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> app-login<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> dlp-alert<br> -- [symantec-cloud-dlp-alert](../Parsers/parserContent_symantec-cloud-dlp-alert.md)<br><br> failed-app-login<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> file-delete<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> file-download<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> file-upload<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br> | T1020 - Automated Exfiltration<br>T1048 - Exfiltration Over Alternative Protocol<br>T1083 - File and Directory Discovery<br>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions<br>T1114.003 - Email Collection: Email Forwarding Rule<br>T1204 - User Execution<br> |  - 20 Rules<br> - 6 Models |
|          [Internal Fraud](../UseCases/usecase_internal_fraud.md)          | - Application Activity                                                                                                                                                                                                    |  app-activity<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> app-login<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> dlp-alert<br> -- [symantec-cloud-dlp-alert](../Parsers/parserContent_symantec-cloud-dlp-alert.md)<br><br> failed-app-login<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> file-delete<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> file-download<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> file-upload<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br> | T1078 - Valid Accounts<br>                                                                                                                                                                                                                                                             |  - 13 Rules<br> - 1 Models |
|        [Lateral Movement](../UseCases/usecase_lateral_movement.md)        | - Activity Time  and Type<br>- Application Activity<br>- Network zones and Location Access                                                                                                                                |  app-activity<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> app-login<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> dlp-alert<br> -- [symantec-cloud-dlp-alert](../Parsers/parserContent_symantec-cloud-dlp-alert.md)<br><br> failed-app-login<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> file-delete<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> file-download<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> file-upload<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br> | T1078 - Valid Accounts<br>T1133 - External Remote Services<br>                                                                                                                                                                                                                         |  - 7 Rules<br> - 1 Models  |
|       [Malware Detection](../UseCases/usecase_malware_detection.md)       | - Asset Logon and Access<br>- Data Loss Prevention<br>- Endpoint Activity<br>- Process Activity                                                                                                                           |  app-activity<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> app-login<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> dlp-alert<br> -- [symantec-cloud-dlp-alert](../Parsers/parserContent_symantec-cloud-dlp-alert.md)<br><br> failed-app-login<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> file-delete<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> file-download<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> file-upload<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br> | T1078 - Valid Accounts<br>T1090.003 - Proxy: Multi-hop Proxy<br>T1204 - User Execution<br>                                                                                                                                                                                             |  - 11 Rules<br> - 1 Models |
|     [Privileged Activity](../UseCases/usecase_privileged_activity.md)     | - Application Activity<br>- Email Activity<br>- Service Account Activity                                                                                                                                                  |  app-activity<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> app-login<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> dlp-alert<br> -- [symantec-cloud-dlp-alert](../Parsers/parserContent_symantec-cloud-dlp-alert.md)<br><br> failed-app-login<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> file-delete<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> file-download<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> file-upload<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br> | T1078 - Valid Accounts<br>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions<br>                                                                                                                                                                                    |  - 5 Rules<br> - 1 Models  |
|    [Ransomware Detection](../UseCases/usecase_ransomware_detection.md)    | - Asset Logon and Access<br>- Data Loss Prevention<br>- Endpoint Activity<br>- Process Activity                                                                                                                           |  app-activity<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> app-login<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> dlp-alert<br> -- [symantec-cloud-dlp-alert](../Parsers/parserContent_symantec-cloud-dlp-alert.md)<br><br> failed-app-login<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> file-delete<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> file-download<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br><br> file-upload<br> -- [symantec-cloud-activity](../Parsers/parserContent_symantec-cloud-activity.md)<br> | T1078 - Valid Accounts<br>T1090.003 - Proxy: Multi-hop Proxy<br>T1204 - User Execution<br>                                                                                                                                                                                             |  - 11 Rules<br> - 1 Models |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                                                                                                   | Execution                                                           | Persistence                                                                                                                                                                                                                                                                                                                                 | Privilage escalation                                                | Defense evasion                                                     | Credential Access | Discovery                                                                         | Lateral Movement | Collection                                                                                                                                                            | Command and Control                                                                                                                       | Exfiltration                                                                                                                                                           | Impact |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------------------------------------------------------------------------------- | ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
| [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [User Execution](https://attack.mitre.org/techniques/T1204)<br><br> | [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Account Manipulation](https://attack.mitre.org/techniques/T1098)<br><br>[Account Manipulation: Exchange Email Delegate Permissions](https://attack.mitre.org/techniques/T1098/002)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   | [File and Directory Discovery](https://attack.mitre.org/techniques/T1083)<br><br> |                  | [Email Collection](https://attack.mitre.org/techniques/T1114)<br><br>[Email Collection: Email Forwarding Rule](https://attack.mitre.org/techniques/T1114/003)<br><br> | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> | [Exfiltration Over Alternative Protocol](https://attack.mitre.org/techniques/T1048)<br><br>[Automated Exfiltration](https://attack.mitre.org/techniques/T1020)<br><br> |        |