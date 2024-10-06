#Finding Files

```bash
Connected!
find hacker@commands~finding-files:~$ find flag
find: ‘flag’: No such file or directory
hacker@commands~finding-files:~$ find
.
./.dbus
./.dbus/session-bus
./.dbus/session-bus/924007f00738404793a6a7c3330a0265-0
./.profile
./.cache
./.cache/fontconfig
./.cache/fontconfig/111d16ad01ec7e96a1fc2ee34d740d2d-x86_64.cache-9
./.cache/fontconfig/3830d5c3ddfd5cd38a049b759396e72e-x86_64.cache-9
./.cache/fontconfig/CACHEDIR.TAG
./.cache/fontconfig/d589a48862398ed80a3d6066f4f56f4c-x86_64.cache-9
./.cache/fontconfig/de156ccd2eddbdc19d37a45b8b2aac9c-x86_64.cache-9
./.cache/fontconfig/91e6fd8df8eae133e8cc910311cd171d-x86_64.cache-9
./.cache/fontconfig/7ef2298fde41cc6eeb7af42e48b7d293-x86_64.cache-9
./.cache/fontconfig/573ec803664ed168555e0e8b6d0f0c7f-x86_64.cache-9
./.cache/fontconfig/d0972c3d32f097851eb916381fc38920-x86_64.cache-9
./.cache/fontconfig/4c599c202bc5c08e2d34565a40eac3b2-x86_64.cache-9
./.cache/fontconfig/c57959a16110560c8d0fcea73374aeeb-x86_64.cache-9
./.cache/sessions
./.local
./.local/share
./Desktop
./.config
./.config/Thunar
./.config/Thunar/uca.xml
./.config/xfce4
./.config/xfce4/xfconf
./.config/xfce4/xfconf/xfce-perchannel-xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfwm4.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-desktop.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xsettings.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/displays.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/thunar.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-keyboard-shortcuts.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-panel.xml
./.config/xfce4/desktop
./.config/xfce4/desktop/icons.screen0-1008x725.rc
./.config/xfce4/desktop/icons.screen.latest.rc
./.config/xfce4/xfwm4
./.config/xfce4/panel
./.config/xfce4/panel/launcher-18
./.config/xfce4/panel/launcher-18/17279643912.desktop
./.config/xfce4/panel/launcher-19
./.config/xfce4/panel/launcher-19/17279643913.desktop
./.config/xfce4/panel/launcher-20
./.config/xfce4/panel/launcher-20/17279643914.desktop
./.config/xfce4/panel/launcher-17
./.config/xfce4/panel/launcher-17/17279643911.desktop
./.bash_history
./a
./.bashrc
./.bash_logout
./.ICEauthority
hacker@commands~finding-files:~$ find / -Desktop
find: unknown predicate `-Desktop'
hacker@commands~finding-files:~$ find / -name flag 2>/dev/null
/usr/local/share/radare2/5.9.5/flag
/usr/local/lib/python3.8/dist-packages/pwnlib/flag
/opt/linux/linux-5.4/drivers/char/tpm/st33zp24/flag
/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
/opt/radare2/libr/flag
/nix/store/pmvk2bk4p550w182rjfm529kfqddnvh3-python3.11-pwntools-4.12.0/lib/python3.11/site-packages/pwnlib/flag
/nix/store/1yagn5s8sf7kcs2hkccgf8d0wxlrv5sz-radare2-5.9.0/share/radare2/5.9.0/flag
hacker@commands~finding-files:~$ cat /usr/local/share/radare2/5.9.5/flag
cat: /usr/local/share/radare2/5.9.5/flag: Is a directory
hacker@commands~finding-files:~$ cat /usr/local/lib/python3.8/dist-packages/pwnlib/flag
cat: /usr/local/lib/python3.8/dist-packages/pwnlib/flag: Is a directory
hacker@commands~finding-files:~$ cat /opt/linux/linux-5.4/drivers/char/tpm/st33zp24/flag
pwn.college{ofdqiT0nkRIMGF9eIbe20SltWdt.dJzM4QDLxMTO0czW}hacker@commands~finding-files:~$
```
