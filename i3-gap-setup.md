---
layout: i3-gap-setups
title: /i3-gap-setup
permalink: /i3-gap-setup
---

<h1>Introduction</h1>

<p>This post describes how to setup the windows manager i3-gaps on kali linux. I will describe how to set it up with my custom configuration to obtain this result:

<img src="/i3-gap-setup/result.jpg" alt="configuration result" width="1200" height="auto"></p>

<h1>Installing i3-gaps</h1>

<p>Download <a href="https://raw.githubusercontent.com/Plotkine/kali-config/main/wallpaper.jpg" target="_blank" rel="noopener noreferrer">this image</a> as <code>~/Pictures/wallpaper.jpg</code>.

<img src="/i3-gap-setup/saving_wallpaper.jpg" alt="saving wallpaper">

These tools will be used by i3 to configure the wallpaper, execute applications and allow terminal transparency:
<br><code>sudo apt install feh -y</code>
<code>sudo apt install rofi -y</code>
<code>sudo apt install compton -y</code>

Install i3-gaps:
<br><code>sudo apt install i3-gaps</code>

If i3-gaps wasn't in the sources file, do <a href="https://launchpad.net/~kgilmer/+archive/ubuntu/speed-ricer" target="_blank" rel="noopener noreferrer">this</a>.

Add <a href="https://github.com/roosta/i3wsr" target="_blank" rel="noopener noreferrer">i3wsr</a>.</p>

<h1>Configuration files</h1>

<p>Let us create the necessary folder with this command: <code>mkdir -p ~/.config/i3</code>. Then we can put the <a href="https://github.com/Plotkine/kali-config/blob/main/i3_config" target="_blank" rel="noopener noreferrer">i3 general configuration file</a> at <code>~/.config/i3/config</code>.</p>

<p>Now we can place the <a href="https://github.com/Plotkine/kali-config/blob/main/i3_i3status.conf" target="_blank" rel="noopener noreferrer">status bar configuration file</a> at <code>/etc/i3status.conf</code> (this file is owned by root).</p>

<h1>Start an i3 session</h1>

<p>Logout:
  
<img src="/i3-gap-setup/logout.jpg" alt="logout">

Select i3 on the top right menu:

<img src="/i3-gap-setup/select_i3.jpg" alt="select i3">

Login again, right click on the terminal and select "Preferences":

<img src="/i3-gap-setup/preferences.jpg" alt="select preferences">

Configure everything like this:

<img src="/i3-gap-setup/settings.jpg" alt="configure preferences"></p>

<p>Now that all is set, read the i3 <a href="https://i3wm.org/docs/userguide.html" target="_blank" rel="noopener noreferrer">documentation to configure it according to your needs!</a>.</p>
