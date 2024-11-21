These are pre-configured config files for Cyber Patriot, which configure certian security settings. To apply them to an image, go to this github page in the image, download the zip of the reposiory, unzip it, and overwrite the configuration files already in the image with these.

1. Press the green "code" button and choose download zip
2. Open the terminal and enter the Downloads directory with <code>cd Downloads</code>
3. Unzip the zip file with <code>unzip cypat-configs.zip</code>
4. Gain administrator privilages with <code>sudo su</code>
5. Backup the old files first:<br>
<code>cp /etc/pam.d/common-password /etc/pam.d/common-password.bak</code><br>
<code>cp /etc/pam.d/pwquality.conf /etc/pam.d/pwquality.conf.bak</code><br>
<code>cp /etc/login.defs /etc/login.defs.bak</code><br>
<code>cp /etc/sysctl.conf /etc/sysctl.conf.bak</code><br>
<code>cp /etc/ssh/sshd_config /etc/ssh/sshd_config.bak</code><br>

6. Overwrite the old configurations with the secure configurations<br>
<code>cp cypat-configs/common-password /etc/pam.d/common-password</code><br>
<code>cp cypat-configs/pwquality.conf /etc/pam.d/pwquality.conf</code><br>
<code>cp cypat-configs/login.defs /etc/login.defs</code><br>
<code>cp cypat-configs/sysctl.conf /etc/sysctl.conf</code><br>
<code>cp cypat-configs/sshd_config /etc/ssh/sshd_config</code><br>

7. Run <code>sysctl -p</code> for the configurations from <code>sysctl.conf</code> to take effect.
