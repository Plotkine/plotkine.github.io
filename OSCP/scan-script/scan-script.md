---
layout: OSCPs
title: /OSCP/scan-script
permalink: /OSCP/scan-script
---

<p><br><a href="https://github.com/Plotkine/scan_script" target="_blank" rel="noopener noreferrer">Scan_script</a> is a bash script I made to automate scanning and initial enumeration for the PWK labs and the OSCP exam.

<img src="/OSCP/scan-script/execution-example.png" alt="execution example" width="800" height="auto"></p>

<p><br>I designed the code so that it:
- runs in parallel commands that can be run in parallel (using background processes)
- runs commands requiring other commands outputs as soon (using <i>wait</i>s) as these outputs are generated</p>

<img src="/OSCP/scan-script/flow.png" alt="script flow" width="800" height="auto"></p>

<!-- <p>Source code and instructions on how to use this script <a href="https://github.com/Plotkine/scan_script" target="_blank" rel="noopener noreferrer">here</a>.</p> -->
