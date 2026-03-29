# orcon-wtw

This is a skelton repository for the Orcon HRC ventilation units. The YAML configuration is intended for Home Assistant along with the RF-ethernet bridge 02EM23 (firmware 53 or higher). 

Pairing instructions for the VMD-15RMS86-2.

Turn off HRC, turn on HRC unit (unit is in pairing mode for 2 minutes).
Write OEM code 0x0067 (ORCON OEM) to register 41101:
```mbpoll -a2 -r 41101 -1 -0 192.168.1.83 0X067```

Write 0xC8A2 0x0001 to register 43000:
```mbpoll -a2 -r 43000 -1 -0 192.168.1.83 0xC8A2 0x0001```

Write 0x0203 to register 43004 to bind the HRC:
```mbpoll -a2  -r 43004 -1 -0 192.168.1.83 0X0203```

