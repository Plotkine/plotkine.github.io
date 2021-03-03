---
layout: page
title: /OSCP/learning-tips
permalink: /OSCP/learning-tips
---

<h1>LEARNING TIPS FOR OSCP STUDENTS</h1>

<h2>-1) My background before enrolling into PWK</h2>
<br>
- rooted a few HTB boxes
- knowledge of: python, linux basics
- certifications: eJPT, eCPPT

<h2>0) Exercises/lab report</h2>

<br><p>Whether you do exercises and lab report is your personal choice. Since the 2020 update there are alot of exercises (~90 sets if I remember correctly); taking you at least 15 days if you work hard on it.</p>

<p>On one side, if you do quick maths you'll realize it's easy to be stuck at 65 or 67.5 points in the exam so it's good to secure passing score. On the other side, time spent doing the exercises could be better spent in the labs rooting boxes.</p>

<p>I personnally don't recommend doing the exercises and the lab report. Lab is the place where you really learn things [edit: if you have some pentesting basics].</p>

1) Rooting boxes

Root as many boxes as you can in the PWK labs.

I rooted around 35-40 boxes, skipping dependent boxes/AD boxes/client-side attacks boxes. More importantly than rooting boxes: take notes about what you learned rooting each boxes and the mistakes you did. The thing to keep in mind when taking notes about a box is that they should help you overcome the difficulties you encountered doing the box, when facing a similar box. Also don't spend too much time on a single box if you don't find the entry point: use PWK forum and discord communities to get hints. I never spent more than 2-3 hours without asking for hints.

[Edit: Just before my lab time expired I launched my enumeration script against all the boxes I rooted to check if it was getting the right infos for the foothold. I think it's a good thing to reinforce your script if it's not complete enough, and to boost your confidence on the fact that the foothold is always there, somewhere, right in front of you!]

2) TJNull OSCP-like boxes list

I personnally only did ~8 boxes from the HTB list and none from the vulnhub one but these are really good resource to help you prepare for the exam.

3) Write an enumeration methodology

From all your pwned box in PWK labs/HTB & vulnhub lists, write an enumeration methodology and personal tips to not fall in the same traps as the ones you falled into.

This is crucial. You should have a methodical way of enumerating boxes and their services.

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
