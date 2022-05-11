# CLI - Command Line Interface

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

1. Az eszköz neve és háttértárának teljes mérete és az elérhető tárhey (elérhető általában kb. *16Kb*).
2. A processzor kártya azonosító száma.
3. A processzor típusa.
4. Az ezközön található portok és azoknak sebességük (ebben az ehelyzetben a **FastEthernet/IEEE 802.3** sebessége *100Mbit/s*).
5. Az **NVRAM** mérete (itt tárolja az olvasható szöveges konfigurációt).
6. ***MEGKÉRDEZÉSRE VÁR***
7. Az eszköz operációs rendszerének adatai.
8. Itt lehet segítséget kérni, persze nem ingyen.
9. A szerzői jog.
10. Mikor lett lefordítva utoljára binárisra.

## Alap tudni valók
  A Command Line konfigurációt követően olvasható szöveges található a konfiguráció ezt az eszköz a **NVRAM**-ban tárolja el.

```
Router>
```
  Ezt promtnak nevezzük, ahol az eszköz hoszt neve **(hostname)** jelenik meg.

  Ha valamelyik parancsból legalább 2 vagy 3 karaktert beírtunk, akkor nyomhatunk egy *tab* billentyűt, ami automatikusan kiegészíti a parancsot (ez nem mindig igaz). Egy jó ellenőrzés az a legtöbb esetben, ha beírunk a parancsból 2/3 karaktert és, amikor nyomunk egy *tab* billentyűt és nem egészíti ki, akkor nagy valószínűséggel rossz helyen vagyunk. 

## Parancsok és azok mit csinálnak
### enable, ena
  Ezzel a paranccsal léphetünk be az úgy nevezett **privilegizált módba**. Onnan tudhatjuk, hogy ebben a módban vagyunk, hogy a **hostname** mögött nem egy *>* van hanem egy *#*
```
Router>enable       ; vagy röviden csak 'Router>ena'
Router#
```
### show, sh
  Ezt a parancsot csak is **privilegizált módban** használhatjuk. Ennek, ha egy parancsot írunk mögé, akkor megmutatja az ahhoz a parancshoz tartozó információkat. Ha egy *?*-et teszünk a **show** parancs után, akkor az megmutatja az összes parancsot amit használhatunk.
```
Router>ena
Router#show ?       ; vagy röviden csak 'Router#sh'
  aaa                Show AAA values
  access-lists       List access lists
  arp                Arp table
  cdp                CDP information
  class-map          Show QoS Class Map
  clock              Display the system clock
  controllers        Interface controllers status
  crypto             Encryption module
  debugging          State of each debugging option
  dhcp               Dynamic Host Configuration Protocol status
 --More-- 
```
  A *space*-et nyomva több parancsot is láthatunk, ha viszont ki akarunk lépni innen egy *esc* billentyűvel tudunk.
  Például nézzük meg, hogy milyen adatok kötődnek a **running-config**-hoz, ami a futó konfigurációt adja vissza olvasható formában.
```
Router>ena
Router#sh running-config 
Building configuration...

Current configuration : 556 bytes
!
version 12.4
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Router
!
!
!
!
!
!
!
!
no ip cef
no ipv6 cef
!
!
 --More-- 
```
  A *!* 10 ms idő várakozást jelent

### configuration terminal, conf t
  Ezt a parancsot csak is **privilegizált módban** használhatjuk. Ezzel a  paranccsal tudunkbelépni a konfigurációs terminálba, ahol konfigurálni tudjuk az esztközt. Onnan tudjuk, hogy a **konfigurációs móban** vagyunk, hogy a **hostname** útán zárójelek között ott van, hogy *config*
  
```
Router>ena
Router#conf t
Enter configuration commands, one per line.  End with CNTL/Z.
Router(config)#
```

### exit
  Ezzel a parancsal tudunk vissza lépni a **konfigurációs móból** **privilegizált módba**.

```
Router>ena
Router#conf t
Enter configuration commands, one per line.  End with CNTL/Z.
Router(config)#exit
Router#
```

### 

