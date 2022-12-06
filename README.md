# Install-Mysql-5.6-Ubuntu-20.04

MySQL Download URL

```https://dev.mysql.com/get/Downloads/MySQL-5.6/mysql-5.6.46-linux-glibc2.12-x86_64.tar.gz```
### Open the terminal and follow along:

- Uninstall any existing version of MySQL

```
sudo rm /var/lib/mysql/ -R
```
- Delete the MySQL profile
```
sudo rm /etc/mysql/ -R
```
- Automatically uninstall mysql
```
sudo apt-get autoremove mysql* --purge
sudo apt-get remove apparmor
```
- Download version 5.6.46 from MySQL site
```
wget https://dev.mysql.com/get/Downloads/MySQL-5.6/mysql-5.6.46-linux-glibc2.12-x86_64.tar.gz
```
- Add mysql user group
```
sudo groupadd mysql
```

- Add mysql (not the current user) to mysql user group
```
sudo useradd -g mysql mysql
```

- Extract it

```
sudo tar -xvf mysql-5.6.46-linux-glibc2.12-x86_64.tar.gz
```
- Move it to /usr/local

```
sudo mv mysql-5.6.46-linux-glibc2.12-x86_64 /usr/local/
```

- Create mysql folder in /usr/local by moving the untarred folder
```
cd /usr/local
sudo mv mysql-5.6.46-linux-glibc2.12-x86_64 mysql

```

- set MySql directory owner and user group

```
cd mysql
sudo chown -R mysql:mysql *
```
- Install the required lib package
```
sudo apt-get install libaio1 libncurses5
```
- Execute mysql installation script

```
sudo scripts/mysql_install_db --user=mysql
```

- Set mysql directory owner from outside the mysql directory

```
sudo chown -R root .
```
- Set data directory owner from inside mysql directory

```
sudo chown -R mysql data
```
- Copy the mysql configuration file

```
sudo cp support-files/my-default.cnf /etc/my.cnf
```
- Start mysql
```
sudo bin/mysqld_safe --user=mysql &
sudo cp support-files/mysql.server /etc/init.d/mysql.server
```
- Set root user password

```
sudo bin/mysqladmin -u root password '[your new password]'
```

- Add mysql path to the system

```
sudo ln -s /usr/local/mysql/bin/mysql /usr/local/bin/mysql
```

- Reboot!

- Start mysql server

```
sudo /etc/init.d/mysql.server start
```
- Stop mysql server

```
sudo /etc/init.d/mysql.server stop
```

- Check status of mysql
```
sudo /etc/init.d/mysql.server status
```

- Enable myql on startup

```
sudo update-rc.d -f mysql.server defaults
```

*Disable mysql on startup (Optional)

```
sudo update-rc.d -f mysql.server remove
```

- REBOOT!

- Now login using below command, start mysql server if it's not running already 


```
mysql -u root -p
```

# ubuntu-20.04-Repository

    #cp /etc/apt/sources.list /etc/apt/sources.list.back

Timpa semua isi file sources.list dengan list repository Ubuntu 20.04
    
    #apt update
    
    #apt install update-manager
    
    #do-release-upgrade


# Awesome Indonesia Telegram Groups

A list of awesome Indonesia groups related to programming language on Telegram.

## List

### Programming Language

