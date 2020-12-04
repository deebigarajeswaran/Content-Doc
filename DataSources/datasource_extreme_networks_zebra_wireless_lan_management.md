Vendor: Extreme Networks
========================
Product: Zebra wireless LAN management
--------------------------------------
|                                 Use-Case                                  | Activity Types                                                                                                                                             | Event Types/Parsers                                                                               | MITRE TTP                                                                                                                                                                                                                                                                                                                    | Content                    |
|:-------------------------------------------------------------------------:| ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------- |
| [Compromised Credentials](../UseCases/usecase_compromised_credentials.md) | - Asset Logon and Access<br>- Failed Logon and Account Lockout<br>- Pass The Hash and Golden Ticket<br>- Security Operations<br>- Service Account Activity |  failed-logon<br> -- [zebra-wlm-ssh-failed](../Parsers/parserContent_zebra-wlm-ssh-failed.md)<br> | T1021.001 - Remote Services: Remote Desktop Protocol<br>T1078 - Valid Accounts<br>T1110 - Brute Force<br>T1550.002 - Use Alternate Authentication Material: Pass the Hash<br>T1550.003 - Use Alternate Authentication Material: Pass the Ticket<br>T1550.004 - Use Alternate Authentication Material: Web Session Cookie<br> |  - 17 Rules<br> - 3 Models |
|        [Lateral Movement](../UseCases/usecase_lateral_movement.md)        | - Asset Logon and Access<br>- Security Operations                                                                                                          |  failed-logon<br> -- [zebra-wlm-ssh-failed](../Parsers/parserContent_zebra-wlm-ssh-failed.md)<br> | T1110 - Brute Force<br>T1550.003 - Use Alternate Authentication Material: Pass the Ticket<br>T1550.004 - Use Alternate Authentication Material: Web Session Cookie<br>                                                                                                                                                       |  - 2 Rules<br>             |
|       [Malware Detection](../UseCases/usecase_malware_detection.md)       | - Asset Logon and Access                                                                                                                                   |  failed-logon<br> -- [zebra-wlm-ssh-failed](../Parsers/parserContent_zebra-wlm-ssh-failed.md)<br> | T1078 - Valid Accounts<br>T1090.003 - Proxy: Multi-hop Proxy<br>                                                                                                                                                                                                                                                             |  - 3 Rules<br>             |
|     [Privileged Activity](../UseCases/usecase_privileged_activity.md)     | - Executives                                                                                                                                               |  failed-logon<br> -- [zebra-wlm-ssh-failed](../Parsers/parserContent_zebra-wlm-ssh-failed.md)<br> | T1068 - Exploitation for Privilege Escalation<br>                                                                                                                                                                                                                                                                            |  - 1 Rules<br>             |
|    [Ransomware Detection](../UseCases/usecase_ransomware_detection.md)    | - Asset Logon and Access                                                                                                                                   |  failed-logon<br> -- [zebra-wlm-ssh-failed](../Parsers/parserContent_zebra-wlm-ssh-failed.md)<br> | T1078 - Valid Accounts<br>T1090.003 - Proxy: Multi-hop Proxy<br>                                                                                                                                                                                                                                                             |  - 3 Rules<br>             |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                      | Execution | Persistence                                                         | Privilage escalation                                                                                                                                          | Defense evasion                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Credential Access                                                | Discovery | Lateral Movement                                                                                                                                                                                                                                                | Collection | Command and Control                                                                                                                       | Exfiltration | Impact |
| ------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------- | --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploitation for Privilege Escalation](https://attack.mitre.org/techniques/T1068)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Use Alternate Authentication Material](https://attack.mitre.org/techniques/T1550)<br><br>[Use Alternate Authentication Material: Pass the Hash](https://attack.mitre.org/techniques/T1550/002)<br><br>[Use Alternate Authentication Material: Web Session Cookie](https://attack.mitre.org/techniques/T1550/004)<br><br>[Use Alternate Authentication Material: Pass the Ticket](https://attack.mitre.org/techniques/T1550/003)<br><br> | [Brute Force](https://attack.mitre.org/techniques/T1110)<br><br> |           | [Remote Services](https://attack.mitre.org/techniques/T1021)<br><br>[Use Alternate Authentication Material](https://attack.mitre.org/techniques/T1550)<br><br>[Remote Services: Remote Desktop Protocol](https://attack.mitre.org/techniques/T1021/001)<br><br> |            | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              |        |