---
layout: OSCPs
title: /OSCP/scan-script
permalink: /OSCP/scan-script
---

<p><br><a href="https://github.com/Plotkine/scan_script" target="_blank" rel="noopener noreferrer">Scan_script</a>. is a bash script I made to automate scanning and initial enumeration for the PWK labs and the OSCP exam.

<img src="/OSCP/scan-script/execution-example.png" alt="execution example" width="800" height="auto"></p>

<p>I wrote it in bash instead of python because I wanted to practice bash scripting.

<p>I designed the code in a way that:
- run in parallel commands that can be (using background processes)
- commands requiring other commands outputs are run as soon as they can be (using <i>wait</i>s)</p>

<p>Here is a graph of the script's flow:

<img src="/OSCP/scan-script/flow.png" alt="script flow" width="1200" height="auto"></p>

<p>Source code and instructions on how to use this script <a href="https://github.com/Plotkine/scan_script" target="_blank" rel="noopener noreferrer">here</a>.</p>
