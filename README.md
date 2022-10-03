# Lenovo Yoga Duet 7 13ITL6 

## Ubuntu 22.04 - Issues

### No sound with speakers
Check, if `snd_hda_intel` is used:
```
lsmod | grep snd_hda_intel
```

If yes, then run the following command ([source](https://askubuntu.com/a/1406739)):
```
echo "options snd-hda-intel model=generic" | sudo tee -a /etc/modprobe.d/alsa-base.conf
```

#### Links
* [**ArchLinux Wiki:** Lenovo ThinkPad X1 Yoga](https://wiki.archlinux.org/title/Lenovo_ThinkPad_X1_Yoga_(Gen_3)#Manual_method)
* [**Lenovo Forum 2021:** Yoga 7i 14ITL5 and 15ITL5 - ALC287 no sound with speaker & S3 ACPI mode not available - Linux Ubuntu](https://forums.lenovo.com/t5/Lenovo-Yoga-Series-Notebooks/Yoga-7i-14ITL5-and-15ITL5-ALC287-no-sound-with-speaker-S3-ACPI-mode-not-available-Linux-Ubuntu/m-p/5077334?page=1#5323234)
* [**BBS ArchLinux 2021:** thinkbook no audio](https://bbs.archlinux.org/viewtopic.php?id=266180)
* [**GitHub:** linux-realtek-alc287](https://github.com/thiagotei/linux-realtek-alc287)

