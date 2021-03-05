---
layout: programmings
title: /programming/bash/scan-script
permalink: /programming/bash/scan-script
---

<p><br>Scan_script (<a href="https://github.com/Plotkine/scan_script" target="_blank" rel="noopener noreferrer">source code</a>) is a bash script I made to automate scanning and initial enumeration for the PWK labs and the OSCP exam.

<img src="/OSCP/scan-script/execution-example.png" alt="execution example" width="800" height="auto"></p>

<h1>Design</h1>

<p><br>I designed the code so that it:
- runs in parallel commands that can be run in parallel (using background processes)
- runs commands requiring other commands outputs as soon as they can be run (using <i>wait</i>s)

<!--  <img src="/OSCP/scan-script/flow.png" alt="script flow" width="800" height="auto"></p> -->

                     +--------------------+                                   +----------------+
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
  +------------------------------------------------------------------------+</p>

<p>Graph made with <a href="https://github.com/ironcamel/Graph-Easy" target="_blank" rel="noopener noreferrer">Graph-Easy</a>.</p>

<!-- <p>Source code and instructions on how to use this script <a href="https://github.com/Plotkine/scan_script" target="_blank" rel="noopener noreferrer">here</a>.</p> -->
