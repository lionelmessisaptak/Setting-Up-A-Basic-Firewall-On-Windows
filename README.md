# Task 4: Setup and Use a Firewall on Windows/Linux

## Objective
Configure and test basic firewall rules to allow or block traffic.

## Tools Used
- Windows Firewall  
  (Alternatively, UFW on Linux can be used)

## Deliverables
- Screenshot(s) and configuration steps documenting the applied firewall rules

## Steps Performed (Windows)

1. Opened Windows Defender Firewall with Advanced Security.
2. Navigated to Inbound Rules > New Rule...
3. Selected "Port" as the rule type and specified TCP port 23 (Telnet).
4. Chose "Block the connection" as the action.
5. Applied the rule to Domain, Private, and Public profiles.
6. Named the rule: `Block Telnet Port Incoming Traffic`.
7. Saved and applied the rule.
8. Verified the rule appears and is enabled in the firewall list.
9. Attempted a Telnet connection on port 23, which was successfully blocked.
10. Captured screenshots of the configuration and the blocked connection.

## Observations

- **Before applying the rule**: Port 23 (Telnet) was open and accepting incoming connections.
- **After applying the rule**: Port 23 was blocked — any incoming Telnet connection was denied.
- This confirms that the firewall effectively filtered traffic based on the rule.

## Files Included

- `Setting_Up_A_Firewall_Filter_On_Windows.pdf`: Contains complete documentation of the task including:
  - Firewall configuration steps
  - Telnet port test results
  - Final rule status
- `/screenshots/`: Contains individual screenshots of:
  - Port scan showing Telnet open
  - Each firewall setup step
  - Result after applying the filter

## Summary

The Windows Firewall was used to block Telnet traffic on TCP port 23. This task demonstrated basic rule creation, application, and testing. After applying the rule, Telnet connections were blocked as expected, showcasing how firewalls can be used to filter unwanted or insecure traffic.

For Linux users, similar steps can be done using:
```bash
sudo ufw deny 23
telnet localhost 23

---

Let me know if you'd like this saved as a `.md` file or want to include Linux commands/screenshots too!
```
