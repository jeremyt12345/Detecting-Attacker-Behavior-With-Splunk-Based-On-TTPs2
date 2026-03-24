# Detecting-Attacker-Behavior-With-Splunk-Based-On-TTPs2
Going over what should be known to then find usual behaviors and processes to create good queries


First we want to go over known TTP'S (tactics,technique and procedures) used by attackers (https://attack.mitre.org)

The second detection approach uses statistical analysis to spot abnormal behavior rather than relying on known attack signatures. Instead of hunting for specific threats, it flags anything that deviates from normal activity — working on the premise that malicious behavior will look different from the baseline. Combined with TTP-driven detection, the two approaches create a complete detection strategy covering both known and unknown threats.


PsExec Credential Exposure — Splunk Investigation
Searched for PsExec activity using Sysmon Event ID 1 (ProcessCreate) filtering on the CommandLine field. PsExec accepts a -p flag that passes passwords as plain text arguments, meaning any lateral movement using explicit credentials gets logged in full in the command line. The password was recovered directly from the log without any decryption or additional tooling.



<img width="1050" height="279" alt="image" src="https://github.com/user-attachments/assets/9570088b-b47a-486f-9093-1ab49c319562" />
