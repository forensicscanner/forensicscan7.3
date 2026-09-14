# forensicscan7.3
forensic scan
# FastForensic 7.4

**FastForensic 7.4** is a lightweight PowerShell forensic scanner designed primarily for detecting and investigating potential Roblox cheat-related activity on Windows.

It is a legitimate defensive and forensic tool. It does **not** contain Roblox cheating functionality, an executor, injector, exploit, or gameplay modification.

## What it scans

FastForensic 7.4 checks:

* Windows Registry persistence locations
* Startup folders
* Running processes
* Roblox-loaded modules
* Scheduled Tasks
* Windows Services
* Prefetch
* DNS cache
* Windows Defender history
* RunMRU
* Suspicious files in targeted locations
* SHA256 hashes
* Digital signatures
* PE metadata
* Suspicious PowerShell and script indicators
* Suspicious file locations
* File changes using a local baseline

## How it works

The scanner collects forensic information from Windows and analyzes multiple indicators instead of relying on a single filename, process name, or keyword.

Suspicious indicators are combined into a scoring system to help identify files, processes, or other activity that may require further investigation.

FastForensic 7.4 can compare files with a previously created local baseline. When a file has not changed, information from the baseline can be reused to make subsequent scans faster.

## Performance

FastForensic 7.4 is designed to perform a **quick, targeted forensic scan** rather than a complete long-term forensic investigation.

It uses a cooperative scan deadline of approximately **4 minutes**. The file scan focuses on locations that are more relevant to Roblox-related investigations instead of recursively scanning the entire user profile and all of `ProgramData`.

If the scan cannot finish within the time limit, FastForensic reports that the scan was incomplete and does not replace the existing baseline with incomplete data.

## Roblox-focused

FastForensic 7.4 was created specifically with **Roblox-related cheat detection and forensic investigation** in mind.

Because its detection logic is focused on Roblox and Windows artifacts, it may not work correctly or provide meaningful results for other games.

It should **not** be considered a universal anti-cheat system.

## Legitimate use

FastForensic 7.4 is intended for:

* Defensive security checks
* Forensic analysis
* Investigating suspicious software
* Roblox security research
* System integrity checks
* Reviewing suspicious processes and files

Detection results are indicators that may require further investigation. A detection does **not** automatically prove that cheating or malicious activity occurred.

## Security warning

Only run PowerShell scripts from a **trusted and verified source**.

Someone can create another `.ps1` file with the same or a similar name and falsely claim that it is FastForensic or that it was created by the project author.

Do not run scripts claiming to be an update, patch, fix, modified version, or official copy unless you have verified their source.

Always check the repository and source code before executing a PowerShell script.

A filename alone does **not** prove that a script is genuine.

## Disclaimer

FastForensic 7.4 is provided for legitimate defensive and forensic purposes.

No forensic scanner can guarantee detection of every cheat or prove with absolute certainty that a particular system was used for cheating.

Results should be interpreted together with other available evidence.
