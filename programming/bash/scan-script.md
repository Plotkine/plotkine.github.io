---
layout: programmings
title: /programming/bash/scan-script
permalink: /programming/bash/scan-script
---

<h1>Introduction</h1>

<p>Scan_script is a bash script I made to automate scanning and initial enumeration for the PWK labs and the OSCP exam. It is a wrapper around different tools like nmap, netcat, enum4linux, smbclient, smbmap, dirsearch, gobuster, nikto. Directories named after the IPs of the targets are created by the script in the current directory, containing the outputs of the scans performed by the script.</p>

<p>Source code <a href="https://github.com/Plotkine/scan_script" target="_blank" rel="noopener noreferrer">here</a>.</p>

<h1>Execution example</h1>

<p><img src="/OSCP/scan-script/execution-example.png" alt="execution example" width="800" height="auto"></p>

<h1>Design</h1>

<p>The code is designed so that:
- partial results are outputted as soon as possible
- commands that can be run in parallel are run in parallel (using background processes)
- commands requiring other commands outputs are run as soon as they can be run (using <i>wait</i>s)</p>

<!--  <img src="/OSCP/scan-script/flow.png" alt="script flow" width="800" height="auto"></p> -->

<p>                     +--------------------+                                   +----------------+
                     | UDP version/script |                                   | TCP vuln scan  |
                     |     open ports     |                                   |   open ports   |
                     +--------------------+                                   +----------------+
                       ^                                                        ^
                       |                                                        |
                       |                                                        |
+--------------+     +--------------------+     +-----------------------+     +----------------+     +--------------------+     +--------------+
| OS detection |     |      UDP scan      |     |         <mark><b>START</b></mark>         |     |                |     | TCP version/script |     | HTTP(S) enum |
|  open ports  | <-- |                    | <-- |                       | --> |                | --> |     open ports     | --> |  open ports  |
+--------------+     +--------------------+     +-----------------------+     |                |     +--------------------+     +--------------+
  ^                    |                          |                           |    TCP SYN     |
  |                    |                          |                           |   all ports    |
  |                    v                          v                           |                |
  |                  +--------------------+     +-----------------------+     |                |     +--------------------+
  |                  |       Netcat       |     |        TCP SYN        |     |                |     |       Netcat       |
  |                  |   open UDP ports   |     |   common web ports    |  +- |                | --> |   open TCP ports   |
  |                  +--------------------+     +-----------------------+  |  +----------------+     +--------------------+
  |                                               |                        |    |
  |                                               |                        |    |
  |                                               v                        |    v
  |                                             +-----------------------+  |  +----------------+
  |                                             |     HTTP(S) enum      |  |  |    Smb enum    |
  |                                             | open common web ports |  |  | open smb ports |
  |                                             +-----------------------+  |  +----------------+
  |                                                                        |
  +------------------------------------------------------------------------+<!--</div>--></p>

<p>Graph made with <a href="https://github.com/ironcamel/Graph-Easy" target="_blank" rel="noopener noreferrer">Graph-Easy</a>.</p>

<!-- <p>Source code and instructions on how to use this script <a href="https://github.com/Plotkine/scan_script" target="_blank" rel="noopener noreferrer">here</a>.</p> -->
