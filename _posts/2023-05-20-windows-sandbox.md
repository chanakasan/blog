---
layout: post
title:  "Windows Sandbox as a temporary VM"
date:   2023-05-20 09:00:00 +0530
---
Windows 10 has a built in Sandbox mode that is internally used by the OS (by Windows Defender etc).
We can also use it as a temporary VM.

## Installation
To use it as a VM we must have Windows 10 Pro or Windows 11.
To install run below command in a admin powershell prompt and restart the PC.

```powershell
Enable-WindowsOptionalFeature -FeatureName "Containers-DisposableClientVM" -All -Online
```

## Usage
Search and open windows sandbox from Start menu.
Drag any file, folder or executable to the sandbox window to copy it.
We can install and run apps this way without affecting our main Windows OS.

<img src="{{ "/images/windows-sandbox/21.jpg" | relative_url }}" />
<br/>
<br/>
<img src="{{ "/images/windows-sandbox/22.jpg" | relative_url }}" />


## References
- https://learn.microsoft.com/en-us/windows/security/threat-protection/windows-sandbox/windows-sandbox-overview