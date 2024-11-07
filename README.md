# Privilege Escalation Project

This repository contains files related to the analysis of privilege escalation vulnerabilities in Android applications. Below is a description of each file in this project:

## File Descriptions

### statistics.csv
This file contains statistical data about all analyzed Android apps. It includes the following columns:
- **Time_Androguard**: Time taken by Androguard analysis.
- **No_Of_Permissions**: Number of permissions requested by the app.
- **Time_Permission**: Time spent on permission analysis.
- **No_Of_Intent**: Number of intents used by the app.
- **No_Of_ImplicitIntent**: Number of implicit intents used.
- **No_Of_ExplicitIntent**: Number of explicit intents used.
- **Time_Intent**: Time spent analyzing intents.
- **No_Of_PendingIntent**: Number of Pending Intents used.
- **No_Of_Filter**: Number of intent filters used.
- **Time_Filter**: Time spent analyzing intent filters.
- **No_Of_PermissionIntent**: Number of Permission Intents.
- **Type_Of_PermissionIntent**: Type of Permission Intents.
- **No_Of_PermissionFilter**: Number of Permission Filters.
- **Type_Of_PermissionFilter**: Type of Permission Filters.
- **Danger**: 1 if the app is dangerous, 0 if it s normal.

### BenignApp.pdf
A PDF document containing the names of APKs classified as benign apps (non-malicious).

###  DangerApp.pdf 
A PDF document containing the names of APKs classified as dangerous apps (potentially malicious).

###  Intent.csv 
A CSV file containing a list of intents extracted from 4000 Android apps. This file is used for intent-based analysis in the study of privilege escalation.

###  Intent_filter.rar 
A compressed archive (RAR file) that contains the file ** intent_filter.csv **, which includes all the intent filters extracted from the same 4000 apps. 

###  Intent_Resolution.csv 
This CSV file includes data on the resolution of intents, specifically matching the intents to their corresponding intent filters.

###  Order1_dn.csv 
This CSV file represents **first-order privilege escalation** where a dangerous app (firstApp) is involved with a normal app (secondApp).
###   Order1_nd.csv  
Similar to the previous file, this file represents **first-order privilege escalation**, but with the order reversed: a normal app (firstApp) is interacting with a dangerous app (secondApp).

###   order2_dn(Normal_Privilege_Escalation).csv  
This CSV file represents **second-order normal privilege escalation**, where a dangerous app (firstApp) interacts with a normal app (thirdApp). 

###   order2_dn(Strict_Privilege_Escalation).csv  
This file represents **second-order strict privilege escalation**, where a dangerous app (firstApp) interacts with a normal app (thirdApp).
###   order2_nd(Normal_Privilege_Escalation).csv  
This file represents **second-order normal privilege escalation**, but with a normal app (firstApp) interacting with a dangerous app (thirdApp).

###   order2_nd(Strict_Privilege_Escalation).csv  
Similar to the previous file, this represents **second-order strict privilege escalation**, but the first app is normal (firstApp) and the third app is dangerous (thirdApp).

###   order3_dn(Normal_Privilege_Escalation).csv  
This file tracks **third-order normal privilege escalation**, where a dangerous app (firstApp) interacts with a normal app (fourthApp).

###   order3_nd(Normal_Privilege_Escalation).csv  
Similar to the previous file, this file represents **third-order normal privilege escalation**, but in this case, the first app is normal (firstApp) and the fourth app is dangerous (fourthApp).

###   order4_dn(Normal_Privilege_Escalation).csv  
This file represents **fourth-order normal privilege escalation**, where a dangerous app (firstApp) interacts with a normal app (fifthApp).

###   order4_nd(Normal_Privilege_Escalation).csv  
Similar to the previous file, this file tracks **fourth-order normal privilege escalation**, but in this case, the first app is normal (firstApp) and the fifth app is dangerous (fifthApp).

## Explanation of "Privilege Escalation" Orders

- **Order 1**: Involves direct interactions between two apps (one dangerous and one normal).
- **Order 2**: Involves a chain of three apps, where the first app is dangerous, and the third app is normal, or vice versa, with either normal or strict privilege escalation conditions applied.
- **Order 3 and 4**: These are further extended scenarios where privilege escalation continues across multiple apps (up to four or five apps), increasing the complexity of the privilege escalation chain.

