# CLI - Command Line Interface

A Command Line konfigurációt követően olvasható szöveges található a konfiguráció ezt az eszköz a **NVRAM**-ban tárolja el

## A következő információk vannak feltűntetve (soronként) a **CLI** fejrészében
```
Cisco 1841 (revision 5.0) with 114688K/16384K bytes of memory.
Processor board ID FTX0947Z18E
M860 processor: part number 0, mask 49
2 FastEthernet/IEEE 802.3 interface(s)
191K bytes of NVRAM.
63488K bytes of ATA CompactFlash (Read/Write)
Cisco IOS Software, 1841 Software (C1841-ADVIPSERVICESK9-M), Version 12.4(15)T1, RELEASE SOFTWARE (fc2)
Technical Support: http://www.cisco.com/techsupport
Copyright (c) 1986-2007 by Cisco Systems, Inc.
Compiled Wed 18-Jul-07 04:52 by pt_team
```

1. Az eszköz neve és háttértárának teljes mérete és az elérhető tárhey (elérhető általában kb. *16Kb*)
2. A processzor kártya azonosító száma
3. A processzor típusa
4. Az ezközön található portok és azoknak sebességük (ebben az ehelyzetben a **FastEthernet/IEEE 802.3** sebessége *100Mbit/s*)
5. Az **NVRAM** mérete (itt tárolja az olvasható szöveges konfigurációt)
6. ***Megkérdezére vár***
7. Az eszköz operációs rendszerének adatai
8. Itt lehet segítséget kérni, persze nem ingyen
9. A szerzői jog
10. Mikor lett lefordítva utoljára binárisra

## Alap tudni valók
```
Router>
```
Ezt promtnak nevezzük, ahol az eszköz hoszt neve **(hostname)** jelenik meg
