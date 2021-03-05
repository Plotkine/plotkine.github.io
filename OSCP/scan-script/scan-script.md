---
layout: OSCPs
title: /OSCP/scan-script
permalink: /OSCP/scan-script
---

<!--<h1>What is scan_script?</h1>-->

<p><br> Scan_script is a bash script I made to automate scanning and initial enumeration for the PWK labs and the OSCP exam.<p>

<p><img src="/OSCP/scan-script/execution-example.png" alt="execution example" width="800" height="auto"></p>

<p>I wrote it in bash instead of python because I wanted to practice bash scripting.

<p>I spent quite alot of time designing the code in a way that:
- commands that can be run in parallel are run in parallel (as background processes)
- commands that require output of other commands are run as soon as they can be (using the <i>wait</i> bash command)</p>

<p>Here is a flow graph of the commands run in the script:</p>

<p><img src="/OSCP/scan-script/flow.png" alt="script flow" width="1200" height="auto"></p>

<p>Source code and instructions on how to use this script <a href="https://github.com/Plotkine/scan_script" target="_blank" rel="noopener noreferrer">here</a>.</p>
