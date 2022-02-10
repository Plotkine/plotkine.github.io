---
layout: i3-gap-setups
title: /i3-gap-setup
permalink: /i3-gap-setup
---

This post describes how to setup the windows manager i3-gaps on kali linux. I will describe how to set it up with my custom configuration to obtain this result:

<img src="/i3-gap-setup/result.jpg" alt="configuration result" width="1200" height="auto">

<h1>Install & configure i3-gaps</h1>

Download <a href="https://raw.githubusercontent.com/Plotkine/kali-config/main/wallpaper.jpg" target="_blank" rel="noopener noreferrer">this image</a> as <code>~/Pictures/wallpaper.jpg</code>.

Install a few tools (to configure the wallpaper, execute applications and allow terminal transparency) and i3:
<code>sudo apt install feh -y
sudo apt install rofi -y
sudo apt install compton -y
sudo apt install i3-gaps</code>

If i3-gaps wasn't in the <code>/etc/apt/sources.list</code> file, do <a href="https://launchpad.net/~kgilmer/+archive/ubuntu/speed-ricer" target="_blank" rel="noopener noreferrer">this</a>.

Add <a href="https://github.com/roosta/i3wsr" target="_blank" rel="noopener noreferrer">i3wsr</a>.

Create the <code>~/.config/i3</code> dir and put the <a href="https://github.com/Plotkine/kali-config/blob/main/i3_config" target="_blank" rel="noopener noreferrer">general config file</a> at <code>~/.config/i3/config</code>.

Place the status bar <a href="https://github.com/Plotkine/kali-config/blob/main/i3_i3status.conf" target="_blank" rel="noopener noreferrer">config file</a> at <code>/etc/i3status.conf</code>.

<h1>Start an i3 session</h1>

Logout and select i3 in the top right menu:

<img src="/i3-gap-setup/select_i3.jpg" alt="select i3">

Login again, right click on the terminal and select "Preferences". Configure everything like this:

<img src="/i3-gap-setup/settings.jpg" alt="configure preferences">

<h1>Documentation</h1>

Now that all is set, read the i3 <a href="https://i3wm.org/docs/userguide.html" target="_blank" rel="noopener noreferrer">documentation</a> to configure it according to your needs.