- **.NET**

  - [One .NET Indonesia](https://t.me/dotnetcore_id)
  - [.NET Indonesia](https://t.me/dotnetusergroup)
  - [Xamarin Indonesia](https://t.me/xamarinindonesia)

- **Android**

  - [ADB (Android Developer Bandung)](https://t.me/androidDevBdg)
  - [ADN (Android Developer Nasional)](https://t.me/androiddevelopernasional)
  - [Android Developer Lombok](https://t.me/android_lombok)
  - [Android - Teknorial.com](https://t.me/teknorialcom)
  - [AndroidDev Surabaya](https://t.me/androiddevsurabaya)
  - [Belajar Bareng Android Jakarta](https://t.me/BelajarBarengAndroid)
  - [SANDEC (Semarang Android Developer Center)](https://t.me/AndroidSemarang)
  - [Source Code Android](https://t.me/source_code_android)
  - [Yogyakarta Android Community](https://t.me/YACgroup)

- **Agile**

  - [Agile Circle Indonesia](https://t.me/agilecirclesid)

- **Assembly**

  - [Assembly Programming](https://t.me/AssemblyID)

- **Bash**
  - [Bash.ID](https://t.me/bashidorg)
- **Bootstrap**

  - [Bootstrap Indonesia](https://t.me/bootstrap_id)

- **C/C++**

  - [C/C++ Indonesia](https://t.me/CCpp_Indonesia)
  - [Indonesia C/C++ Warriors](https://t.me/idcplc)

- **Crystal**

  - [Crystal User Group Indonesia](https://t.me/CrystalID)

- **Dart**

  - [dart.web](https://t.me/dart_web)
  - [Flutter Indonesia](https://t.me/flutter_id)
  - [Flutter Jakarta](https://t.me/flutter_jkt)
  - [Flutter Makassar](https://t.me/fluttermakassar)
  - [Lombok Flutter](https://t.me/lombokflutter)

- **Elixir**

  - [Elixir ID](https://t.me/elixir_id)

- **Golang**

  - [Golang Indonesia](https://t.me/golangID)
  - [Golang Surabaya](https://t.me/golangSurabaya)

- **Haskell**

  - [Haskell ID](https://t.me/haskell_id)

- **Java**

  - [JVM User Group](https://t.me/JVMUserGroup)

- **JavaScript**

  - [Adonis.js Indonesia](https://t.me/adonisid)
  - [Angular Indonesia](https://t.me/AngularID)
  - [Deno Indonesia](https://t.me/deno_id)
  - [Electron Desktop User Group](https://t.me/electronatom)
  - [GatsbyJS Indonesia](https://t.me/gatsbyjsid)
  - [Ionic Indonesia](https://t.me/indonesiaionic)
  - [JakartaJS](https://t.me/jakartajs)
  - [Javascript Indonesia](https://t.me/js_id)
  - [Jogja Js](https://t.me/jogjajs)
  - [Lombok Js](https://t.me/lombokjs)
  - [NativeScript ID](https://t.me/nativescript_id)
  - [Next.js Indonesia](https://t.me/nextjs_id)
  - [Nodejs Indonesia](https://t.me/nodejsid)
  - [NuxtJs Indonesia](https://t.me/nuxtjsid)
  - [Polymer Indonesia](https://t.me/polymer_id)
  - [React Indonesia](https://t.me/react_id)
  - [React Native Indonesia](https://t.me/reactnative_id)
  - [React India](https://t.me/reactjsbharat)
  - [Semarang JS](https://t.me/SemarangJS)
  - [SurabayaJs](https://t.me/surabayajs)
  - [Svelte Indonesia](https://t.me/svelte_id)
  - [Vue.js Indonesia](https://t.me/vuejsindonesia)

- **Kotlin**

  - [Kotlin Cirebon](https://t.me/kotlin_crb)
  - [Kotlin Indonesia](https://t.me/KotlinID)

- **Pascal - Delphi**

  - [Delphi Indonesia](https://t.me/delphiindonesia)
  - [Pascal Indonesia](https://t.me/PascalID)

- **PHP**

  - [CodeIgniter Indonesia](https://t.me/codeigniterindonesia)
  - [Laravel Indonesia](https://t.me/laravelindonesia)
  - [Laravel Brazil](https://t.me/laravelbr)
  - [PHP Indonesia for Business](https://t.me/PHPIDforBusiness)
  - [PHP Indonesia for Student](https://t.me/PHPIDforStudent)
  - [PHP Indonesia Jogloraya](https://t.me/phpjogloraya)
  - [Symfony Framework Indonesia](https://t.me/symfonyid)
  - [Telegram Bot PHP - Indonesia](https://t.me/botphp)
  - [Yii Framework Indonesia](https://t.me/YiiFrameworkIndonesia)

- **Python**
  
  - [codewithbiki](https://t.me/codewithbiki)
  - [Django Indonesia](https://t.me/DjangoID)
  - [FastAPI Indonesia](https://t.me/fastapiid)
  - [Flask ID](https://t.me/flaskid)
  - [Lombok.py](https://t.me/lombok_py)
  - [mks.py](https://t.me/mkspy)
  - [Python ID](https://t.me/pythonID)
  - [Python ID Jogja](https://t.me/pyjogja)
  - [Surabaya.py](https://t.me/surabayadotpy)
  
- **Ruby**

  - [Rails Indonesia](https://t.me/RailsID)
  - [Ruby Indonesia](https://t.me/ruby_id)

- **Rust**

  - [Rust Indonesia](https://t.me/rustindonesia)

- **Swift**

  - [Swift Indonesia](https://t.me/swiftID)

- **Typescript**
  - [Typescript Indonesia](https://t.me/TypescriptIndonesia)
- **SAP ABAP Indonesia**
  - [SAP-ABAP Indonesia](https://t.me/sapabapindonesia)

### BLOCKCHAIN

- [Friends with Blockchain](https://t.me/friendswithblockchain)
- [Hyperledger (Enterprise) Blockchain Indonesia](https://t.me/hl_id)
- [Nusantara Chain (Nuchain)](https://t.me/nusantarachain)

### DATABASE

- **Microsoft SQL Server**

  - [SQL Server Indonesia](https://t.me/sqlserverid)

- **MongoDB**

  - [MongoDB Indonesia](https://t.me/MongoDB_ID)

- **MySQL**

  - [MySQL Indonesia](https://t.me/mysqlid)

- **PostgreSQL**
  - [PostgreSQL Indonesia](https://t.me/postgresql_id)

### FIREBASE

- [Firebase Indonesia](https://t.me/firebaseindonesia)

### IOT

- [Arduino Indonesian Community](https://t.me/ArduinoIndonesianCommunity)
- [Raspberry PI Indonesia](https://t.me/raspberrypi_id)
- [arduinoindonesia.id](https://t.me/edukasielektronika)

### DevOps

- [Cloud Computing Indonesia](https://t.me/cloudcomputingindonesia)
- [Docker.id](https://t.me/dockeridn)
- [IDDevOps](https://t.me/IDDevOps)
- [Kubernetes Indonesia](https://t.me/kubernetesindonesia)

### SQA

- [Indonesian Software Quality Assurace](https://t.me/sqa_id)
- [ISQA Chapter Jogja](https://t.me/joinchat/HxMrghPz5z3hr0eiRBcXOQ)
- [Malang Quality Assurace](https://t.me/qamalang)

### Cloud Computing Services

- [#JuaraGCP](https://t.me/JuaraGCP)
- [AWS User Group Indonesia](https://t.me/AWSUserGroupID)
- [AWS Analytics User Group Indonesia](https://t.me/AWSDataUserGroupID)
- [Azure ID](https://t.me/azureindo)
- [GCP User Group Indonesia](https://t.me/GCPUserID)
- [Google Cloud Platform Indonesia](https://t.me/GCP_ID)


### Data PlayGround

- [Artificial Intelligence Indonesia](https://t.me/ArtificialIntelligence_Indonesia)
- [Asosiasi Ilmuwan Data Indonesia (AIDI)](https://t.me/aidindonesia)
- [Big Data Official Group](https://t.me/idbigdata)
- [Business Intelligence Indonesia](https://t.me/businessintelligenceID)
- [Data Scientist Indonesia](https://t.me/datascienceindonesia)
- [Machine Learning Indonesia](https://t.me/machinelearningid)
- [Machine Learning ID Lombok](https://t.me/machinelearninglombok)
- [Natural Language ID](https://t.me/nlp_lounge)
- [PyTorch Indonesia](https://t.me/pytorchid)
- [ScrapeID](https://t.me/ScrapeID)
- [TensorFlow Indonesia](https://t.me/tensorflowid)

### Development

- [Belajar GNU R Indonesia](https://t.me/GNURIndonesia)
- [Belajar Golang MariaDB](https://t.me/BelajarGolangMariaDB)
- [Belajar HTML](https://t.me/belajarhtmlcss)
- [Bogor Developers](https://t.me/BogorDev)
- [Bot Telegram API](https://t.me/TgBotID)
- [Cilegon Developer](https://t.me/cilegondev)
- [CirebonDev](https://t.me/crbdev)
- [[c]oretan Script](https://t.me/cScript)
- [Femalegeek](https://t.me/femalegeek)
- [Free Kelas Github](https://t.me/freekelasgithub)
- [Frontend Developer Indonesia](https://t.me/FrontEndID)
- [Gresik Dev](https://t.me/gresikdev)
- [IAM Indonesia](https://t.me/IAMIndonesia)
- [IDStack](https://t.me/idstack)
- [Info Event Teknologi](https://t.me/eventteknologi)
- [IT Nusantara](https://t.me/ITNusantara)
- [JemberDev](https://t.me/DjemberDev)
- [Kabayan Coding](https://t.me/kabayan_coding)
- [Kelas Mobile Malang](https://t.me/KelasMobileMalang)
- [Komunitas Backend Developer](https://t.me/BackEndID)
- [Komunitas Belajar Koding](https://t.me/komunitasbk)
- [Kongkow IT Medan](https://t.me/kongkowITMedan)
- [Kongkow IT Pekanbaru](https://t.me/kongkowITpekanbaru)
- [Kotakode](https://t.me/kotakodebetachat)
- [Odoo - OpenERP Indonesia](https://t.me/odooindonesia)
- [Pasuruan Dev](https://t.me/pasuruandev)
- [Programmer Lokal](https://t.me/programmerlokal)
- [Programmer Semarang Raya](https://t.me/programersemarangraya)
- [RantauDev](https://t.me/rantaudev)
- [Santren Koding](https://t.me/santrenkoding)
- [SARCCOM Universe](https://t.me/sarccomuniverse)
- [Sidoarjo Dev](https://t.me/sidoarjodev)
- [SinauDev - Sinau Development](https://t.me/sinaudev)
- [Software Engineer Indonesia](https://t.me/soft_eng_id)
- [SparkAR Indonesia](https://t.me/sparkarindonesia)
- [Surabaya Dev](https://t.me/surabayadev)
- [LamonganDev](https://t.me/lamongandev)
- [Taman Kode-Kode](https://t.me/tamankodekode)
- [Tailwind Indonesia](https://t.me/TailwindID)
- [Teknologi Umum](https://t.me/teknologi_umum)
- [Tech in Asia Dev Community](https://t.me/TIAdevcommunity)
- [UI/UX Indonesia](https://t.me/UiuxIndo)
- [UXiD Lombok](https://t.me/uxidlombok)
- [Vim Indonesia](https://t.me/VimID)
- [WordPress](https://t.me/idwordpress)
- [Channel Otodidak Pemrograman](https://t.me/otodidak_ngoding)
- [Kulkul.tech Community - Meetup and Dev Community](https://t.me/kulkultech)
- [Belajar Coding Bareng](https://t.me/BelajarCoding)

### Microservice

- [Microservice Architecture](https://t.me/msarchitecture)
- [Microservice Indonesia](https://t.me/microservices_id)

### LINUX

- [Arch Linux Indonesia](https://t.me/ArchLinuxID)
- [Belajar GNU/Linux Indonesia](https://t.me/GNULinuxIndonesia)
- [BlankOn Linux](https://t.me/BlankOnLinux)
- [CentOS.ID](https://t.me/centosID)
- [Deepin Linux Indonesia](https://t.me/deepin_indonesia)
- [Dotfiles Indonesia](https://t.me/dotfiles_id)
- [Elementary OS Indonesia](https://t.me/elementaryID)
- [Fedora Indonesia](https://t.me/FedoraID)
- [GNOME Indonesia](https://t.me/gnomeid)
- [Grup Pengguna Gentoo Indonesia](https://t.me/GPG_Indonesia)
- [Kali Linux Indonesia](https://t.me/KaliLinuxID)
- [KDE Indonesia](https://t.me/kdeid)
- [Komunitas GNU/Linux Malang](https://t.me/linuxmalang)
- [Komunitas Linux Jember](https://t.me/linuxjember)
- [Linux Mint Indonesia](https://t.me/mint_id)
- [Manjaro Indonesia](https://t.me/manjaroID)
- [openSUSE Indonesia](https://t.me/openSUSE_ID)
- [ParrotSec Indonesia](https://t.me/parrotsecurityindonesia)
- [Ubuntu Indonesia](https://t.me/ubuntu_id)
- [Paguyuban Linux Solo](https://t.me/linuxsolo)
- [Linux From Scratch ID](https://t.me/lfsid)

### BSD

- [Laskar Setan Merah - Sharing All About FreeBSD](https://t.me/setanmerahID)

### Mikrotik

- [Mikrotik Indonesia](https://t.me/mikrotikindonesia)

### Security

- [DevSecOps Indonesia](https://t.me/DevSecOpsIndonesia)
- [ForensicaID](https://t.me/ForensicaID)
- [Reversing.ID](https://t.me/reversingid)
- [Orang Siber Indonesia](https://t.me/orangsiber)
- [IT SECURITY INDONESIA](https://t.me/itsecurityindonesia)
- [OSINT Indonesia](https://t.me/OSINT_ID)

### Windows

- [PegelWindows](https://t.me/pegelwindows)
- [Windows 10 Community ID](https://t.me/WinTenGroup)
- [WINDOWS SERVER INDONESIA](https://t.me/WindServID)

### MacOS

- [macOS Indonesia](https://t.me/macOSID)

### iOS

- [iKaskus](https://t.me/ikaskus)
- [iNitial E](http://t.me/initialestore)

### Tentang Telegram

- [Telegram beta](https://t.me/tgbeta)
- [Telegram Themes](https://t.me/themeschannel)
- [Tentang Telegram](https://t.me/tentangtelegram)

### Open Source

- [DOSCOM - Dinus Open Source Community](https://t.me/doscomedia)

### Lowongan Kerja

- [Freelancer - Indonesia](https://t.me/freelancerID)
- [Freelance Project IT](https://t.me/freelance_01)
- [Kotakode Jobs](https://t.me/kotakodejobs)
- [LOKER DEVELOPER/PROGRAMMER](https://t.me/LokerDeveloper)
- [Loker Jakarta](https://t.me/loker_jakarta)
- [Lowongan Kerja IT](https://t.me/LowonganKerjaIT)
- [Rails Indonesia Loker](https://t.me/RailsID_LOKER)
- [Ruby Indonesia Loker](https://t.me/RubyID_LOKER)

### Game Development

- [Indonesian GDevelop](https://t.me/GDevelopID)
- [Komunitas Godot Indonesia](https://t.me/godot_indonesia)
- [Lombok Games Developers (LGD)](https://t.me/lombokgamedev)
- [GAMERANG - Game Developer Semarang](https://t.me/gamerang)

### Startup

- [Cafe Startup 140315](https://t.me/cafestartup)
- [STARTUP INDONESIA on TELEGRAM](https://t.me/startupindonesia)
- [Startup Weekend Indonesia](https://t.me/startupweekendindonesia)

### Science

- **Geographic Information System and Remote Sensing**
  - [GIS Indonesia](https://t.me/gis_id)
  - [QGIS Indonesia](https://t.me/qgisindonesia)
  - [Leaflet.js Indonesia](https://t.me/leafletid)

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) for details.

## Listed by _Hendi Santika_

- Email: hendisantika@gmail.com
- Telegram: [@hendisantika34](https://t.me/hendisantika34)

## License

[![CC0](https://i.creativecommons.org/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, [Hendi Santika](https://github.com/hendisantika) has waived all copyright and related or neighboring rights to this work.


