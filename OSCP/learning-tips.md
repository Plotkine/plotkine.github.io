---
layout: OSCPs
title: /OSCP/learning-tips
permalink: /OSCP/learning-tips
---

<h1>What this post is about</h1>

<p><br>This post describes learning tips I'd give to PWK students.</p>

<h1>My background before enrolling into PWK</h1>

<p><br>- linux basics, python programming
- rooted a few HTB boxes
- eJPT, eCPPT</p>

<h1>About exercises/lab reports</h1>

<p><br><b>I don't recommend doing the exercises and lab reports</b> if you have some pentesting basics like I did have.</p>

<p>Since the 2020 update there are ~90 sets of exercises; taking you at least 15 days if you work full time on it (Offsec mentions ~100 hours of work to complete them).</p>

<p>If you do quick maths you'll realize it's easy to be stuck at 65 or 67.5 points in the exam so those 10 points can really make the difference. However imo, time spent doing exercises and lab reports are better spent in the labs rooting boxes.</p>

<h1>Root as many boxes as you can</h1>

<p><br>Rooting boxes is what makes you learn the most. I rooted around 35-40 boxes, skipping dependent boxes/AD boxes/client-side attacks boxes as those topics were not covered in the exam at the time I passed it.</p>

<p>Don't spend too much time on a single box. If you don't find a foothold, use PWK forum and discord communities like <a href="https://discord.com/invite/mEtEFhp" target="_blank" rel="noopener noreferrer">InfoSecPrep</a> to get hints. I never spent more than 2-3 hours without asking for hints.</p>

<h1>Take smart notes</h1>

<p><br>More important than rooting boxes: <b>take notes about what you learned when rooting each box and about the things you didn't see</b>. What you should keep in mind when taking notes about a box is that these notes should help you overcome the difficulties you encountered doing the box when facing a similar box. If you don't do this you'll fall in the same traps over and over again.</p>

<p>Don't take stupid screenshot notes that you'll never read again. Take efficient, searchable notes describing how you rooted each box and the commands you used.</p>

<h1>Write your own enumeration script</h1>

<p><br>From day 1 in the labs try to <b>automate (with bash or python) the scanning phase (nmap) and the stuff you do everytime you come across particular services (http(s), smb, ftp,...)</b> and update your script as you progress through the labs. You should try to parallelize as much things as possible in your script.</p>

<p>You can use or take inspiration from scripts made by others like <a href="https://github.com/Tib3rius/AutoRecon" target="_blank" rel="noopener noreferrer">AutoRecon</a> but I highly recommend writing your own as it is a good scripting exercise and you may want to run your specific commands with your specific options.</p>

<p>Once you approach the end of your lab time, launch your enumeration script against all the boxes you rooted to check if it's getting the right infos to spot the foothold (if its easily spottable).</p>

I wrote a post about my enumeration script <a href="/OSCP/scan-script">here</a>.

<h1>TJNull OSCP-like boxes list and privesc resources</h1>

<p><br>You don't necessarily have to do all the boxes from the <a href="https://docs.google.com/spreadsheets/d/1dwSMIAPIam0PuRBkCiDI88pU3yzrqqHkDtBngUHNCw8/edit#gid=1839402159" target="_blank" rel="noopener noreferrer">HTB list</a> but these boxes are really good training to prepare for the exam. You may come across the same kind of tricks or exploits in the exam.</p>

<p>For privesc I recommend taking those two udemy courses:
- <a href="https://www.udemy.com/course/windows-privilege-escalation/" target="_blank" rel="noopener noreferrer">Windows privilege escalation</a>
- <a href="https://www.udemy.com/course/linux-privilege-escalation/" target="_blank" rel="noopener noreferrer">Linux privilege escalation</a></p>

<h1>Write an enumeration methodology</h1>

<p><br>From your notes of pwned PWK/HTB/vulnhub boxes and privesc courses, <b>write an enumeration methodology</b> and personal tips to not fall in the same traps as the ones you falled into.</p>

<p>This is crucial as <b>OSCP is all about enumeration</b>. You should have a methodical way of enumerating boxes and their services.</p>

<h1>The exam</h1>

<p><br>Start by focusing on the BOF box while your enumeration script is running.</p>

<p>Once you are done with the BOF box, keep in mind that offsec gives you enough time to do the exam, so <b>be methodical and enumerate everything</b>. <i>Don't leave any stone unturned</i>) and you'll eventually end up finding the foothold for each box.</p>

<p>It is important to proceed methodically because <b>there are a lot of services to enumerate in the exam</b>. You don't want to be unsure if you forgot to do something and loose time enumerating the same thing twice.</p>

<p>You'll most probably be blocked at some points in the exam. Don't panick and review your methodology: what did you miss? what could you try?</p>

<p>You should take into account that the proctoring software can take a lot of resources on your computer (for me: streaming 3 screens and a webcam). When I launched my enumeration script my CPU peaked regularly at 100% because of it; that didn't lead big lags but my computer was clearly pushed.</p>

<h1>The report</h1>

<p><br><b>Don't underestimate the time needed to write your report</b>: I took ~7 hours to make it while I thought I would be done in 2-3 hours. You really don't want to write you report in a hurry like I did so my advice would be to sleep some hours after the exam and immediately start writing your report afterwards. I used <a href="https://github.com/whoisflynn/OSCP-Exam-Report-Template" target="_blank" rel="noopener noreferrer">this template</a>.
</p>

<p><b>I wish you the best of luck. If I did it, so can you!</b></p>
