# Mini S12 Pro

This is a collection of notes specific to the Mini S12 Pro mini PC

  * 12th Gen Intel Alder Lake-N100 Processor
  * Graphics is handled by Intel Arc and Iris
  * 16Gb Ram
  * 512Gb SSD
  * Pre-installed with Windows 11

## Networking

When trying to use WIFI the firmware included with the gentoo **LiveGUI USB** Image can be a little buggy

```bash
[  425.944448] iwlwifi 0000:00:14.3: Microcode SW error detected. Restarting 0x0.
[  425.944566] iwlwifi 0000:00:14.3: Start IWL Error Log Dump:
[  425.944571] iwlwifi 0000:00:14.3: Transport status: 0x0000004B, valid: 6
[  425.944576] iwlwifi 0000:00:14.3: Loaded firmware version: 83.e8f84e98.0 so-a0-hr-b0-83.ucode
[  425.944580] iwlwifi 0000:00:14.3: 0x00000071 | NMI_INTERRUPT_UMAC_FATAL
[  425.944585] iwlwifi 0000:00:14.3: 0x00A08200 | trm_hw_status0
[  425.944589] iwlwifi 0000:00:14.3: 0x00000000 | trm_hw_status1
[  425.944592] iwlwifi 0000:00:14.3: 0x004D9024 | branchlink2
[  425.944595] iwlwifi 0000:00:14.3: 0x004CF2F2 | interruptlink1
[  425.944597] iwlwifi 0000:00:14.3: 0x004CF2F2 | interruptlink2
[  425.944600] iwlwifi 0000:00:14.3: 0x00015080 | data1
```

In order to get this to work I've found the following is needed

  * First boot into the Windows 11 image to get some form of initialisation done on the wifi card
    Then reboot onto the gento USB image without fully shutting down
  * When connecting to a WIFI SSID, I found connecting to my main router would have issues based on the output of `dmesg`
    Connecting to a wifi repeater seemed to fix this

Another workaround for the initial setup would be to just use an ethernet connection instead.
Since the device does have an ethernet port on the back.
