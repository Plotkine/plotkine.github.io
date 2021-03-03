---
layout: page
title: /OSCP/scan-script
permalink: /OSCP/scan-script
---

<h1>LEARNING TIPS FOR OSCP STUDENTS</h1>

<h2>-1) My background before enrolling into PWK</h2>

<p><br>- linux basics, python programming
- rooted a few HTB boxes
- eJPT, eCPPT</p>

<h2>0) About exercises/lab reports</h2>

<p><br><b>I don't recommend doing the exercises and lab reports</b>, especially if you are a minimum familiar with kali linux tools like I was.</p>

<p>Since the 2020 update there are alot of exercises (~90 sets iirc); taking you at least 15 days if you work hard on it (I remember offsec mentioning ~100 hours of work to complete them).</p>

<p>If you do quick maths you'll realize it's easy to be stuck at 65 or 67.5 points in the exam so those 10 points can really make the difference. But in my opinion, time spent doing exercises and lab reports could be better spent in the labs rooting boxes.</p>

<h2>1) Root boxes</h2>

<p><br><b>Root as many boxes as you can in the labs</b>. I rooted around 35-40 boxes, skipping dependent boxes/AD boxes/client-side attacks boxes because those topics were not covered in the exam at the time I passed it.</p>

<p>Don't spend too much time on a single box. If you don't find a foothold, use PWK forum and discord communities like <a href="https://discord.com/invite/mEtEFhp" target="_blank" rel="noopener noreferrer">InfoSecPrep</a> to get hints. I never spent more than 2-3 hours without asking for hints.</p>

<h2>2) Take smart notes</h2>

<p><br>More importantly than rooting boxes: <b>take notes about what you learned rooting each boxes and the mistakes you did</b>. The thing to keep in mind when taking notes about a box is that they should help you overcome the difficulties you encountered doing the box when facing a similar box. If you don't do this you'll fall in the same traps over and over again.</p>

<p>Don't take stupid screenshot notes that you'll never read again. Write searchable notes describing how you rooted each box and the commands you used.</p>

<h2>3) Write your own enumeration script</h2>

<p><br>From day 1 in the labs try to automate the stuff you do everytime you enumerate a box (nmap, dirbuster, smb and ftp recon, etc..) and keep adding stuff to your enumeration script (could be written f.e. in bash or python).</p>

<p>Once you approach the end of your lab time, launch your enumeration script against all the boxes you rooted to check if it's getting the right infos to spot the foothold.</p>

I wrote a post about my own enumeration script <a href="/OSCP/scan_script" target="_blank" rel="noopener noreferrer">here</a>.

<h2>2) Take smart notes</h2>

<h2>3) Write an enumeration methodology</h2>

<p><br>From all your pwned box in PWK labs/HTB & vulnhub lists, write an enumeration methodology and personal tips to not fall in the same traps as the ones you falled into.</p>

<p>This is crucial. You should have a methodical way of enumerating boxes and their services.</p>

<h2>5) TJNull OSCP-like boxes list</h2>

You don't have to do all the boxes from the HTB and vulnhub lists but these boxes are really good training to prepare for the exam. You may come across the same kind of tricks or exploits in the exam.

4) Privilege escalation

I recommend taking those two udemy courses:https://www.udemy.com/course/windows-privilege-escalation/https://www.udemy.com/course/linux-privilege-escalation/

They are truly awesome and help you have a good methodology to enumerate boxes for privilege escalation vectors.

5) Tooling

For enumeration: You can use autorecon by tib3rius: https://github.com/Tib3rius/AutoRecon. I personnally made my own bash enumeration script to add more enumeration commands and to use the commands I prefer but this tool helped me alot in the labs.

For privilege escalation: winPEAS, LinEnum.sh, lse.sh, linpeas, https://gtfobins.github.io/, windows-exploit-suggestor.py,... (follow the two udemy courses and you should be fine)

6) Exam

Take your time. Be methodical and enumerate everything you can, you'll end up finding the way in. As people use to say: "don't leave any stone unturned".

You'll be most probably blocked at some points in the exam. Don't panick and review your methodology: what did you miss? what could you try?

As people already said there are "lots of rabbit holes in the exam", meaning you'll get alot of things to enumerate and that's why you should be as methodical as you can.

During my exam my focus dropped dramatically after ~15 hours in, also due to the fact that I couldn't sleep the night before. I took regular breaks (around 5 minutes every hour, and a longer break to eat).

One thing I wasn't expecting in the exam is that the proctoring software took alot of resources on my computer (streaming 3 screens and a webcam). You should take that into account because when I launched my enumeration script at the beginning of the exam my CPU peaked regularly at 100% because of this proctoring software running in parallel. That didn't lead to freezing or other problems but my computer was clearly pushed.

7) Report

Don't underestimate the time needed to write your report: I took ~7 hours to make it while I thought I would be done in 2-3 hours. You really don't want to write you report in a hurry like I did. My advice would be to sleep some hours after the exam and immediately start writing your report afterwards. I used offensive security templates.

I wish you the best of luck. If I did it, so can you!