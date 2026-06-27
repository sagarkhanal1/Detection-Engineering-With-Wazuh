# Detection Engineering With Wazuh

A blue-team lab focused on creating and validating a custom Wazuh detection rule using Windows endpoint telemetry.

## Project Summary

This project demonstrates a basic detection engineering workflow: identify behaviour of interest, create a Wazuh rule, generate controlled lab activity, confirm the event appears in Sysmon logs, and validate that Wazuh produces an alert.

The goal is to practise how defenders turn endpoint behaviour into useful SIEM detections.

## Skills Demonstrated

- Detection engineering workflow
- Wazuh custom rule creation
- Windows endpoint telemetry review
- Sysmon event validation
- Alert testing and verification
- SIEM investigation notes
- Screenshot-based security documentation

## Detection Workflow

```text
Define behaviour to detect
        ↓
Create Wazuh rule
        ↓
Generate controlled lab event
        ↓
Verify Sysmon logging
        ↓
Check Wazuh alert
        ↓
Document evidence and improvements
```

## Tools Used

| Tool | Purpose |
|---|---|
| Wazuh | SIEM alerting and rule validation |
| Sysmon | Windows endpoint telemetry |
| Windows client | Controlled test endpoint |
| Wazuh dashboard | Alert review and evidence capture |

## Walkthrough

### 1. Create a Wazuh Detection Rule

A custom rule was created to detect selected Windows activity inside the lab environment.

<img width="789" height="613" alt="Wazuh rule creation" src="https://github.com/user-attachments/assets/bc62e027-efe6-46ba-ab97-201dd7c23717" />

### 2. Generate Controlled Activity on the Windows Client

The target behaviour was run on a Windows client in the lab to produce telemetry for validation.

<img width="521" height="443" alt="Windows client activity" src="https://github.com/user-attachments/assets/71eea8b0-9a03-4063-a156-5e4340f6a621" />

### 3. Verify Sysmon Logs

Sysmon logs were reviewed to confirm that the endpoint recorded the activity.

<img width="609" height="545" alt="Sysmon logs" src="https://github.com/user-attachments/assets/85dafd93-a4a0-45b7-946a-4c4c2432c2da" />

### 4. Confirm Wazuh Alert

The Wazuh dashboard was checked to confirm that the custom rule produced an alert.

<img width="1359" height="793" alt="Wazuh alert" src="https://github.com/user-attachments/assets/293b1565-4137-4ddb-8fa1-85b2ca0d5b60" />

### 5. Review Alert Evidence

The resulting alert was reviewed as evidence that the detection logic worked in the lab.

<img width="707" height="389" alt="Alert evidence" src="https://github.com/user-attachments/assets/492842f8-9ed9-4b5b-ab0a-112984e3051d" />

## Key Takeaways

- A useful detection should be tested against real telemetry, not just written as theory.
- Sysmon helps provide detailed Windows process visibility.
- Wazuh custom rules can be used to turn endpoint events into analyst-friendly alerts.
- Documentation should show the full path from event generation to alert validation.

## Future Improvements

- Add the exact rule logic in a dedicated file.
- Add alert fields such as rule ID, process name, event ID, and timestamp.
- Map the detection to MITRE ATT&CK where appropriate.
- Add false-positive considerations and tuning notes.
