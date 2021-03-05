---
layout: OSCPs
title: /OSCP/scan-script
permalink: /OSCP/scan-script
---

<!--<h1>What is scan_script?</h1>-->

<p><br>I used bash instead of python because I wanted to practice bash scripting. To implement asynchronicity I used the <i>wait</i> command. I am quite happy with the result as the script is very efficient at running in parallel what can be.</p>

<p><img src="/OSCP/execution-example.png" alt="execution example" width="800" height="auto"></p>

<p>I wrote it in bash instead of python because I wanted to practice bash scripting. To implement commands asynchronicity I used the bash <i>wait</i> command (would have used async functions in python).</p>

<p>I spent quite alot of time designing the enumeration process in a way that commands are run as soon as they can be (some require previous results to be launched, for example the existence of a web service on a particular port to start bruteforcing its directories) and what commands can be run in parallel.</p>

<p><img src="/OSCP/scan-script-flow.png" alt="script flow" width="800" height="auto"></p>

<p>Source code and instructions on how to use it <a href="https://github.com/Plotkine/scan_script" target="_blank" rel="noopener noreferrer">here</a>.</p>
