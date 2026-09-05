### Настройка VPN ProxyVM { #qubes-vpn-proxyvm }

**Пропустите этот шаг, если вы не хотите использовать VPN и будете использовать только Tor либо если VPN также недоступен.**

Это руководство также должно работать с любым провайдером OpenVPN (например, Mullvad, IVPN, Safing.io или Proton VPN).

Оно основано на руководстве, предоставленном самими разработчиками Qubes OS (<https://github.com/Qubes-Community/Contents/blob/master/docs/configuration/vpn.md> <sup>[[Archive.org]](https://web.archive.org/web/https://github.com/Qubes-Community/Contents/blob/master/docs/configuration/vpn.md)</sup>). Если вы знакомы с этим процессом, можете следовать их руководству.

Кроме того, у Mullvad есть справочная статья, в которой описывается настройка Proxy VM: <https://mullvad.net/en/help/qubes-os-4-and-mullvad-vpn/> <sup>[[Archive.org]](https://web.archive.org/web/https://mullvad.net/en/help/qubes-os-4-and-mullvad-vpn/)</sup>.

#### Создание ProxyVM { #qubes-create-proxyvm }

- Щёлкните значок Applications (в левом верхнем углу)

- Щёлкните Create Qubes VM

- Задайте любое имя и метку: рекомендуем "VPNGatewayVM"

- Выберите Type: Standalone Qube copied from a template

- Выберите Template: Debian-11 (по умолчанию)

- Выберите Networking:

    - Выберите sys-whonix, если хотите использовать VPN поверх Tor / только Tor (рекомендуется)

    - Выберите sys-firewall, если хотите использовать Tor поверх VPN / без Tor или VPN / только VPN

- Advanced: отметьте provides network

- Отметьте "Start Qube automatically on boot"

- Создайте ВМ

    - Если вы выбираете VPN поверх Tor, перейдите в настройки созданной ProxyVM и выберите "sys-vpn" для сетевого подключения.
        + Более простой способ настроить ProxyVM — просто запустить VPN-клиент в ProxyVM.
        + Обычно при подключении к сайту вашего VPN-провайдера он сообщает, правильно ли направляется ваш трафик через VPN.

    - Если вы выбираете Tor поверх VPN, следует сделать наоборот: для сетевого подключения ProxyVM нужно указать "sys-tor", а для ВМ "sys-tor" — "sys-vpn".
        + Проверьте подключение ВМ к интернету, запустив браузер внутри ProxyVM. Откройте <https://check.torproject.org> <sup>[[Archive.org]](https://web.archive.org/web/https://check.torproject.org/)</sup> (там должно быть указано, что вы подключены к Tor)

#### Загрузка конфигурации VPN у VPN-провайдера, принимающего наличные/Monero { #qubes-vpn-config-download }

##### Если вы можете использовать Tor { #qubes-vpn-tor }

**Используя Tor Browser (будьте внимательны: не используйте для этого браузер Clearnet),** скачайте у своего VPN-провайдера необходимые файлы конфигурации OpenVPN для Linux.

Это можно сделать с помощью встроенного Tor Browser Qubes OS: откройте значок Applications (в левом верхнем углу) и выберите приложение Disposable Tor Browser.

##### Если вы не можете использовать Tor { #qubes-vpn-no-tor }

Запустите браузер из DisposableVM и скачайте у своего VPN-провайдера необходимые файлы конфигурации OpenVPN для Linux. См. [Что делать, когда Tor и VPN недоступны?](#tor-vpn-not-possible)

Завершив загрузку конфигурационных файлов в Disposable Browser (обычно это ZIP-файл), скопируйте их на VPN Gateway в ProxyVM (щелкните файл правой кнопкой мыши и отправьте в другую AppVM).

#### Настройка ProxyVM { #qubes-configure-proxyvm }

**Пропустите этот шаг, если вы не будете использовать VPN**

- Щёлкните в левом верхнем углу

- Выберите только что созданную VPN VM

- Откройте Files VPN VM

- Перейдите в "Qubesincoming" > dispXXXX (это была ваша Disposable Browser VM)

- Дважды щёлкните скачанный ZIP-файл с файлами конфигурации OpenVPN, чтобы распаковать его

- Теперь снова выберите VPN VM и запустите терминал

- Установите OpenVPN следующей командой ```sudo apt-get install openvpn```

- Скопируйте все файлы конфигурации OpenVPN, предоставленные вашим VPN-провайдером, в /etc/openvpn/

- Для всех файлов конфигурации OpenVPN (для каждого местоположения):

    - Отредактируйте каждый файл с помощью ```sudo nano configfile``` (не забудьте sudo, чтобы редактировать файл в /etc)

    - Измените протокол с "udp" на "tcp" (Tor не поддерживает UDP)

    - Измените порт на поддерживаемый вашим VPN-провайдером TCP-порт (например, 80 или 443)

    - Сохраните и закройте каждый файл

- Отредактируйте файл конфигурации OpenVPN (/etc/default/openvpn), введя ```sudo nano /etc/default/openvpn```

    - Измените ```#AUTOSTART="all"``` на ```AUTOSTART="all"``` (то есть удалите "#")

    - Сохраните и закройте файл

- Отредактируйте файл правил межсетевого экрана Qubes (/rw/config/qubes-firewall-user-script), введя "sudo nano /rw/config/qubes-firewall-user-script"

    - Добавьте следующие строки (без кавычек и примечаний в скобках)

        + ```virtualif=10.137.0.17```

> (Это IP-адрес ProxyVM; он не является динамическим, и после перезагрузки его может потребоваться изменить)

- ```vpndns1=10.8.0.1```

> (Это первый DNS-сервер вашего VPN-провайдера; он не должен измениться)

- ```vpndns2=10.14.0.1```

> (Это второй DNS-сервер вашего VPN-провайдера; он не должен измениться)

- ```iptables -F OUTPUT```

- ```iptables -I FORWARD -o eth0 -j DROP```

- ```iptables -I FORWARD -i eth0 -j DROP```

- ```ip6tables -I FORWARD -o eth0 -j DROP```

- ```ip6tables -I FORWARD -i eth0 -j DROP```

> (Эти правила блокируют исходящий трафик, когда VPN отключён; это аварийный выключатель. Подробнее: <https://linuxconfig.org/how-to-create-a-vpn-killswitch-using-iptables-on-linux> <sup>[[Archive.org]](https://web.archive.org/web/https://linuxconfig.org/how-to-create-a-vpn-killswitch-using-iptables-on-linux)</sup> )

- ```iptables -A OUTPUT -d 10.8.0.1 -j ACCEPT```

- ```iptables -A OUTPUT -d 10.14.0.1 -j ACCEPT```

> (Эти правила разрешают DNS-запросы к DNS-серверам вашего VPN-провайдера для разрешения имён VPN-серверов в файлах конфигурации OpenVPN)

- ```iptables -F PR-QBS -t nat```

- ```iptables -A PR-QBS -t nat -d $virtualif -p udp --dport 53 -j DNAT --to $vpndns1```

- ```iptables -A PR-QBS -t nat -d $virtualif -p tcp --dport 53 -j DNAT --to $vpndns1```

- ```iptables -A PR-QBS -t nat -d $virtualif -p udp --dport 53 -j DNAT --to $vpndns2```

- ```iptables -A PR-QBS -t nat -d $virtualif -p tcp --dport 53 -j DNAT --to $vpndns2```

> (Эти правила перенаправляют все DNS-запросы от ProxyVM на DNS-серверы VPN-провайдера)

- Перезапустите ProxyVM, введя "sudo reboot"

- Проверьте VPN-подключение ProxyVM: запустите в ней браузер и перейдите на страницу проверки вашего VPN-провайдера. Теперь там должно быть указано, что вы подключены к VPN:

    - Mullvad: <https://mullvad.net/en/check/> <sup>[[Archive.org]](https://web.archive.org/web/https://mullvad.net/en/check/)</sup>

    - IVPN: <https://www.ivpn.net/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.ivpn.net/)</sup> (проверьте верхний баннер)

    - Proton VPN: следуйте инструкциям здесь: <https://protonvpn.com/support/vpn-ip-change/> <sup>[[Archive.org]](https://web.archive.org/web/https://protonvpn.com/support/vpn-ip-change/)</sup>

#### VPN поверх Tor { #qubes-vpn-over-tor-setup }

##### Настройка disposable Browser Qube для использования VPN поверх Tor { #qubes-browser-qube }

- В меню Applications (в левом верхнем углу) выберите Disposable Fedora VM

- Перейдите в Qube Settings

- Щёлкните Clone Qube и задайте, например, имя "sys-VPNoverTor"

- Снова в меню Application выберите только что созданный клон

- Перейдите в Qube Settings

- Измените Networking на созданный ранее ProxyVPN

- Щёлкните OK

- Запустите браузер в Whonix Workstation

- Убедитесь, что VPN-подключение работает

Теперь у вас должна быть Disposable Browser VM, работающая с VPN, оплаченным наличными/Monero, поверх Tor.

#### Tor поверх VPN { #qubes-tor-over-vpn-setup }

Перенастройте Whonix Gateway VM, чтобы она использовала ProxyVM в качестве NetVM вместо sys-firewall:

- В меню Applications (в левом верхнем углу) выберите ВМ sys-whonix.

- Перейдите в Qube Settings

- Измените Networking NetVM на созданный ранее ProxyVPN вместо sys-firewall

- Щёлкните OK

- Создайте Whonix Workstation Disposable VM (следуйте этому руководству: <https://www.whonix.org/wiki/Qubes/DisposableVM> <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Qubes/DisposableVM)</sup>)

- Запустите браузер из ВМ и убедитесь, что VPN-подключение работает.

Кроме того, можно создать disposable VM другого типа (но она будет менее безопасной, чем Whonix):

- В меню Applications (в левом верхнем углу) выберите Disposable Fedora VM

- Перейдите в Qube Settings

- Щёлкните Clone Qube и задайте, например, имя "sys-TorOverVPN"

- Снова в меню Application выберите только что созданный клон

- Перейдите в Qube Settings

- Измените Networking на созданный ранее sys-whonix

- Щёлкните OK

- Запустите браузер в ВМ

- Убедитесь, что VPN-подключение работает

Теперь у вас должна быть Disposable Browser VM, работающая с Tor поверх VPN, оплаченным наличными/Monero.

#### Любая другая комбинация? { #qubes-other-combo }

**Например, VPN поверх Tor поверх VPN**

К этому моменту вы уже должны понимать, насколько легко с Qubes направлять трафик от одной ВМ к другой.

Вы можете создать несколько ProxyVM для VPN-подключений и оставить Whonix для Tor. Чтобы изменить схему, достаточно изменить настройки NetVM различных ВМ.

Возможна следующая схема:

- Одна VPN ProxyVM для базового подключения Qubes OS

- Использование ВМ sys-whonix (Whonix Gateway), получающей сеть от первой ProxyVM

- Вторая VPN ProxyVM, получающая сеть от sys-whonix

- Disposable VM, получающие NetVM от второй ProxyVM

В результате получится Пользователь > VPN > Tor > VPN > Интернет (VPN поверх Tor поверх VPN). Поэкспериментируйте самостоятельно. Qubes OS отлично подходит для таких задач.

### Настройка безопасного браузера в Qubes OS { #qubes-safe-browser }

См.: [Какой браузер использовать в Guest VM/Disposable VM](#guest-vm-browser-choice)

#### Fedora Disposable VM { #qubes-fedora-vm }

В меню Applications (слева вверху) выберите шаблон Fedora-36:

- Перейдите в Qube Settings

- Клонируйте ВМ и назовите её "fedora-36-brave" (в этом шаблоне ВМ будет Brave)

- Снова перейдите в меню Applications и выберите только что созданный клон

- Перейдите в Qube Settings

- Измените её сеть на ProxyVPN и нажмите Apply

- Запустите терминал из ВМ

Если вы хотите использовать Brave: следуйте инструкциям из [их документации](https://brave.com/linux/) <sup>[[Archive.org]](https://web.archive.org/web/https://brave.com/linux/)</sup> и выполните следующие команды:

```sudo dnf install dnf-plugins-core```

```sudo dnf config-manager --add-repo https://brave-browser-rpm-release.s3.brave.com/x86_64/```

```sudo rpm --import https://brave-browser-rpm-release.s3.brave.com/brave-core.asc```

```sudo dnf install brave-browser```

Вам также следует рассмотреть усиление защиты браузера; см. [Усиление защиты браузеров](#hardening-browsers)

#### Whonix Disposable VM { #qubes-whonix-vm }

Отредактируйте шаблон Whonix Disposable VM и следуйте инструкциям здесь: <https://www.whonix.org/wiki/Install_Software> <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Install_Software)</sup>

#### Дополнительные меры предосторожности для браузера { #qubes-browser-precautions }

- См.: [Усиление защиты браузеров](#hardening-browsers)

- См.: [Дополнительные меры предосторожности для браузера с включённым JavaScript](#browser-precautions-js)

### Настройка Android VM { #qubes-android-vm }

Иногда вам также нужно анонимно запускать мобильные приложения. Для этого можно настроить Android VM. Как и в других случаях, в идеале эта ВМ также должна находиться за Whonix Gateway для подключения к сети Tor. Но можно также настроить VPN поверх Tor поверх VPN.

Поскольку Android-x86 не работает с Qubes OS «хорошо» (по моему опыту), мы рекомендуем вместо него AnBox (<https://anbox.io/> <sup>[[Archive.org]](https://web.archive.org/web/https://anbox.io/)</sup>), который работает с Qubes OS «достаточно хорошо». Дополнительную информацию также можно найти по адресу <https://www.whonix.org/wiki/Anbox> <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Anbox)</sup>

#### Если вы можете использовать Tor { #qubes-android-tor }

Позже, при создании в настройках Qubes:

- Выберите Networking

- Измените на sys-whonix, чтобы поместить её за Whonix Gateway (поверх Tor).

#### Если вы не можете использовать Tor { #qubes-android-no-tor }

Просто используйте руководства без изменений. См. [Что делать, когда Tor и VPN недоступны?](#tor-vpn-not-possible).

**Установка**

По сути, следуйте приведённому здесь руководству:

- Щёлкните значок Applications (в левом верхнем углу)

- Щёлкните Create Qubes VM

- Задайте любое имя и метку: рекомендуем "Android"

- Выберите Type: Standalone Qube copied from a template

- Выберите Template: Debian-11

- Выберите Networking:

    - Выберите sys-whonix, если хотите использовать VPN поверх Tor / только Tor (рекомендуется)

    - Выберите sys-firewall, если хотите использовать Tor поверх VPN / без Tor или VPN / только VPN

- Запустите Qube и откройте терминал

Теперь вам нужно будет выполнить инструкции отсюда: <https://github.com/anbox/anbox-modules> <sup>[[Archive.org]](https://web.archive.org/web/https://github.com/anbox/anbox-modules)</sup>:

- Начните с клонирования репозитория AnBox Modules, выполнив:

    - ```git clone https://github.com/anbox/anbox-modules.git```

    - Перейдите в клонированный каталог

    - Выполните ```./INSTALL.sh``` (или следуйте инструкциям для ручной установки в руководстве)

- Перезагрузите машину

- Откройте новый терминал

- Установите Snap, выполнив:

    - ```sudo apt install snapd```

Теперь следуйте другому руководству, приведённому здесь: <https://github.com/anbox/anbox/blob/master/docs/install.md> <sup>[[Archive.org]](https://web.archive.org/web/https://github.com/anbox/anbox/blob/master/docs/install.md)</sup>:

- Установите AnBox, выполнив:

    - ```snap install --devmode --beta anbox```

- Чтобы позднее обновить AnBox, выполните:

    - ```snap refresh --beta --devmode anbox```

- Перезагрузите машину

- Снова откройте терминал и запустите эмулятор, выполнив:

    - ```anbox.appmgr```

Должен появиться интерфейс Android. Иногда он будет аварийно завершаться, и для работы его, возможно, придётся запустить дважды.

Если вы хотите устанавливать приложения в этот эмулятор:

- Установите ADB, выполнив:

    - ```sudo apt install android-tools-adb```

- Сначала запустите Anbox (выполните ```anbox.appmgr```)

- Получите APK любого приложения, которое хотите установить

- Теперь установите любой APK, выполнив:

    - ```adb install my-app.apk```

Вот и всё: теперь у вас должна быть Android Qube поверх Tor (или чего-либо другого), способная запускать практически любое приложение, которое можно загрузить через ADB. Пока это самый простой способ получить эмуляцию Android в Qubes OS.

### KeePassXC { #qubes-keepassxc }

Вам понадобится место для хранения данных (логинов/паролей, идентичностей и информации TOTP[^369]).

Для этой цели рекомендуется KeePassXC благодаря встроенной функции TOTP. Она позволяет создавать записи для аутентификации 2FA[^370] с помощью функции аутентификатора.

В контексте Qubes OS конфиденциальную информацию следует хранить в Qube vault:

- Сначала щёлкните значок Applications (слева вверху) и выберите Qube vault.

- Щёлкните Qubes Settings

- Выберите вкладку Applications

- В списке доступных приложений добавьте KeePassXC в список выбранных приложений.

Готово; теперь можете пропустить оставшуюся часть и перейти к разделу "[Создание анонимных онлайн-идентичностей](#creating-identities)".

### Руководство по установке ВМ на базе Windows в Qubes OS { #qubes-windows-vm-tutorial }

См. их руководство здесь: <https://github.com/Qubes-Community/Contents/blob/master/docs/os/windows/windows-tools41.md> <sup>[[Archive.org]](https://web.archive.org/web/https://github.com/Qubes-Community/Contents/blob/master/docs/os/windows/windows-tools41.md)</sup>

# Краткое примечание: корреляция и атрибуция { #correlation-vs-attribution }

**Корреляция** — это связь между двумя или более переменными либо **[атрибутами](https://www.digitalshadows.com/blog-and-research/cyber-attacks-the-challenge-of-attribution-and-response/)**. Как определяется атрибуция? Во время цифровой криминалистической экспертизы и реагирования на инциденты (DFIR) аналитики обычно ищут индикаторы компрометации (IoC) после событий, требующих от них действий. Эти индикаторы обычно состоят из IP-адресов, имён, баз данных; всё это может приписать отдельному человеку или группе определённый поведенческий «ярлык». Это называется атрибуцией. Один из принципов статистики гласит: «корреляция не подразумевает причинно-следственной связи». Это означает, что, хотя вы можете оставить определённые следы в определённых областях устройства или сети, они показывают лишь наличие действия, то есть не обязательно именно ваше присутствие. Они не показывают, кто вы; они лишь устанавливают, что нечто произошло и _кто-то_ сделал _что-то_.

Атрибуция необходима для доказательства вины или виновности и является главной причиной, по которой люди, использующие сеть Tor для доступа к даркнету, были скомпрометированы: они оставили следы, которые удалось связать с их настоящими личностями. Ваш IP-адрес может быть — но обычно не является — достаточно весомым индикатором для установления виновности. Это было показано во время печально известных кибератак NotPetya против США, которые позднее также были развёрнуты против Украины. Хотя Белый дом никогда не _говорил_, что это дело рук России, он приписал атаку российскому [(ГРУ)](https://www.reuters.com/article/us-britain-russia-gru-factbox/what-is-russias-gru-military-intelligence-agency-idUSKCN1MF1VK) — ведомству, непосредственно включающему российские киберподразделения для ведения отрицаемой войны[^311], которые в разведывательском сообществе (IC) нечасто называют «создателями шпионов».

_В чём суть_, спросите вы? Грубо говоря, это идеальный пример: хотя теперь несомненно, что NotPetya — дело рук российских киберопераций против зарубежных стран и правительств, он всё равно никогда не был официально приписан России, а лишь известной группе внутри России (неформально прозванной [Cozy Bear](https://wikiless.tiekoetter.com/wiki/Cozy_Bear)), что невозможно ни подтвердить, ни опровергнуть, учитывая её высокую обособленность в структуре российских вооружённых сил. Отчасти это также связано с усилиями по маскировке под обычную программу-вымогатель и с тем, что она регулярно использовала серверы взломанных зарубежных ресурсов, не связанных ни с Россией, ни с её внутренними сетями.

Всё это показывает, на что готовы пойти государственные субъекты. Возможно, вы этого не осознаёте, но иностранные правительства используют такие методы сокрытия, как рассмотренные в разделах этого руководства. Они регулярно используют Tor и VPN для сокрытия трафика; каждый день используют взломанные устройства и доступ к похищенному оборудованию для кибершпионажа, и это чрезвычайно затрудняет, если вообще не делает невозможной, атрибуцию с точки зрения судебного эксперта. Проблема корреляции тривиальна: её можно решить, просто используя инструменты сокрытия IP, такие как VPN и сеть Tor, но при этом всё ещё оставаться связанным со своим настоящим именем и IP-адресом из-за утечек данных или других факторов. Вас нельзя легко связать с вашими действиями, если вы тщательно следуете и применяете приведённые ниже методы и навыки.

# Создание анонимных онлайн-идентичностей { #creating-identities }

