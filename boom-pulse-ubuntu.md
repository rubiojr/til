# Ubuntu Mate + pulseaudio with the UE BOOM bluetooth speaker

```
sudo apt-get install -y pulseaudio-module-bluetooth
pactl load-module module-bluetooth-discover
```

Pair the BOOM with your computer.

Add `load-module module-bluetooth-discover` to /etc/pulse/default.pa so it's always loaded.

You should see something like the following in `/var/log/syslog`:

```
Oct 19 21:41:09 x240 pulseaudio[6689]: [pulseaudio] module-bluetooth-device.c: Default profile not connected, selecting off profile
Oct 19 21:41:42 x240 bluetoothd[576]: /org/bluez/576/hci0/dev_00_0D_44_DF_5A_D6/fd0: fd(28) ready
```

Open the "Sound Preferences" application. In the hardware tab, select the UE BOOM and use the "High Fidelity" profile.

![](/images/soud-prefs-harware-ueboom.png)

Select the output device to you be "UE BOOM" in the "Sound Preferences" application.

![](/images/soud-prefs-harware-ueboom.png)