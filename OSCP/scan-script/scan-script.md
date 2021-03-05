---
layout: OSCPs
title: /OSCP/scan-script
permalink: /OSCP/scan-script
---

<p><a href="https://github.com/Plotkine/scan_script" target="_blank" rel="noopener noreferrer">Scan_script</a> is a bash script I made to automate scanning and initial enumeration for the PWK labs and the OSCP exam.

<img src="/OSCP/scan-script/execution-example.png" alt="execution example" width="800" height="auto"></p>

<p>I designed the code so that it:
- runs in parallel commands that can be run in parallel (using background processes)
- runs commands requiring other commands outputs as soon (using <i>wait</i>s) as these outputs are generated

<img src="/OSCP/scan-script/flow.png" alt="script flow" width="800" height="auto"></p>

<p>                     +--------------------+                                   +----------------+<br>
                     | UDP version/script |                                   | TCP vuln scan  |<br>
                     |     open ports     |                                   |   open ports   |<br>
                     +--------------------+                                   +----------------+<br>
                       ^                                                        ^<br>
                       |                                                        |<br>
                       |                                                        |<br>
+--------------+     +--------------------+     +-----------------------+     +----------------+     +--------------------+     +--------------+<br>
| OS detection |     |      UDP scan      |     |         START         |     |                |     | TCP version/script |     | HTTP(S) enum |<br>
|  open ports  | <-- |                    | <-- |                       | --> |                | --> |     open ports     | --> |  open ports  |<br>
+--------------+     +--------------------+     +-----------------------+     |                |     +--------------------+     +--------------+<br>
  ^                    |                          |                           |    TCP SYN     |<br>
  |                    |                          |                           |   all ports    |<br>
  |                    v                          v                           |                |<br>
  |                  +--------------------+     +-----------------------+     |                |     +--------------------+<br>
  |                  |       Netcat       |     |        TCP SYN        |     |                |     |       Netcat       |<br>
  |                  |   open UDP ports   |     |   common web ports    |  +- |                | --> |   open TCP ports   |<br>
  |                  +--------------------+     +-----------------------+  |  +----------------+     +--------------------+<br>
  |                                               |                        |    |<br>
  |                                               |                        |    |<br>
  |                                               v                        |    v<br>
  |                                             +-----------------------+  |  +----------------+<br>
  |                                             |     HTTP(S) enum      |  |  |    Smb enum    |<br>
  |                                             | open common web ports |  |  | open smb ports |<br>
  |                                             +-----------------------+  |  +----------------+<br>
  |                                                                        |<br>
  +------------------------------------------------------------------------+</p>

<!-- <p>Source code and instructions on how to use this script <a href="https://github.com/Plotkine/scan_script" target="_blank" rel="noopener noreferrer">here</a>.</p> -->
