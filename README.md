# Configuring YARA Rules

## Objective

This Endpoint Detection and Response Lab project aimed to configure YARA rules within a virtual simulation in a Windows environment. The primary focus included analyzing a file content, creting a YARA rule, and using it to detect a malicious file.

### Skills Learned

- Advanced understanding of YARA rules.
- Proficiency in analyzing and interpreting a malicious file.
- Ability to conduct malware analysis.
- Distinguish betweeen benign and potentially malicious cybersecurity attacks and intrusions.

### Tools Used

- YARA rule configuration.
- ClamAV


## Steps

*Ref 1= Installing ClamAV*
<img width="1271" alt="Screenshot 2025-03-16 at 8 29 08 PM" src="https://github.com/user-attachments/assets/920c3e2c-220f-497f-9c6d-0389ad1fc283" />

Installed ClamAV in Ubuntu Linux via a Windows environment in order to detect if there is a malicious file on the virtual device.


*Ref 2= Clamscan*
<img width="1273" alt="Screenshot 2025-03-16 at 8 44 44 PM" src="https://github.com/user-attachments/assets/31f60814-46e6-4bcd-8920-415940e77655" />

Upon conducting a clamscan of the file, it was detected there is no malicous file due to no YARA rule being in place.


*Ref 3= Creating a String*
<img width="1265" alt="Screenshot 2025-03-16 at 8 46 20 PM" src="https://github.com/user-attachments/assets/560ae620-f195-48f3-a708-a99ceb4bf34d" />

A string command was created due to the strings' ability to extract all strings written in plain-text from a file. This string command enabled the ability to create signatures of the suspicious file stored in the signature database that will be used to then create the YARA rule.


*Ref 4= Creating YARA Rule*
<img width="1272" alt="Screenshot 2025-03-16 at 8 47 15 PM" src="https://github.com/user-attachments/assets/015e27d7-696b-477d-9219-daa8c76a34ff" />

In the step above, the nano command was used to edit a file in the specified path. In order to create the YARA rule, the type of rule had to be identified. In order to successfully create the rule. the string had to be identified as "$text_string = http" and the condition section refers to previously defined strings using the "$text_string" variable. 


*Ref 5= Rescanning Malicious File*

<img width="1272" alt="Screenshot 2025-03-16 at 8 49 15 PM" src="https://github.com/user-attachments/assets/80073ec7-bf96-4d6f-b0c3-50549b21bea2" />

The command clamscan was utilized to rescan the previous file flagged with the newly made Yara file. The scan showed that the file was infected and the rule was added to the Yara database to detect the file as malicious. 


