# Ansible Workshop

## Instrukcja uruchomienia środowiska laboratoryjnego

1. **Wymagane komponenty**

Komputer PC z systemem operacyjnym MS Windows 10, Apple macOS lub Linux o następujących minimalnych parametrach:
- procesor min. 4 rdzeniowy lub 2 rdzeniowy z technologią Hyper-Threading i włączoną opcją wirtualizacji w BIOS / UEFI
- min. 8 GB pamięci RAM
- min. 40 GB wolnej przestrzeni dyskowej

Dodatkowo należy pobrać i zainstalować następujące oprogramowanie:

- Vagrant - narzędzie do automatyzacji uruchamiania środowisk wirtualnych https://www.vagrantup.com/downloads
- VirtualBox - środowisko wirtualizacyjne https://www.virtualbox.org/wiki/Downloads
- Git - narzędzie do kontroli wersji plików https://git-scm.com/downloads

> Instalacja powyższych komponentów wymaga posiadania uprawnień Administratora systemu operacyjnego. 

2. **Uruchomienie środowiska laboratoryjnego**

Po instalacji wymaganego oprogramowania należy pobrać plik z definicją laboratoryjnego środowiska Ansible i zapisać go w lokalnym katalogu np. 'AnsibleWorkshop' na dysku C: (w sytemach MS Windows) lub w katalogu domowym użytkownika (w systemach Apple macOS i Linux):
- https://github.com/piotrszewczuk/AnsibleWorkshop-OL8/raw/main/Vagrantfile

> **UWAGA !!!**
> **Przy pobieraniu pliku "Vagrantfile" ważne jest, aby go zapisać w takiej postaci w jakiej jest udostępniony na stronie GitHub, bez żadnych rozszerzeń typu .txt, zmian itp. Najlepiej w przeglądarce internetowej, na wskazanym linku, wywołać menu kontekstowe i wybrać opcję "Zapisz link jako".**

Po pobraniu pliku Vagrantfile należy uruchomić terminal i wykonać następujące polecenia: 
- w systemie MS Windows
```bash
cd c:\AnsibleWorkshop
vagrant box add --name oraclelinux/8 https://yum.oracle.com/boxes/oraclelinux/ol8/OL8U4_x86_64-vagrant-virtualbox-b220.box
vagrant up
```
- w systemach Apple macOS i Linux
```bash
cd ~/AnsibleWorkshop
vagrant box add --name oraclelinux/8 https://yum.oracle.com/boxes/oraclelinux/ol8/OL8U4_x86_64-vagrant-virtualbox-b220.box
vagrant up
```
Poprawne inicjalizowanie środowiska laboratoryjnego powinno zakończyć się uruchomieniem 4 maszyn wirtualnych widocznych w programie VirtualBox, tak jak na poniższym zrzucie ekranu.

![](https://github.com/piotrszewczuk/OpenSourceTech2021/blob/main/images/vb-ansible-lab.png)
