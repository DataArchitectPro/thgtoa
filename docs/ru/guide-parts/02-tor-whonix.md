## Шаги для всех других маршрутов { #steps-other-routes }

### Получите выделенный ноутбук { #dedicated-laptop }

Ideally, you should get a dedicated laptop that will not be tied to you in any effortless way (ideally paid with cash anonymously and using the same precautions as previously mentioned for the phone and the SIM card). It is recommended but not mandatory. This guide will help you harden your laptop as much as possible to prevent data leaks through various means. There will be several lines of defense standing between your online identities and yourself which should prevent most adversaries from de-anonymizing you - besides state/global actors. It will take considerable resources.

This laptop should ideally be a clean, freshly installed laptop (running Windows, Linux, or macOS); which is clean of your normal day-to-day activities; and which is offline (never connected to your home network). In the case of a Windows laptop, and if you used it before such a clean install, it should also not be activated. Simply reinstall without a product key in the case that it came pre-activated. Specifically, in the case of MacBooks, it should never have been tied to your identity before in any means. So, buy secondhand with cash from an unknown stranger who does not know your identity.

Это должно смягчить некоторые будущие проблемы в случае утечек в Интернете (включая телеметрию с вашего OS или Apps), которые могут скомпрометировать любые уникальные идентификаторы ноутбука при его использовании (MAC Address, адрес Bluetooth и ключ продукта...). Но также, чтобы вас не отследили, если вам нужно утилизировать ноутбук.

Если вы раньше использовали этот ноутбук для разных целей (например, для повседневной деятельности), все его аппаратные идентификаторы, вероятно, известны и зарегистрированы Microsoft или Apple. Если позже какой-либо из этих идентификаторов будет скомпрометирован (вредоносным ПО, телеметрией, эксплойтами, человеческими ошибками ...), они могут привести к вам.

Ноутбук должен иметь не менее 250 ГБ дискового пространства ** не менее 6 ГБ (в идеале 8 ГБ или 16 ГБ)** RAM и должен иметь возможность запускать пару Virtual Machines одновременно. Он должен иметь работающую батарею, которая работает несколько часов. Если возможно, вы должны стремиться к чему-то с большим хранилищем (1 ТБ+), потому что нам понадобится как можно больше.

Этот ноутбук может иметь накопитель HDD (7200 об/мин) или SSD/NVMe. Обе возможности имеют свои преимущества и проблемы, которые будут подробно описаны позже.

Все будущие онлайн-шаги, выполняемые с помощью этого ноутбука, в идеале должны выполняться из безопасной сети, такой как Public Wi-Fi, в безопасном месте (см. [Find some safe places with decent public Wi-Fi](#safe-wifi)). Но сначала придется сделать несколько шагов в автономном режиме.

### Некоторые рекомендации для ноутбуков { #laptop-recommendations }

Мы настоятельно рекомендуем приобрести ноутбук «бизнес-класса» (то есть не потребительский/игровой ноутбук), если это возможно. Например, некоторые ThinkPad из Lenovo (мой личный фаворит).

Это связано с тем, что эти бизнес-ноутбуки обычно предлагают лучшие и более настраиваемые функции безопасности (особенно в настройках BIOS/UEFI) с более длительной поддержкой, чем большинство потребительских ноутбуков (ASUS, MSI, Gigabyte, Acer...). Интересные функции для поиска:

- Улучшенные пользовательские настройки Secure Boot* * (где вы можете выборочно управлять всеми ключами, а не просто использовать стандартные)**

- Пароли HDD/SSD в дополнение к паролям BIOS/UEFI.

- Ноутбуки AMD могут быть более интересными, так как некоторые из них предоставляют возможность отключить AMD PSP (эквивалент AMD IME) из настроек BIOS/UEFI по умолчанию. И, поскольку AFAIK, AMD PSP был проверен и, вопреки IME, не было обнаружено каких-либо «злых» функций. Однако, если вы собираетесь использовать Qubes OS Route, рассмотрите Intel CPUs, поскольку Qubes OS не поддерживает AMD со своей системой защиты от злобы.[^304][^305]

- Secure Wipe tools from the BIOS (особенно полезно для дисков SSD/NVMe, см. [BIOS/UEFI options to wipe disks in various Brands](#bios-disk-wipe-options)).

- Улучшенный контроль над отключением/включением выбранных периферийных устройств (порты USB, Wi-Fis, Bluetooth, камера, микрофон ...).

- Улучшенные функции безопасности благодаря виртуализации.

- Встроенные средства защиты от несанкционированного доступа.

- Более длительная поддержка обновлений BIOS/UEFI (и последующих обновлений безопасности BIOS/UEFI).

- Некоторые из них поддерживаются Libreboot

### Bios/UEFI/Настройки прошивки вашего ноутбука { #bios-uefi-settings }

#### PC { #bios-pc }

Доступ к этим настройкам можно получить через меню загрузки вашего ноутбука. Вот хороший учебник от HP, объясняющий все способы доступа к BIOS на различных компьютерах: <https://store.hp.com/us/en/tech-takes/how-to-enter-bios-setup-windows-pcs> <sup>[[Archive.org]](https://web.archive.org/web/https://store.hp.com/us/en/tech-takes/how-to-enter-bios-setup-windows-pcs)</sup>

Обычно доступ к нему можно получить, нажав определенную клавишу (F1, F2 или Del) при загрузке (перед OS).

Как только вы окажетесь там, вам нужно будет применить несколько рекомендуемых настроек:

- Полностью отключите Bluetooth, если можете.

- Отключите биометрию (сканеры отпечатков пальцев), если они у вас есть. Однако вы можете добавить биометрическую дополнительную проверку только для загрузки (перед загрузкой), но не для доступа к настройкам BIOS/UEFI.

- Отключите веб-камеру и микрофон, если это возможно.

- Включите пароль BIOS/UEFI и используйте длинную парольную фразу вместо пароля (если можете) и убедитесь, что этот пароль требуется для:

    - Доступ к настройкам BIOS/UEFI самостоятельно

    - Изменение порядка загрузки

    - Запуск/включение устройства

- Включите пароль HDD/SSD, если функция доступна. Эта функция добавит еще один пароль на сам HDD/SSD (не в прошивке BIOS/UEFI), который предотвратит использование этого HDD/SSD на другом компьютере без пароля. Обратите внимание, что эта функция также характерна для некоторых производителей и может потребовать специального программного обеспечения для разблокировки этого диска с совершенно другого компьютера.

- Предотвратите доступ к параметрам загрузки (порядок загрузки) без предоставления пароля BIOS/UEFI, если это возможно.

- Отключите USB/HDMI или любой другой порт (Ethernet, Firewire, SD-карта ...), если это возможно.

- Отключите Intel ME, если можете (шансы очень высоки, вы не можете).

- Отключите AMD PSP, если можете (эквивалент AMD IME, см. [Your CPU](#cpu))

- Отключите Secure Boot, если вы собираетесь использовать Qubes OS, так как они не поддерживают его из коробки. Держите его включенным, если вы собираетесь использовать Linux/Windows.[^306]

- Проверьте, есть ли на вашем ноутбуке BIOS опция безопасного стирания для вашего HDD/SSD, которая может быть удобной в случае необходимости.

Включите только тех, кто «нуждается в использовании», и отключите их снова после использования. Это может помочь смягчить некоторые атаки в случае, если ваш ноутбук заблокирован, но все еще включен или, если вам пришлось выключить его довольно быстро, и кто-то завладел им (эта тема будет объяснена позже в этом руководстве).

##### О безопасной загрузке { #secure-boot }

Итак, что такое Secure Boot? Короче говоря, это функция безопасности UEFI, предназначенная для предотвращения загрузки операционной системы, с которой загрузчик не был подписан определенными ключами, хранящимися в прошивке UEFI вашего ноутбука.[^307]

Когда операционная система (или загрузчик) поддерживает его, вы можете хранить ключи вашего загрузчика в прошивке UEFI, и это предотвратит загрузку любой несанкционированной операционной системы (например, OS USB или чего-либо подобного).[^308]

Настройки Secure Boot защищены паролем, который вы установили для доступа к настройкам BIOS/UEFI. Если у вас есть этот пароль, вы можете отключить Secure Boot и разрешить загрузку неподписанного OSes в вашей системе. Это может помочь смягчить некоторые атаки Злой горничной (объясняется далее в этом руководстве).

В большинстве случаев Secure Boot отключен по умолчанию или включен, но в режиме «Настройка», который позволит любой системе загрузиться. Для работы Secure Boot ваша операционная система должна будет его поддерживать, а затем подписать свой загрузчик и вставить эти ключи подписи в прошивку UEFI. После этого вам нужно будет перейти к настройкам BIOS/UEFI и сохранить эти нажатые клавиши из вашего OS и изменить Secure Boot из режима настройки в пользовательский режим (или в некоторых случаях в пользовательский режим).

После выполнения этого шага только операционные системы, из которых ваша прошивка UEFI может проверить целостность загрузчика, смогут загрузиться.

На большинстве ноутбуков некоторые ключи по умолчанию уже хранятся в настройках безопасной загрузки. Обычно это от самого производителя или некоторых компаний, таких как Microsoft. Таким образом, это означает, что по умолчанию всегда можно будет загрузить некоторые диски USB даже при безопасной загрузке. К ним относятся Windows, Fedora, Ubuntu, Mint, Debian, CentOS, OpenSUSE, Tails, Clonezilla и многие другие. Однако Secure Boot на данный момент вообще не поддерживается Qubes OS.

В некоторых ноутбуках вы можете управлять этими ключами и удалять те, которые вам не нужны, с помощью «пользовательского режима», чтобы авторизовать только загрузчик, который вы можете подписать самостоятельно, если хотите.

Итак, от чего Secure Boot защищает вас? Он защитит ваш ноутбук от загрузки неподписанных загрузчиков (провайдером OS), например, с помощью вредоносного ПО.

От чего Secure Boot **не** защищает вас?

- Secure Boot не шифрует ваш диск, и злоумышленник все равно может просто извлечь диск из вашего ноутбука и извлечь из него данные с помощью другой машины. Поэтому Secure Boot бесполезен без полного шифрования диска.

- Secure Boot не защищает вас от подписанного загрузчика, который будет скомпрометирован и подписан самим производителем (Microsoft, например, в случае Windows). Большинство основных дистрибутивов Linux подписаны в эти дни и будут загружаться с включенным Secure Boot.

- Secure Boot может иметь недостатки и эксплойты, как и любая другая система. Если вы используете старый ноутбук, который не получает новых обновлений BIOS/UEFI, их можно оставить без изменений.

Кроме того, возможно несколько атак на Secure Boot, как объясняется (подробно) в этих технических видео:

- Defcon 22, <https://www.youtube.com/watch?v=QDSlWa9xQuA> <sup>[[Invidious]](https://yewtu.be/watch?v=QDSlWa9xQuA)</sup>

- BlackHat 2016, <https://www.youtube.com/watch?v=0fZdL3ufVOI> <sup>[[Invidious]](https://yewtu.be/watch?v=0fZdL3ufVOI)</sup>

**Таким образом, он может быть полезен в качестве дополнительной меры против некоторых противников, но не всех. Secure Boot сам по себе не шифрует ваш жесткий диск. Это добавленный слой, но это все.**

**Я все еще рекомендую вам оставить его включенным, если вы можете.**

#### Mac { #bios-mac }

Найдите время, чтобы установить пароль прошивки в соответствии с руководством здесь: <https://support.apple.com/en-au/HT204455> <sup>[[Archive.org]](https://web.archive.org/web/https://support.apple.com/en-au/HT204455)</sup>

Вы также должны включить защиту от сброса пароля прошивки (доступно в Catalina) в соответствии с документацией здесь: <https://support.apple.com/en-gb/guide/security/sec28382c9ca/web> <sup>[[Archive.org]](https://web.archive.org/web/https://support.apple.com/en-gb/guide/security/sec28382c9ca/web)</sup>

Эта функция уменьшит вероятность того, что некоторые злоумышленники могут использовать аппаратные взломы для отключения/обхода пароля прошивки. Обратите внимание, что это также предотвратит доступ Apple к прошивке в случае ремонта.

### Физически защитите свой ноутбук { #tamper-protection }

В какой-то момент вы неизбежно оставите этот ноутбук в покое. Вы не будете спать с ним и носить его повсюду каждый день. Вы должны сделать так, чтобы никто не мог вмешаться, не заметив этого. Это в основном полезно против некоторых ограниченных противников, которые не будут использовать гаечный ключ на 5 $ против вас.[^11]

Важно знать, что некоторым специалистам тривиально легко установить в ноутбук регистратор ключей или просто сделать клонированную копию жесткого диска, которая впоследствии может позволить им обнаружить наличие в нем зашифрованных данных с помощью криминалистических методов (подробнее об этом позже).

Вот хороший дешевый способ сделать ваш ноутбук защищенным от несанкционированного доступа с помощью лака для ногтей (с блестками) <https://mullvad.net/en/help/how-tamper-protect-laptop/><sup>[[Archive.org]](https://web.archive.org/web/https://mullvad.net/en/help/how-tamper-protect-laptop/)</sup> (с фотографиями).[^309]

While this is a good cheap method, it could also raise suspicions as it is quite "noticeable" and might just reveal that you "have something to hide". So, there are more subtle ways of achieving the same result. You could also for instance make a close-up macro photography of the back screws of your laptop or just use a small amount of candle wax within one of the screws that could just look like usual dirt. You could then check for tampering by comparing the photographs of the screws with new ones. Their orientation might have changed a bit if your adversary was not careful enough (Tightening them exactly the same way they were before). Or the wax within the bottom of a screw head might have been damaged compared to before.

![image20](../media/image20.png)

![image21](../media/image21.png)

Те же методы можно использовать с портами USB, где вы можете просто поместить небольшое количество свечного воска в штекер, который будет поврежден, вставив в него ключ USB.

В более рискованных условиях перед регулярным использованием ноутбука проверьте его на предмет несанкционированного доступа.

## Маршрут Whonix { #whonix-route }

**Примечание о версии Whonix**: Whonix был обновлен с версии 17 до 18 (Whonix 18.1.4.x на момент написания статьи) с поддержкой автоматического обновления выпуска. См. [Обновление до Whonix 18](# qubes-whonix18) для пути обновления, если вы в настоящее время используете Whonix 17.x или более ранние версии.

### Выбираем ваш Host OS { #host-os-choice }

Этот маршрут будет широко использовать Virtual Machines, им потребуется хост OS для запуска программного обеспечения виртуализации. В этой части руководства есть три рекомендуемых варианта:[^310]

- Ваше распределение Linux по выбору (за исключением Qubes OS)

- Windows 10/11 (предпочтительно Home edition в связи с отсутствием Bitlocker)

- macOS (Каталина или выше до Монтерея)

Кроме того, высока вероятность того, что ваш Mac привязан или был привязан к учетной записи Apple (во время покупки или после входа в систему), и поэтому его уникальные аппаратные идентификаторы могут привести к вам в случае утечки аппаратных идентификаторов.

Linux is also not necessarily the best choice for anonymity depending on your threat model. This is because using Windows will allow us to **conveniently** use Plausible Deniability (aka Deniable Encryption) easily at the OS level. Windows is also unfortunately at the same time a privacy nightmare but is the only easy to set up option for using OS-wide plausible deniability. Windows telemetry and telemetry blocking are also widely documented which should mitigate many issues.[^311][^312][^313]

**Итак, что такое правдоподобное отрицание?** Вы можете сотрудничать со злоумышленником, запрашивающим доступ к вашему устройству/данным, не раскрывая свой истинный секрет. Все это с помощью Deniable Encryption.[^314]

Мягкий законный злоумышленник может запросить пароль от вашего зашифрованного ноутбука. Сначала вы могли отказаться выдавать какой-либо пароль (используя свое «право хранить молчание», «право не свидетельствовать против себя»), но некоторые страны применяют законы ', чтобы освободить это от таких прав (потому что террористы и «думают о детях»). В этом случае вам, возможно, придется раскрыть пароль или вам грозит тюремное заключение за неуважение к суду. Именно здесь вступает в игру правдоподобное отрицание.[^315][^316]

You could then reveal a password, but that password will only give access to "plausible data" (a decoy OS). The forensics will be well aware that it is possible for you to have hidden data but should not be able to prove this **(if you do this right)**. You will have cooperated, and the investigators will have access to something but not what you actually want to hide. Since the burden of proof should lie on their side, they will have no options but to believe you unless they have proof that you have hidden data.

Эту функцию можно использовать на уровне OS (правдоподобный OS и скрытый OS) или на уровне файлов, где у вас будет зашифрованный файловый контейнер (аналогичный ZIP-файлу), где будут отображаться разные файлы в зависимости от используемого вами пароля шифрования.

This also means you could set up your own advanced "plausible deniability" setup using any Host OS by storing for instance Virtual Machines on a Veracrypt hidden volume container (be careful of traces in the Host OS tho that would need to be cleaned if the host OS is persistent, see [Some additional measures against forensics](#anti-forensics) section later). There is a project for achieving this within Tails (<https://github.com/aforensics/HiddenVM> <sup>[[Archive.org]](https://web.archive.org/web/https://github.com/aforensics/HiddenVM)</sup>) which would make your Host OS non-persistent and use plausible deniability within Tails.

In the case of Windows, plausible deniability is also the reason you should ideally have Windows 10/11 Home (and not Pro). This is because Windows 10/11 Pro natively offers a full-disk encryption system (Bitlocker) where Windows 10/11 Home offers no full-disk encryption at all. You will later use third-party open-source software for encryption that will allow full-disk encryption on Windows 10/11 Home. This will give you a good (plausible) excuse to use this software. While using this software on Windows 10/11 Pro would be suspicious.[^317]

**Примечание о Linux:** Итак, как насчет Linux и правдоподобного отрицания? Да, с Linux также можно добиться правдоподобного отрицания. Более подробная информация приведена в разделе Linux Host OS позже.

К сожалению, шифрование - это не магия, и есть некоторые риски:

#### Угрозы с шифрованием { #encryption-threats }

**Атака гаечным ключом на 5 $ **

Помните, что шифрование с правдоподобным отрицанием или без него не является серебряной пулей и будет малопригодным в случае пыток. На самом деле, в зависимости от того, кем будет ваш противник (ваша модель угроз), возможно, было бы разумно вообще не использовать Veracrypt (ранее TrueCrypt), как показано на этой демонстрации: <https://defuse.ca/truecrypt-plausible-deniability-useless-by-game-theory.htm> <sup>[[Archive.org]](https://web.archive.org/web/https://defuse.ca/truecrypt-plausible-deniability-useless-by-game-theory.htm)</sup>

Правдоподобное отрицание эффективно только против мягких законных противников, которые не будут прибегать к физическим средствам. **По возможности избегайте использования программного обеспечения, допускающего правдоподобное отрицание (например, Veracrypt), если ваша модель угроз включает в себя жестких противников. Таким образом, пользователи Windows должны в этом случае установить Windows Pro в качестве Host OS и вместо этого использовать Bitlocker.**

См. <https://en.wikipedia.org/wiki/Rubber-hose_cryptanalysis><sup>[[Wikiless]](https://wikiless.tiekoetter.com/wiki/Rubber-hose_cryptanalysis)</sup> <sup>[[Archive.org]](https://web.archive.org/web/https://en.wikipedia.org/wiki/Rubber-hose_cryptanalysis)</sup>

##### Атака злой горничной { #evil-maid-attack }

Evil Maid Attacks are conducted when someone tampers with your laptop while you are away. To install to clone your hard drive, install malware or a key logger. If they can clone your hard drive, they can compare one image of your hard drive at the time they took it while you were away with the hard drive when they seize it from you. If you used the laptop again in between, forensics examiners might be able to prove the existence of the hidden data by looking at the variations between the two images in what should be an empty/unused space. This could lead to compelling evidence of the existence of hidden data. If they install a key logger or malware within your laptop (software or hardware), they will be able to simply get the password from you for later use when they seize it. Such attacks can be done at your home, your hotel, a border crossing, or anywhere you leave your devices unattended.[^318]

Вы можете смягчить эту атаку, выполнив следующие действия (как рекомендовано ранее):

- Имейте базовую защиту от несанкционированного доступа (как объяснялось ранее), чтобы предотвратить физический доступ к внутренним устройствам ноутбука без вашего ведома. Это предотвратит клонирование ваших дисков и установку физического регистратора ключей без вашего ведома.

- Отключите все порты USB (как объяснялось ранее) в защищенном паролем BIOS/UEFI. Опять же, они не смогут включить их (без физического доступа к материнской плате для сброса BIOS), чтобы загрузить устройство USB, которое может клонировать ваш жесткий диск или установить вредоносное ПО на основе программного обеспечения, которое может выступать в качестве регистратора ключей.

- Настройте пароли BIOS/UEFI/прошивки, чтобы предотвратить несанкционированную загрузку несанкционированного устройства.

- Некоторые программы OSes и шифрования имеют [Anti Evil Maid (AEM)](#qubes-aem) защиту, которую можно включить. Это относится к Windows/Veracrypt и QubeOS (только на Intel CPUs).

##### Атака холодным ботинком { #cold-boot-attack }

Атаки холодной загрузки сложнее, чем атака Злой горничной, но могут быть частью атаки Злой горничной, поскольку для этого требуется, чтобы противник завладел вашим ноутбуком, пока вы активно используете свое устройство или вскоре после этого.[^319]

The idea is rather simple, as shown in this video, an adversary could theoretically quickly boot your device on a special USB key that would copy the content of the RAM (the memory) of the device after you shut it down. If the USB ports are disabled or if they feel like they need more time, they could open it and "cool down" the memory using a spray or other chemicals (liquid nitrogen for instance) preventing the memory from decaying. They could then be able to copy its content for analysis. This memory dump could contain the key to decrypt your device. You will later apply a few principles to mitigate these.[^320]

В случае правдоподобного отрицания было проведено несколько криминалистических исследований о техническом доказательстве наличия скрытых данных с помощью простой криминалистической экспертизы (без атаки Cold Boot/Evil Maid), но они были оспорены другими исследованиями и сопровождающим Veracrypt, поэтому мы пока не будем слишком беспокоиться о них.[^321][^322][^323]

Те же меры, которые используются для смягчения атак Evil Maid, должны быть приняты для атак Cold Boot с некоторыми дополнительными:

- Если ваше программное обеспечение OS или Encryption позволяет это, вам также следует рассмотреть возможность шифрования ключей в RAM (это возможно с Windows/Veracrypt и будет объяснено позже). Снова см. <https://sourceforge.net/p/veracrypt/discussion/technical/thread/3961542951/> <sup>[[Archive.org]](https://web.archive.org/web/https://sourceforge.net/p/veracrypt/discussion/technical/thread/3961542951/)</sup>

- Включите опцию Протирать ключи из памяти, если устройство вставлено в Veracrypt.

- Вы должны ограничить использование режима ожидания Sleep и вместо этого использовать Shutdown или Hibernate, чтобы ключи шифрования не оставались в RAM, когда ваш компьютер переходит в спящий режим. Это связано с тем, что сон будет поддерживать силу в вашей памяти для более быстрого возобновления вашей деятельности. Только спящий режим и выключение фактически очистят ключ из памяти.[^324]

См. также [Защита от атаки холодным ботинком](https://www.whonix.org/wiki/Cold_Boot_Attack_Defense) <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Cold_Boot_Attack_Defense)</sup> и [Защита от физических атак](https://www.whonix.org/wiki/Protection_Against_Physical_Attacks) <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Protection_Against_Physical_Attacks)</sup>.

Вот также некоторые интересные инструменты, которые следует учитывать пользователям Linux для защиты от них:

- <https://github.com/0xPoly/Centry> <sup>[[Archive.org]](https://web.archive.org/web/https://github.com/0xPoly/Centry)</sup>(к сожалению, не поддерживается)

- <https://github.com/hephaest0s/usbkill> <sup>[[Archive.org]](https://web.archive.org/web/https://github.com/hephaest0s/usbkill)</sup> (к сожалению, также не поддерживается)

- <https://github.com/Lvl4Sword/Killer> <sup>[[Archive.org]](https://web.archive.org/web/https://github.com/Lvl4Sword/Killer)</sup>

- <https://askubuntu.com/questions/153245/how-to-wipe-ram-on-shutdown-prevent-cold-boot-attacks> <sup>[[Archive.org]](https://web.archive.org/web/https://askubuntu.com/questions/153245/how-to-wipe-ram-on-shutdown-prevent-cold-boot-attacks)</sup>

- (Qubes OS, только Intel CPU) <https://github.com/QubesOS/qubes-antievilmaid> <sup>[[Archive.org]](https://web.archive.org/web/https://github.com/QubesOS/qubes-antievilmaid)</sup>

##### О Sleep, Hibernation и Shutdown { #sleep-hibernation-shutdown }

If you want better security, you should shut down your laptop completely every time you leave it unattended or close the lid. This should clean and/or release the RAM and provide mitigations against cold boot attacks. However, this can be a bit inconvenient as you will have to reboot completely and type in a ton of passwords into various apps. Restart various VMs and other apps. So instead, you could also use hibernation (not supported on Qubes OS). Since the whole disk is encrypted, hibernation in itself should not pose a large security risk but will still shut down your laptop and clear the memory while allowing you to conveniently resume your work afterward. **What you should never do is using the standard sleep feature which will keep your computer on, and the memory powered. This is an attack vector against evil-maid and cold-boot attacks discussed earlier. This is because your powered-on memory holds the encryption keys to your disk (encrypted or not) and could then be accessed by a skilled adversary.**

В этом руководстве будет приведено руководство о том, как включить спящий режим на различных хостах OSes (кроме Qubes OS), если вы не хотите завершать работу каждый раз.

##### Локальные утечки данных (следы) и криминалистическая экспертиза { #host-local-data-leaks }

Как упоминалось вкратце ранее, это утечки данных и трассировки из вашей операционной системы и приложений при выполнении каких-либо действий на вашем компьютере. Они в основном применяются к зашифрованным файловым контейнерам (с правдоподобным отрицанием или без него), чем шифрование в масштабе OS. Такие утечки менее «важны», если весь ваш OS зашифрован (если вы не обязаны раскрывать пароль).

Допустим, у вас есть ключ Veracrypt, зашифрованный USB, с включенным правдоподобным отрицанием. В зависимости от пароля, который вы используете при монтировании ключа USB, он откроет папку-приманку или конфиденциальную папку. В этих папках у вас будут документы/данные-приманки в папке-приманке и конфиденциальные документы/данные в конфиденциальной папке.

Во всех случаях вы (скорее всего) откроете эти папки с помощью Windows Explorer, macOS Finder или любой другой утилиты и сделаете все, что планировали. Возможно, вы отредактируете документ в конфиденциальной папке. Возможно, вы будете искать документ в папке. Возможно, вы удалите его или посмотрите конфиденциальное видео с помощью VLC.

Ну, все эти Apps и ваша операционная система могут хранить журналы и следы этого использования. Это может включать полный путь к папке/файлам/дискам, время доступа к ним, временные кэши этих файлов, «последние» списки в каждом приложении, систему индексирования файлов, которая может индексировать диск, и даже эскизы, которые могут быть сгенерированы

Вот несколько примеров таких утечек:

###### Windows { #host-local-leaks-windows }

- Windows ShellBags, которые хранятся в реестре Windows, тихо сохраняя различные истории доступных томов/файлов/папок.[^325]

- Windows Индексирование следов файлов, присутствующих в папке пользователя по умолчанию.[^326]

- Последние списки (aka Jump Lists) в Windows и различных приложениях, хранящих следы недавно просмотренных документов.[^327]

- Еще много следов в различных журналах, пожалуйста, посмотрите этот удобный интересный плакат для получения дополнительной информации: <https://www.sans.org/security-resources/posters/windows-forensic-analysis/170/download><sup>[[Archive.org]](https://web.archive.org/web/https://www.sans.org/security-resources/posters/windows-forensic-analysis/170/download)</sup>

###### macOS { #host-local-leaks-macos }

- Gatekeeper и XProtect отслеживают историю загрузок в локальной базе данных и атрибуты файлов.[^328]

- Индексация Spotlight

- Недавние списки в различных приложениях, содержащие следы недавно просмотренных документов.

- Временные папки, содержащие различные следы использования App и использования Документов.

- Журналы macOS

###### Linux { #host-local-leaks-linux }

- Индексация Tracker

- Bash История

- Журналы USB

- Недавние списки в различных приложениях, содержащие следы недавно просмотренных документов.

- Журналы Linux

Эксперты могут использовать все эти утечки (см. [Local Data Leaks and Forensics](# local-data-leaks)), чтобы доказать существование скрытых данных и победить ваши попытки использовать правдоподобное отрицание и узнать о ваших различных конфиденциальных действиях.

Поэтому важно применить различные шаги, чтобы не допустить этого, предотвращая и очищая эти утечки/следы и, что более важно, используя шифрование всего диска, виртуализацию и разделение.

Криминалисты не могут извлечь локальные утечки данных из OS, к которому они не могут получить доступ. И вы сможете очистить большинство этих следов, стерев диск или надежно стерев виртуальные машины (что не так просто, как вы думаете на дисках SSD).

Тем не менее, некоторые методы очистки будут рассмотрены в разделе «Накрыть свои следы» этого руководства в самом конце.

##### Онлайн-утечки данных { #host-online-data-leaks }

Независимо от того, используете ли вы простое шифрование или правдоподобное шифрование отрицания. Даже если вы заметали следы на самом компьютере. По-прежнему существует риск утечки данных в Интернете, которая может выявить наличие скрытых данных.

**Телеметрия - ваш враг**. Как объяснялось ранее в этом руководстве, телеметрия операционных систем, а также Apps может отправлять ошеломляющее количество личной информации в Интернете.

В случае Windows эти данные могут, например, использоваться для доказательства существования скрытого OS/ Volume на компьютере и будут легко доступны на Microsoft. Поэтому крайне важно отключать и блокировать телеметрию всеми имеющимися в вашем распоряжении средствами. Независимо от того, какой OS вы используете.

#### Заключение { #host-os-conclusion }

Вы никогда не должны выполнять конфиденциальные действия из незашифрованной системы. И даже если он зашифрован, вы никогда не должны проводить конфиденциальные действия из самого Host OS. Вместо этого вы должны использовать VM, чтобы иметь возможность эффективно изолировать и разделять свои действия и предотвращать локальные утечки данных.

Если у вас мало знаний о Linux или вы хотите использовать правдоподобное отрицание OS, мы рекомендуем перейти на Windows (или вернуться к [маршруту Tails](# tails-route)) для удобства. Это руководство поможет вам максимально упрочить его, чтобы предотвратить утечки. Это руководство также поможет вам максимально упрочить macOS и Linux, чтобы предотвратить подобные утечки.

Если вы не заинтересованы в правдоподобном отрицании OS и хотите научиться использовать Linux, мы настоятельно рекомендуем выбрать Linux или маршрут Qubes OS, если ваше оборудование позволяет это.

**Во всех случаях хост OS никогда не должен использоваться для проведения конфиденциальных мероприятий напрямую. Хост OS будет использоваться только для подключения к общедоступной точке доступа Wi-Fi. Он останется неиспользованным, пока вы проводите конфиденциальные мероприятия, и в идеале не должен использоваться для какой-либо повседневной деятельности.**

Читайте также **<https://www.whonix.org/wiki/Full_Disk_Encryption#Encrypting_Whonix_VMs>**<sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Full_Disk_Encryption)</sup>

### Linux Host OS { #linux-host-os }

Как упоминалось ранее, мы не рекомендуем использовать ваш ежедневный ноутбук для конфиденциальных действий. Или, по крайней мере, мы не рекомендуем использовать для них OS. Это может привести к нежелательным утечкам данных, которые могут быть использованы для деанонимизации. Если у вас есть специальный ноутбук для этого, вы должны переустановить свежий чистый OS. Если вы не хотите стирать свой ноутбук и начинать все сначала, вам следует рассмотреть маршрут Tails или действовать на свой страх и риск.

Я также рекомендую выполнить первоначальную установку полностью в автономном режиме, чтобы избежать утечки данных.

Вы всегда должны помнить, что, несмотря на репутацию, основные дистрибутивы Linux (например, Ubuntu) не обязательно лучше защищены, чем другие системы, такие как macOS и Windows. См. эту ссылку, чтобы понять, почему <https://madaidans-insecurities.github.io/linux.html><sup>[[Archive.org]](https://web.archive.org/web/https://madaidans-insecurities.github.io/linux.html)</sup>.

#### Полное шифрование диска { #linux-fde }

Здесь есть два маршрута с дистрибутивами на основе Ubuntu или Debian:

- Использование LUKS:

    - Без правдоподобного отрицания:

        + (Рекомендуется и легко) Шифровать в процессе установки: <https://ubuntu.com/tutorials/install-ubuntu-desktop> <sup>[[Archive.org]](https://web.archive.org/web/https://ubuntu.com/tutorials/install-ubuntu-desktop)</sup>

            * Этот процесс требует полного стирания всего накопителя (чистая установка).

            * Просто проверьте «Шифрование новой установки Ubuntu для обеспечения безопасности»

        + (Утомительно, но возможно) Шифровать после установки: <https://help.ubuntu.com/community/ManualFullSystemEncryption> <sup>[[Archive.org]](https://web.archive.org/web/https://help.ubuntu.com/community/ManualFullSystemEncryption)</sup>

    - С правдоподобным отрицанием: см. следующий раздел [The Detached Headers Way]

- Использование Veracrypt:

    - С правдоподобным отрицанием или без него: см. следующий раздел [Путь Veracrypt]

Для других дистрибутивов вам придется документировать себя, но, скорее всего, это будет похоже. Шифрование во время установки намного проще в контексте этого руководства.

#### Примечание о правдоподобном отрицании на Linux { #linux-deniability-note }

Существует несколько способов достижения правдоподобного отрицания на Linux, и это возможно. Вот более подробная информация о некоторых способах, которые мы рекомендуем. Все эти варианты требуют некоторого более высокого уровня навыков использования Linux.[^329]

##### The Detached Headers Way { #detached-headers }

Хотя это руководство еще не поддерживается, можно достичь формы отрицания на Linux, используя LUKS, используя отсоединенные заголовки LUKS. На данный момент мы перенаправим вас на эту страницу для получения дополнительной информации: <https://wiki.archlinux.org/title/Dm-crypt/Specialties#Encrypted_system_using_a_detached_LUKS_header> <sup>[[Archive.org]](https://web.archive.org/web/https://wiki.archlinux.org/title/Dm-crypt/Specialties#Encrypted_system_using_a_detached_LUKS_header)</sup>

##### Veracrypt Way { #veracrypt-way }

Технически возможно не только использовать Veracrypt, но и добиться правдоподобного отрицания на Linux Host OS, используя Veracrypt для системного полнодискового шифрования (вместо LUKS). Это не поддерживается Veracrypt (системное шифрование поддерживается только на Windows) и требует некоторой обработки с различными командами. Это не рекомендуется для неквалифицированных пользователей и должно использоваться только на свой страх и риск.

Шаги для достижения этого еще не включены в это руководство, но их можно найти здесь: <http://dreadytofatroptsdj6io7l3xptbet6onoyno2yv7jicoxknyazubrad.onion/post/5779e55aae7fc06e4758> (это адрес .onion и требует Tor Browser).

#### Отклонить/отключить любую телеметрию { #linux-disable-telemetry }

- Во время установки просто убедитесь, что вы не разрешаете сбор данных при появлении запроса.

- Если вы не уверены, просто убедитесь, что вы не включили телеметрию, и при необходимости следуйте этому руководству <https://vitux.com/how-to-force-ubuntu-to-stop-collecting-your-data-from-your-pc/> <sup>[[Archive.org]](https://web.archive.org/web/https://vitux.com/how-to-force-ubuntu-to-stop-collecting-your-data-from-your-pc/)</sup>

- Любой другой дистрибутив: вам нужно будет задокументировать себя и узнать, как отключить телеметрию.

#### Отключите все ненужное { #linux-disable-unnecessary }

- Отключите Bluetooth, если он включен, следуя этому руководству<https://www.addictivetips.com/ubuntu-linux-tips/disable-bluetooth-in-ubuntu/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.addictivetips.com/ubuntu-linux-tips/disable-bluetooth-in-ubuntu/)</sup> или выполнив следующую команду:

    - ```sudo systemctl disable bluetooth.service --force```

- Отключите индексирование, если оно включено по умолчанию (Ubuntu >19.04), следуя этому руководству <https://www.linuxuprising.com/2019/07/how-to-completely-disable-tracker.html><sup>[[Archive.org]](https://web.archive.org/web/https://www.linuxuprising.com/2019/07/how-to-completely-disable-tracker.html)</sup> или выполнив следующие команды:

    - ```sudo systemctl --user mask tracker-store.service tracker-miner-fs.service tracker-miner-rss.service tracker-extract.service tracker-miner-apps.service tracker-writeback.service```

        + Вы можете спокойно игнорировать любую ошибку, если там написано, что какая-то услуга не существует

    - ```sudo tracker reset -hard```

##### Гибернация { #linux-hibernation }

As explained previously, you should not use the sleep features but shut down or hibernate your laptop to mitigate some evil-maid and cold-boot attacks. Unfortunately, this feature is disabled by default on many Linux distros including Ubuntu. It is possible to enable it, but it might not work as expected. Follow this information at your own risk. If you do not want to do this, you should never use the sleep function and power off instead (and set the lid closing behavior to power off instead of sleep).

Следуйте одному из этих руководств, чтобы включить Hibernate:

- <https://www.how2shout.com/linux/how-to-hibernate-ubuntu-20-04-lts-focal-fossa/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.how2shout.com/linux/how-to-hibernate-ubuntu-20-04-lts-focal-fossa/)</sup>

- <http://www.lorenzobettini.it/2020/07/enabling-hibernation-on-ubuntu-20-04/> <sup>[[Archive.org]](https://web.archive.org/web/http://www.lorenzobettini.it/2020/07/enabling-hibernation-on-ubuntu-20-04/)</sup>

- <https://blog.ivansmirnov.name/how-to-set-up-hibernate-on-ubuntu-20-04/> <sup>[[Archive.org]](https://web.archive.org/web/20211011215449/https://blog.ivansmirnov.name/how-to-set-up-hibernate-on-ubuntu-20-04/)</sup>

После включения Hibernate измените поведение так, чтобы ваш ноутбук впадал в спящий режим при закрытии крышки, следуя этому уроку для Ubuntu 20.04 <http://ubuntuhandbook.org/index.php/2020/05/lid-close-behavior-ubuntu-20-04/> <sup>[[Archive.org]](https://web.archive.org/web/http://ubuntuhandbook.org/index.php/2020/05/lid-close-behavior-ubuntu-20-04/)</sup> и этому уроку для Ubuntu 18.04 <https://tipsonubuntu.com/2018/04/28/change-lid-close-action-ubuntu-18-04-lts/> <sup>[[Archive.org]](https://web.archive.org/web/https://tipsonubuntu.com/2018/04/28/change-lid-close-action-ubuntu-18-04-lts/)</sup>. Учебника по Ubuntu 21.04 или 21.10 пока нет, но вышеизложенное для 20.04, вероятно, тоже должно сработать.

К сожалению, это не очистит ключ из памяти непосредственно при спящем режиме. Чтобы избежать этого ценой некоторой производительности, вы можете рассмотреть возможность шифрования файла подкачки, следуя этому руководству: <https://help.ubuntu.com/community/EnableHibernateWithEncryptedSwap> <sup>[[Archive.org]](https://web.archive.org/web/https://help.ubuntu.com/community/EnableHibernateWithEncryptedSwap)</sup>

Эти настройки должны смягчать атаки холодной загрузки, если вы можете достаточно быстро перейти в спящий режим.

#### Включить рандомизацию адресов MAC { #linux-mac-randomization }

- Для Ubuntu выполните следующие действия <https://help.ubuntu.com/community/AnonymizingNetworkMACAddresses> <sup>[[Archive.org]](https://web.archive.org/web/https://help.ubuntu.com/community/AnonymizingNetworkMACAddresses)</sup>.

- Рассмотрим это руководство, которое все еще должно работать: <https://josh.works/shell-script-basics-change-mac-address><sup>[[Archive.org]](https://web.archive.org/web/https://josh.works/shell-script-basics-change-mac-address)</sup>

#### Закалка Linux { #hardening-linux }

В качестве легкого введения для новых пользователей Linux рассмотрим <https://www.youtube.com/watch?v=Sa0KqbpLye4> <sup>[[Invidious]](https://yewtu.be/watch?v=Sa0KqbpLye4)</sup>

Более подробные и расширенные варианты см. в разделе:

- Это отличное руководство: <https://madaidans-insecurities.github.io/guides/linux-hardening.html> <sup>[[Archive.org]](https://web.archive.org/web/https://madaidans-insecurities.github.io/guides/linux-hardening.html)</sup>

- Этот отличный вики-ресурс: <https://wiki.archlinux.org/title/Security> <sup>[[Archive.org]](https://web.archive.org/web/https://wiki.archlinux.org/title/Security)</sup>

- Эти отличные скрипты основаны на руководстве и вики выше: <https://codeberg.org/SalamanderSecurity/PARSEC> <sup>[[Archive.org]](https://web.archive.org/web/https://codeberg.org/SalamanderSecurity/PARSEC)</sup>

- Эти инструменты, которые могут помочь вам укрепить ваш Linux Kernel:

    - Lynis: <https://github.com/CISOfy/lynis>

    - Kconfig-hardened-check: <https://github.com/a13xp0p0v/kconfig-hardened-check>

- Рассмотрите возможность установки Safing Portmaster из <https://safing.io/portmaster/><sup>[[Archive.org]](https://web.archive.org/web/https://safing.io/portmaster/)</sup>* *(Предупреждение: могут возникнуть проблемы с некоторыми клиентами VPN. См.:<https://docs.safing.io/portmaster/install/status/vpn-compatibility>* *<sup>[[Archive.org]](https://web.archive.org/web/https://docs.safing.io/portmaster/install/status/vpn-compatibility)</sup>

- Рассмотрите возможность использования KickSecure при использовании Debian: [Kicksecure](https://www.whonix.org/wiki/Kicksecure) <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Kicksecure)</sup>

- Эта интересная статья: <http://0pointer.net/blog/authenticated-boot-and-disk-encryption-on-linux.html> <sup>[[Archive.org]](https://web.archive.org/web/http://0pointer.net/blog/authenticated-boot-and-disk-encryption-on-linux.html)</sup>

#### Настройка безопасного браузера { #linux-safe-browser }

См. [Safe Browser on the Host OS](#safe-browser-host-os)

### macOS Host OS { #macos-host-os }

**Примечание: чипы Mac M1/M2 теперь поддерживаются изначально или, если вы хотите использовать коммерческие инструменты, такие как VMWare Fusion или Parallels Desktop, но они не рассматриваются в этом руководстве. Ищите эту информацию самостоятельно.**

Как упоминалось ранее, мы не рекомендуем использовать ваш ежедневный ноутбук для конфиденциальных действий. Или, по крайней мере, мы не рекомендуем использовать для них OS. Это может привести к нежелательным утечкам данных, которые могут быть использованы для деанонимизации. Если у вас есть специальный ноутбук для этого, вы должны переустановить свежий чистый OS. Если вы не хотите стирать свой ноутбук и начинать все сначала, вам следует рассмотреть [маршрут Tails](# tails-route) или действовать на свой страх и риск.

Мы также рекомендуем выполнить первоначальную установку полностью в автономном режиме, чтобы избежать утечки данных.

**Никогда не входите в свою учетную запись Apple с помощью этого Mac.**

#### Во время установки { #macos-install }

- Не подключаться

- Отключите все запросы на совместное использование данных, включая службы определения местоположения, при появлении запроса

- Не входите в систему с помощью Apple

- Не включать Siri

#### Закалка macOS { #hardening-macos }

В качестве легкого введения для новых пользователей macOS рассмотрим <https://www.youtube.com/watch?v=lFx5icuE6Io> <sup>[[Invidious]](https://yewtu.be/watch?v=lFx5icuE6Io)</sup>

Теперь, чтобы углубиться в обеспечение и укрепление вашего macOS, мы рекомендуем прочитать это руководство, которое охватывает многие вопросы: <https://www.bejarano.io/hardening-macos/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.bejarano.io/hardening-macos/)</sup>

Вот основные шаги, которые вы должны предпринять после установки в автономном режиме:

##### Включить пароль прошивки с опцией «disable-reset-capability» { #macos-firmware-password }

Во-первых, вы должны установить пароль прошивки, следуя этому руководству от Apple: <https://support.apple.com/en-us/HT204455> <sup>[[Archive.org]](https://web.archive.org/web/https://support.apple.com/en-us/HT204455)</sup>

К сожалению, некоторые атаки все еще возможны, и злоумышленник может отключить этот пароль, поэтому вы также должны следовать этому руководству, чтобы предотвратить отключение пароля прошивки от кого-либо, включая Apple: <https://support.apple.com/en-gb/guide/security/sec28382c9ca/web><sup>[[Archive.org]](https://web.archive.org/web/https://support.apple.com/en-gb/guide/security/sec28382c9ca/web)</sup>

##### Включить спящий режим вместо сна { #macos-hibernation }

Again, this is to prevent some cold-boot and evil-maid attacks by powering down your RAM and cleaning the encryption key when you close the lid. You should always either hibernate or shut down. On macOS, the hibernate feature even has a special option to specifically clear the encryption key from memory when hibernating (while you might have to wait for the memory to decay on other Operating Systems). Once again there are no easy options to do this within the settings so instead, we will have to do this by running a few commands to enable hibernation:

- Открыть терминал

- Запуск: ```sudo pmset -a destroyfvkeyonstandby 1```

    - Эта команда даст команду macOS уничтожить ключ Filevault на Standby (Sleep)

- Запуск: ```sudo pmset -a hibernatemode 25```

    - Эта команда проинструктирует macOS отключать память во время сна, а не выполнять гибридную спячку, которая поддерживает питание памяти. Это приведет к более медленным пробуждениям, но увеличит время автономной работы.

Теперь, когда вы закрываете крышку вашего MacBook, он должен впадать в спячку вместо сна и смягчать попытки выполнения атак холодной загрузки.

Кроме того, вы также должны настроить автоматический режим сна (Настройки > Энергия), чтобы ваш MacBook автоматически переходил в спящий режим, если оставить его без присмотра.

##### Отключить ненужные сервисы { #macos-disable-services }

Отключите некоторые ненужные настройки в настройках:

- Отключить Bluetooth

- Отключение камеры и микрофона

- Отключение сервисов определения местоположения

- Отключить Airdrop

- Отключить индексирование

##### Предотвращение вызовов Apple OCSP { #macos-ocsp }

Это печально известные «разблокируемые телеметрические» звонки от macOS Big Sur, раскрытые здесь: <https://sneak.berlin/20201112/your-computer-isnt-yours/> <sup>[[Archive.org]](https://web.archive.org/web/https://sneak.berlin/20201112/your-computer-isnt-yours/)</sup>

Вы можете заблокировать отчет OCSP, выполнив следующую команду в терминале:

- ``` sudo sh -c 'echo "127.0.0.1 ocsp.apple.com" >> /etc/hosts'```

Но вы должны задокументировать фактическую проблему, прежде чем действовать. Эта страница - хорошее место для начала: <https://blog.jacopo.io/en/post/apple-ocsp/> <sup>[[Archive.org]](https://web.archive.org/web/https://blog.jacopo.io/en/post/apple-ocsp/)</sup>

Это действительно зависит от вас. Мы заблокируем его, потому что мы вообще не хотим никакой телеметрии от моего OS к материнскому кораблю без моего конкретного согласия. Нет.

##### Включить полное шифрование диска (Filevault) { #filevault }

Вы должны включить полное шифрование диска на своем Mac с помощью Filevault в соответствии с этой частью руководства: <https://github.com/drduh/macOS-Security-and-Privacy-Guide#full-disk-encryption> <sup>[[Archive.org]](https://web.archive.org/web/https://www.bejarano.io/hardening-macos/)</sup>

**Будьте осторожны при включении. Не храните ключ восстановления в Apple при появлении запроса (это не должно быть проблемой, так как на данном этапе вы должны быть в автономном режиме). Вы не хотите, чтобы у третьей стороны был ваш ключ восстановления.**

##### MAC Address Рандомизация { #macos-mac-randomization }

К сожалению, macOS не предлагает нативного удобного способа рандомизации вашего MAC Address, поэтому вам придется делать это вручную. Это будет сбрасываться при каждой перезагрузке, и вам придется повторять это каждый раз, чтобы убедиться, что вы не используете свой фактический MAC Address при подключении к различным Wi-Fis

Это можно сделать, выполнив следующие команды в терминале (без скобок):

- (Выключите Wi-Fi) ```networksetup -setairportpower en0 off```

- (Изменить MAC Address) ```sudo ifconfig en0 ether 88:63:11:11:11:11```

- (Включите Wi-Fi) ```networksetup -setairportpower en0 on```

#### Настройка безопасного браузера { #macos-safe-browser }

См. [Safe Browser on the Host OS](#safe-browser-host-os)

### Windows Host OS { #windows-host-os }

Как упоминалось ранее, мы не рекомендуем использовать ваш ежедневный ноутбук для конфиденциальных действий. Или, по крайней мере, не рекомендуем использовать для этого OS. Это может привести к нежелательным утечкам данных, которые могут быть использованы для деанонимизации. Если у вас есть специальный ноутбук для этого, вы должны переустановить свежий чистый OS. Если вы не хотите стирать свой ноутбук и начинать все сначала, вам следует рассмотреть [маршрут Tails](# tails-route) или действовать на свой страх и риск.

Я также рекомендую выполнить первоначальную установку полностью в автономном режиме, чтобы избежать утечки данных.

#### Установка { #windows-host-install }

Вы должны следовать [Windows Installation](#windows-installation)

В качестве легкого введения рассмотрите возможность просмотра <https://www.youtube.com/watch?v=vNRics7tlqw> <sup>[[Invidious]](https://yewtu.be/watch?v=vNRics7tlqw)</sup>

#### Включить рандомизацию адресов MAC { #windows-mac-randomization }

Вы должны рандомизировать свой адрес MAC, как объяснялось ранее в этом руководстве:

Перейдите в Settings > Network & Internet > Wi-Fi > Enable Random hardware addresses (Настройки > Сеть и Интернет > ZZPROT0

В качестве альтернативы вы можете использовать это бесплатное программное обеспечение: <https://technitium.com/tmac/> <sup>[[Archive.org]](https://web.archive.org/web/https://technitium.com/tmac/)</sup>

#### Настройка безопасного браузера { #windows-safe-browser }

См. [Safe Browser on the Host OS](#safe-browser-host-os)

#### Включите некоторые дополнительные настройки конфиденциальности на Host OS { #windows-privacy-settings }

См. [Дополнительные настройки конфиденциальности Windows](#win-additional-privacy)

##### Windows Host OS шифрование { #windows-encryption }

###### Если вы намерены использовать общесистемное правдоподобное отрицание { #windows-with-deniability }

Veracrypt - это программное обеспечение, которое мы рекомендуем для полного шифрования диска, шифрования файлов и правдоподобного отрицания. Это форк известного, но устаревшего и не поддерживаемого TrueCrypt. Может использоваться для:[^330]

- Полное простое шифрование диска (ваш жесткий диск зашифрован одной парольной фразой).

- Полное шифрование диска с правдоподобным отрицанием (это означает, что в зависимости от парольной фразы, введенной при загрузке, вы загрузите либо приманку OS, либо скрытый OS).

- Простое шифрование файлового контейнера (это большой файл, который вы сможете монтировать в Veracrypt, как если бы это был внешний диск для хранения зашифрованных файлов).

- Контейнер файлов с правдоподобным отрицанием (это один и тот же большой файл, но в зависимости от парольной фразы, которую вы используете при его монтировании, вы можете смонтировать «скрытый том» или «том-приманку»).

Насколько мне известно, это единственное (удобное и используемое кем угодно) бесплатное программное обеспечение с открытым исходным кодом и открытым аудитом, которое также обеспечивает правдоподобное отрицание для широкого использования и работает с Windows Home Edition.[^331]

Загрузите и установите Veracrypt из: <https://www.veracrypt.fr/en/Downloads.html> <sup>[[Archive.org]](https://web.archive.org/web/https://www.veracrypt.fr/en/Downloads.html)</sup>

После установки ознакомьтесь со следующими вариантами, которые помогут смягчить некоторые атаки:

- Шифруйте память с помощью опции Veracrypt (настройки > параметры производительности/драйвера > шифровать RAM) по цене 5-15% производительности. Этот параметр также отключает спящий режим (который активно не очищает ключ при спящем режиме) и вместо этого полностью шифрует память, чтобы смягчить некоторые атаки с холодной загрузкой. Подробнее об этой функции здесь: <https://sourceforge.net/p/veracrypt/discussion/technical/thread/3961542951/> <sup>[[Archive.org]](https://web.archive.org/web/https://sourceforge.net/p/veracrypt/discussion/technical/thread/3961542951/)</sup>[^332]

- Включите опцию Veracrypt, чтобы стереть ключи из памяти, если вставлено новое устройство (система > настройки > безопасность > очистить ключи из памяти, если вставлено новое устройство). Это может помочь в случае, если ваша система захвачена, пока она все еще включена (но заблокирована).

- Включите опцию Veracrypt, чтобы монтировать тома как съемные тома (Настройки > Настройки > Монтировать том как съемный носитель). Это предотвратит запись Windows некоторых журналов о ваших монтированиях в журналах событий и предотвратит некоторые локальные утечки данных.[^333]

- Будьте осторожны и будьте хорошо осведомлены о ситуации, если почувствуете что-то странное. Выключите ноутбук как можно быстрее.

Если вы не хотите использовать зашифрованную память (потому что производительность может быть проблемой), вы должны по крайней мере включить спящий режим вместо сна. Это не удалит ключи из памяти (вы все еще уязвимы для атак с холодной загрузкой), но, по крайней мере, должно смягчить их, если у вашей памяти достаточно времени для распада.

Более подробная информация приведена далее в [Route A and B: Simple Encryption using Veracrypt (Windows tutorial)].

###### Если вы не намерены использовать общесистемное правдоподобное отрицание { #windows-no-deniability }

В этом случае мы рекомендуем использовать BitLocker вместо Veracrypt для полного шифрования диска. Аргументация заключается в том, что BitLocker не предлагает правдоподобной возможности отрицания вопреки Veracrypt. Жесткий противник не имеет никакого стимула проводить свой «усиленный» допрос, если вы раскрываете кодовую фразу.

Обычно в этом случае вы должны были установить Windows Pro, и настройка BitLocker довольно проста.

В принципе, вы можете следовать инструкциям здесь: <https://support.microsoft.com/en-us/windows/turn-on-device-encryption-0c453637-bc88-5f74-5105-741561aae838> <sup>[[Archive.org]](https://web.archive.org/web/https://support.microsoft.com/en-us/windows/turn-on-device-encryption-0c453637-bc88-5f74-5105-741561aae838)</sup>

Overview:

- Нажмите на меню Windows

- Тип «Bitlocker»

- Нажмите «Управление Bitlocker»

- Нажмите «Включить Bitlocker» на системном диске

- Следуйте указаниям

    - **При появлении запроса не сохраняйте ключ восстановления в учетной записи Microsoft.**

    - ** Сохраняйте ключ восстановления только на внешний зашифрованный диск. Чтобы обойти это, распечатайте ключ восстановления с помощью принтера Microsoft Print в PDF и сохраните ключ в папке Documents. Удалите этот файл позже.**

    - **Зашифруйте весь диск (не шифруйте только используемое дисковое пространство).**

    - **Используйте «Новый режим шифрования»**

    - **Запустите проверку BitLocker**

    - Перезагрузка

- Теперь шифрование должно быть запущено в фоновом режиме (вы можете проверить, нажав на значок Bitlocker в нижней правой части панели задач).

К сожалению, этого недостаточно. С помощью этой настройки ваш ключ Bitlocker может быть сохранен как есть в чипе TPM вашего компьютера. Это довольно проблематично, так как ключ может быть извлечен в некоторых случаях с помощью ease '' '.[^334][^335][^336][^337]

Чтобы смягчить это, вам придется включить еще несколько вариантов в соответствии с рекомендациями Microsoft:[^338]

- Нажмите на значок Windows

- Тип Запуск

- Введите "gpedit.msc" (это редактор групповой политики)

- Перейдите в Конфигурация компьютера > Административные шаблоны > Компоненты Windows > BitLocker > Диски операционной системы

    - Дважды щелкните «Требовать дополнительную аутентификацию при запуске»

        + Нажмите «Настроить PIN-КОД запуска TPM» и установите его на «Требовать PIN-КОД запуска с TPM»

    - Дважды щелкните «Разрешить расширенные PIN-коды для запуска»

        + Нажмите «Включить» (это позволит нам установить пароль, а не PIN-КОД)

- Закройте редактор групповой политики

- Нажмите на значок Windows

- Введите команду, чтобы отобразить «Командную строку»

- Щелкните по нему правой кнопкой мыши и нажмите «Запустить от имени администратора»

- Запустите ```manage-bde -protectors -delete c:`ZPROT2QQ (это удалит текущую защиту: ключ восстановления, который вам не понадобится)

- Запустите ```manage-bde -protectors -add c: -TPMAndPIN`ZPROT2QQ (вам будет предложено ввести пароль перед загрузкой)

    - Введите пароль или парольную фразу по вашему выбору (подходящую)

- Запустите ```manage-bde -status```

    - Теперь вы должны увидеть на диске C: ниже «Key Protectors» опцию «TPM и PIN-КОД»

- Ты закончила

Теперь, когда вы перезагружаете компьютер, в идеале вам должно быть предложено:

- Загрузочный пароль BIOS/UEFI

- Пароль разблокировки SSD/HDD (если функция доступна на вашем BIOS)

- Экран PIN-кода перед загрузкой Bitlocker, где вам нужно ввести пароль/парольную фразу, которую вы только что настроили

- И, наконец, экран входа в Windows, где вы можете ввести учетные данные, которые вы настроили ранее

##### Включить спящий режим (опционально) { #windows-hibernation }

Опять же, как объяснялось ранее. Вы никогда не должны использовать функцию сна/ожидания, чтобы смягчить некоторые атаки холодной загрузки и злой горничной. Вместо этого вы должны отключиться или впасть в спячку. Поэтому вы должны переключить свой ноутбук из спящего режима в спящий режим при закрытии крышки или когда ваш ноутбук переходит в спящий режим.

(**Обратите внимание, что вы не можете включить спящий режим, если вы ранее включили шифрование RAM в Veracrypt)**

Причина в том, что Hibernation фактически полностью выключит ваш ноутбук и очистит память. Sleep, с другой стороны, оставит память включенной (включая ваш ключ дешифрования) и может сделать ваш ноутбук уязвимым для атак с холодной загрузкой.

По умолчанию Windows 10/11 может не предлагать вам эту возможность, поэтому вы должны включить ее, следуя этому руководству Microsoft: <https://docs.microsoft.com/en-us/troubleshoot/windows-client/deployment/disable-and-re-enable-hibernation> <sup>[[Archive.org]](https://web.archive.org/web/https://docs.microsoft.com/en-us/troubleshoot/windows-client/deployment/disable-and-re-enable-hibernation)</sup>

- Откройте командную строку администратора (щелкните правой кнопкой мыши Command Prompt и "Run as Administrator")

- Запуск: powercfg.exe /hibernate on

- Теперь выполните дополнительную команду: ```powercfg /h /type full```

    - **Эта команда убедится, что ваш режим гибернации заполнен, и полностью очистит память (ненадежно).**

После этого перейдите к настройкам питания:

- Откройте панель управления.

- Безопасность системы

- Параметры питания

- Откройте «Выберите, что делает кнопка питания»

- Измените все от сна до гибернации или выключения

- Вернуться к параметрам питания

- Выберите Изменить настройки плана.

- Выберите Расширенные настройки питания

- Измените все значения Sleep для каждого плана электропитания на 0 (Никогда)

- Убедитесь, что гибридный Sleep выключен для каждого плана электропитания

- Включить Hibernate через время, которое вы хотите

- Отключить все таймеры пробуждения

#### Решение о том, какой подмаршрут вы будете использовать { #windows-subroute }

Теперь вам нужно будет выбрать следующий шаг между двумя вариантами:

- Маршрут A: Простое шифрование вашего текущего OS

    - Преимущества:

        + Не требует протирания ноутбука

        + Нет проблем с локальными утечками данных

        + Отлично работает с накопителем SSD

        + Работает с любым OS

        + Простой

    - Аферы

        + Злоумышленник может заставить вас раскрыть ваш пароль и все ваши секреты, и у вас не будет правдоподобного отрицания.

        + Опасность утечки данных в Интернете

- Маршрут B: Простое шифрование вашего текущего OS с последующим использованием правдоподобного отрицания на самих файлах:

    - Преимущества:

        + Не требует протирания ноутбука

        + Отлично работает с накопителем SSD

        + Работает с любым OS

        + Правдоподобное отрицание возможно с «мягкими» противниками

    - Аферы

        + Опасность утечки данных в Интернете

        + Опасность локальных утечек данных (что приведет к дополнительной работе по устранению этих утечек)

- Маршрут C: Правдоподобное шифрование отказа вашей операционной системы (у вас будет «скрытый OS» и «приманка OS», запущенная на ноутбуке):

    - Преимущества:

        + Нет проблем с локальными утечками данных

        + Правдоподобное отрицание возможно с «мягкими» противниками

    - Аферы

        + Требуется Windows (эта функция не «легко» поддерживается на Linux).

        + Опасность утечки данных в Интернете

        + Требуется полная очистка ноутбука

        + Не используется с диском SSD из-за требования отключения Trim Operations. Это со временем серьезно ухудшит производительность/работоспособность вашего накопителя SSD.[^339][^340]

**Как вы можете видеть, маршрут C предлагает только два преимущества конфиденциальности по сравнению с другими, и он будет полезен только против мягкого законного противника. Помните, что <https://en.wikipedia.org/wiki/Rubber-hose_cryptanalysis> ** <sup>[[Wikiless]](https://wikiless.tiekoetter.com/wiki/Rubber-hose_cryptanalysis)</sup><sup>[[Archive.org]](https://web.archive.org/web/https://en.wikipedia.org/wiki/Rubber-hose_cryptanalysis)</sup>**.**

Выбор маршрута зависит от вас. Маршрут А - минимальный.

**Всегда проверяйте наличие новых версий Veracrypt, чтобы убедиться, что вы пользуетесь последними исправлениями. Особенно проверьте это перед применением больших обновлений Windows, которые могут сломать загрузчик Veracrypt и отправить вас в цикл загрузки.**

**NOTE THAT BY DEFAULT VERACRYPT WILL ALWAYS PROPOSE A SYSTEM PASSWORD IN QWERTY (display the password as a test). This can cause issues if your boot input is using your laptop's keyboard (AZERTY for example) as you will have set up your password in QWERTY and will input it at boot time in AZERTY. So, make sure you check when doing the test boot what keyboard layout your BIOS is using. You could fail to log in just because of the QWERTY/AZERTY mix-up. If your BIOS boots using AZERTY, you will need to type the password in QWERTY within Veracrypt.**

##### Маршрут A и B: простое шифрование с использованием Veracrypt (руководство по Windows) { #veracrypt-simple-encryption }

**Пропустите этот шаг, если вы использовали BitLocker ранее.**

Вам не нужно иметь HDD для этого метода, и вам не нужно отключать Trim на этом маршруте. Утечки Trim будут полезны только для криминалистов при обнаружении наличия скрытого тома, но не будут иметь большого значения в противном случае.

Этот маршрут довольно прост и просто зашифрует вашу текущую операционную систему без потери данных. Обязательно прочитайте все тексты, которые Veracrypt показывает вам, чтобы у вас было полное понимание того, что происходит. Для этого выполните следующие действия:

- Запустить VeraCrypt

- Перейдите в Настройки:

    - Настройки > Параметры производительности/драйвера > Шифровать RAM

    - System (Система) > Settings (Настройки) > Security (Безопасность) > Clear keys from memory if a new device is inserted (Очистить

    - System > Settings > Windows > Enable Secure Desktop (Система > Настройки > Windows >

- Выберите Систему

- Выберите Encrypt System Partition/Drive (Зашифровать системный раздел/

- Выберите Обычный (Простой)

- Выберите одиночную загрузку

- Выберите AES в качестве алгоритма шифрования (нажмите кнопку тестирования, если вы хотите сравнить скорости)

- Выберите SHA-512 в качестве алгоритма хеширования (потому что почему бы и нет)

- Введите сильную парольную фразу (чем длиннее, тем лучше, помните [Guidelines for passwords and passphrases](#password-guidelines))

- Соберите энтропию, случайным образом перемещая курсор до тех пор, пока полоса не заполнится

- Нажмите Next (Далее) в качестве экрана Generated Keys (Сгенерированные клю

- Спасать или не спасать disk - решать вам. Мы рекомендуем сделать один (на всякий случай), просто убедитесь, что он хранится за пределами вашего зашифрованного диска (например, ключ USB или подождите и посмотрите конец этого руководства для руководства по безопасному резервному копированию). Этот диск спасения не будет хранить вашу кодовую фразу, и она все равно понадобится вам для ее использования.[^341]

- Режим протирания:

    - Если у вас еще нет конфиденциальных данных на этом ноутбуке, выберите Ԥ

    - Если у вас есть конфиденциальные данные на SSD, только Trim должен позаботиться об этом, но мы рекомендуем один проход (случайные данные), чтобы быть уверенным.[^342]

    - Если у вас есть конфиденциальные данные на HDD, Trim отсутствует, и мы рекомендуем пройти хотя бы 1 проход.

- Проверьте свою настройку. Veracrypt теперь перезагрузит вашу систему, чтобы проверить загрузчик перед шифрованием. Этот тест должен пройти, чтобы шифрование продолжалось.

- После перезагрузки компьютера и прохождения теста. Veracrypt предложит вам начать процесс шифрования.

- Запустите шифрование и дождитесь его завершения.

- Вы закончили, пропустите маршрут B и перейдите к следующим шагам.

Будет еще один раздел о создании зашифрованных файловых контейнеров с правдоподобным отрицанием на Windows.

##### Маршрут B: правдоподобное шифрование отрицания с помощью скрытого OS (только Windows) { #veracrypt-hidden-os }

**Это поддерживается только на Windows.**

**Это рекомендуется только для накопителя HDD. Это не рекомендуется на диске SSD.**

**Ваш скрытый OS не должен быть активирован (с ключом продукта MS). Поэтому этот маршрут порекомендует и проведет вас через полную чистую установку, которая сотрет все на вашем ноутбуке.**

Ознакомьтесь с документацией Veracrypt <https://www.veracrypt.fr/en/VeraCrypt%20Hidden%20Operating%20System.html> <sup>[[Archive.org]](https://web.archive.org/web/https://www.veracrypt.fr/en/VeraCrypt%20Hidden%20Operating%20System.html)</sup> (Процесс создания части скрытой операционной системы) и <https://www.veracrypt.fr/en/Security%20Requirements%20for%20Hidden%20Volumes.html> <sup>[[Archive.org]](https://web.archive.org/web/https://www.veracrypt.fr/en/Security%20Requirements%20for%20Hidden%20Volumes.html)</sup> (Требования безопасности и меры предосторожности, относящиеся к скрытым томам).

Вот как будет выглядеть ваша система после завершения этого процесса:

![image22](../media/image22.png)

(Иллюстрация из документации Veracrypt, <https://veracrypt.fr/en/VeraCrypt%20Hidden%20Operating%20System.html> <sup>[[Archive.org]](https://web.archive.org/web/https://www.veracrypt.fr/en/VeraCrypt%20Hidden%20Operating%20System.html)</sup>)

Как видите, этот процесс требует наличия двух разделов на жестком диске с самого начала.

Этот процесс будет выполнять следующие действия:

- Зашифруйте второй раздел (внешний том), который будет выглядеть как пустой неформатированный диск из приманки OS.

- Предложите вам возможность скопировать некоторый контент-приманку во внешнем объеме.

    - Здесь вы скопируете свою коллекцию аниме/порно с внешнего жесткого диска на внешний том.

- Создайте скрытый том во внешнем объеме этого второго раздела. Здесь будет находиться скрытый OS.

- Клонируйте текущую установку Windows 10/11 на скрытый том.

- Протрите текущий Windows 10/11.

- Это означает, что ваш текущий Windows 10/11 станет скрытым Windows 10/11 и что вам нужно будет переустановить свежую приманку Windows 10/11 OS.

**Mandatory if you have an SSD drive and you still want to do this against the recommendation: Disable SSD Trim in Windows** **(again this is NOT recommended at all as** **disabling Trim in itself is highly suspicious**). **Also** **as mentioned earlier, disabling Trim will reduce the lifetime of your SSD drive and will significantly impact its performance over time (your laptop will become slower and slower over several months of use until it becomes almost unusable, you will then have to clean the drive and re-install everything). But you must do it to prevent data leaks** **that could allow forensics to defeat your plausible deniability****. The only way around this at the moment is to have a laptop with a classic HDD drive instead.**[^343][^344][^345][^346]

###### Шаг 1: Создайте Windows 10/11 установите ключ USB { #hidden-os-step1 }

См. [Windows Installation Media Creation](# win-installation-media) и перейдите к ключевому маршруту USB.

###### Шаг 2: Загрузите ключ USB и запустите процесс установки Windows 10/11 (скрытый OS) { #hidden-os-step2 }

- Вставьте ключ USB в ноутбук

- См. [Установка Windows](#windows-installation) и приступите к установке Windows 10/11 Home.

###### Шаг 3: Настройки конфиденциальности (скрытый OS) { #hidden-os-step3 }

См. [Дополнительные настройки конфиденциальности Windows](#win-additional-privacy)

###### Шаг 4: Запуск процесса установки и шифрования Veracrypt (Hidden OS) { #hidden-os-step4 }

Не забудьте прочитать <https://www.veracrypt.fr/en/VeraCrypt%20Hidden%20Operating%20System.html> <sup>[[Archive.org]](https://web.archive.org/web/https://www.veracrypt.fr/en/VeraCrypt%20Hidden%20Operating%20System.html)</sup>

Не подключайте этот OS к вашему известному Wi-Fi. Вы должны загрузить установщик Veracrypt с другого компьютера и скопировать его сюда, используя ключ USB. Для этого выполните следующие действия:

- Установка Veracrypt

- Начало Veracrypt

- Перейдите в Настройки:

    - Настройки > Параметры производительности/драйвера > Шифровать RAM (**обратите внимание, что эта опция несовместима с гибернацией вашего ноутбука и означает, что вам придется полностью выключиться)**

    - System (Система) > Settings (Настройки) > Security (Безопасность) > Clear keys from memory if a new device is inserted (Очистить

    - System > Settings > Windows > Enable Secure Desktop (Система > Настройки > Windows >

- Войдите в систему и выберите Create Hidden Operating System (Создать скрытую операционную систему)

- Внимательно прочитайте все подсказки

- Выберите Single-Boot (Одиночная загрузка), если

- Создайте внешний том с помощью AES и SHA-512.

- Используйте все пространство, доступное на втором разделе для внешнего тома

- Используйте надежную парольную фразу (помните [Guidelines for passwords and passwordphrases](#password-guidelines))

- Выберите «Да» для «Больших файлов»

- Создайте некоторую энтропию, перемещая мышь до тех пор, пока полоса не заполнится, и выберите NTFS (не выбирайте exFAT, поскольку вы хотите, чтобы этот внешний том выглядел «нормальным», а NTFS - нормальным).

- Форматирование внешнего тома

- Открытый внешний объем:

    - На этом этапе вы должны скопировать данные-приманку на внешний том. Таким образом, у вас должно быть несколько конфиденциальных, но не настолько конфиденциальных файлов/папок для копирования туда. В случае, если вам нужно раскрыть пароль к этому тому**.** Это хорошее место для вашей коллекции аниме/mp3/фильмов/порно.

    - Мы рекомендуем не заполнять внешний объем слишком много или слишком мало (около 40%). Помните, что вы должны оставить достаточно места для скрытого OS (который будет того же размера, что и первый раздел, созданный вами во время установки).

- Используйте сильную парольную фразу для скрытого тома (очевидно, отличную от парольной фразы для внешнего тома).

- Теперь вы создадите скрытый том, выберите AES и SHA-512

- Заполните полосу энтропии до конца случайными движениями мыши

- Форматирование скрытого тома

- Продолжить клонирование

- Теперь Veracrypt перезапустит и клонирует Windows, где вы запустили этот процесс, в скрытый том. Этот Windows станет вашим скрытым OS.

- Когда клонирование будет завершено, Veracrypt перезапустится в скрытой системе

- Veracrypt сообщит вам, что скрытая система теперь установлена, а затем предложит вам стереть оригинальный OS (тот, который вы установили ранее с помощью ключа USB).

- Используйте 1-проходную протирку и продолжайте.

- Теперь ваш скрытый OS будет установлен, перейдите к следующему шагу

###### Шаг 5: Перезагрузите и загрузите ключ USB и снова запустите процесс установки Windows 10/11 (приманка OS) { #decoy-os-step5 }

Теперь, когда скрытый OS полностью установлен, вам нужно будет установить приманку OS:

- Вставьте ключ USB в ноутбук

- См. [Установка Windows](# windows-installation) и повторите установку Windows 10/11 Home (не устанавливайте другую версию и придерживайтесь Home).

###### Шаг 6: Настройки конфиденциальности (приманка OS) { #decoy-os-step6 }

См. [Дополнительные настройки конфиденциальности Windows](#win-additional-privacy)

###### Шаг 7: Запуск процесса установки и шифрования Veracrypt (приманка OS) { #decoy-os-step7 }

Теперь вы зашифруете приманку OS:

- Установка Veracrypt

- Запустить VeraCrypt

- Выберите Систему

- Выберите Encrypt System Partition/Drive (Зашифровать системный раздел/

- Выберите Обычный (Простой)

- Выберите одиночную загрузку

- Выберите AES в качестве алгоритма шифрования (нажмите кнопку тестирования, если вы хотите сравнить скорости)

- Выберите SHA-512 в качестве алгоритма хеширования (потому что почему бы и нет)

- Введите короткий слабый пароль (да это серьезно, сделайте это, это будет объяснено позже).

- Соберите энтропию, случайным образом перемещая курсор до тех пор, пока полоса не заполнится

- Нажмите Next (Далее) в качестве экрана Generated Keys (Сгенерированные клю

- Спасать или не спасать disk - решать вам. Мы рекомендуем сделать один (на всякий случай), просто убедитесь, что он хранится за пределами вашего зашифрованного диска (например, ключ USB или подождите и посмотрите конец этого руководства для руководства по безопасному резервному копированию). Этот диск спасения не будет хранить вашу кодовую фразу, и она все равно понадобится вам для ее использования.[^347]

- Режим очистки: выберите 1-проход, чтобы быть в безопасности

- Предварительно протестируйте вашу установку. Veracrypt теперь перезагрузит вашу систему, чтобы проверить загрузчик перед шифрованием. Этот тест должен пройти, чтобы шифрование продолжалось.

- После перезагрузки компьютера и прохождения теста. Veracrypt предложит вам начать процесс шифрования.

- Запустите шифрование и дождитесь его завершения.

- Ваш приманка OS теперь готова к использованию.

###### Шаг 8: Проверьте свою настройку (загрузка на обоих) { #veracrypt-step8-test }

Пора протестировать вашу настройку:

- Перезагрузите и введите свою парольную фразу Hidden OS, вы должны загрузиться в Hidden OS.

- Перезагрузите и введите кодовую фразу приманки OS, вы должны загрузиться в приманке OS.

- Запустите Veracrypt на приманке OS и смонтируйте второй раздел с помощью парольной фразы внешнего тома (смонтируйте его как только для чтения, перейдя в Параметры монтирования и выбрав Только для чтения), и он должен смонтировать второй раздел как только для чтения, отображающий ваши данные приманки (вашу коллекцию аниме/порно). Теперь вы монтируете его только для чтения, потому что, если бы вы записывали на него данные, вы могли бы переопределить контент из своего скрытого OS.

###### Шаг 9. Безопасное изменение данных приманки на внешнем томе { #veracrypt-step9-decoy-data }

Прежде чем перейти к следующему шагу, вы должны узнать, как безопасно смонтировать внешний том для записи на него контента. Это также объясняется в этой официальной документации Veracrypt <https://www.veracrypt.fr/en/Protection%20of%20Hidden%20Volumes.html> <sup>[[Archive.org]](https://web.archive.org/web/https://www.veracrypt.fr/en/Protection%20of%20Hidden%20Volumes.html)</sup>

**Вы должны делать это из безопасного и надежного места.**

По сути, вы монтируете внешний том, а также предоставляете парольную фразу скрытого тома в параметрах монтирования, чтобы защитить скрытый том от перезаписи:

- Открыть Veracrypt

- Выберите второй раздел

- Нажмите Mount (Подключить)

- Нажмите Mount Options (Параметры монтирования

- Отметьте опцию «Защитить скрытый том...»

- Введите скрытую парольную фразу OS

- Нажимаем ОК.

- Введите парольную фразу внешнего объема

- Нажимаем ОК.

- Теперь вы можете открывать и записывать на внешний том, чтобы изменить содержимое (копировать/перемещать/удалять/редактировать...)

Эта операция фактически не монтирует скрытый том и должна предотвратить создание каких-либо криминалистических доказательств, которые могут привести к обнаружению скрытого OS. Однако, пока вы выполняете эту операцию, оба пароля будут храниться в вашем RAM. Вы все еще можете быть уязвимы для атаки холодной загрузки. Чтобы смягчить эту проблему, убедитесь, что у вас есть возможность зашифровать RAM, как указано ранее.

###### Шаг 10: Оставьте некоторые криминалистические доказательства вашего внешнего объема (с данными приманки) в вашем приманке OS { #veracrypt-step10-forensics }

Мы должны сделать приманку OS максимально правдоподобной. Мы также хотим, чтобы ваш противник недооценил ваш интеллект.

Важно добровольно оставить некоторые криминалистические доказательства вашего Контента-приманки в вашем Приманке OS. Эти доказательства позволят судебно-медицинским экспертам увидеть, что вы часто монтировали внешний том для доступа к его содержимому.

Вот полезные советы, чтобы оставить некоторые криминалистические доказательства:

- Воспроизвести содержимое внешнего тома из приманки OS (например, с помощью VLC). Обязательно сохраните их историю.

- Редактируйте документы и работайте над ними.

- Включите индексирование файлов снова на приманке OS и включите смонтированный внешний том.

- Демонтируйте его и часто монтируйте, чтобы просматривать некоторый контент или перемещать файлы.

- Скопируйте некоторый контент с внешнего тома на приманку OS, а затем удалите его небезопасно. Просто положите его в корзину, что сделает только тот, кто наивен, думая, что он был удален.

- Установите клиент Torrent на приманку OS; используйте его время от времени, чтобы загрузить некоторые аналогичные материалы, которые вы оставите на приманке OS.

- На приманке OS может быть установлен клиент VPN с вашим известным VPN (безналичная оплата).

Не ставьте на приманку OS ничего подозрительного, например:

- это руководство

- Любые ссылки на это руководство

- Любое подозрительное программное обеспечение для обеспечения анонимности, такое как Tor Browser

- Любые тома Veracrypt

- Любые документы об анонимности или безопасности

Цель состоит в том, чтобы заставить вашего противника поверить, что вы не так умны, как они думали, чтобы удержать его от более глубокого поиска.

###### Примечания { #veracrypt-notes }

**Помните, что вам понадобятся веские оправдания для этого правдоподобного сценария отрицания:**

- **Вы используете Veracrypt, потому что используете Windows 10/11 Home, которые не имеют функции Bitlocker, но вы все равно хотели разумной конфиденциальности.**

- **У вас есть два раздела, потому что вы хотели отделить систему от данных для легкой организации, а также потому, что какой-то чудаковатый друг сказал вам, что это лучше для производительности.**

- **Вы использовали слабый пароль для легкой и удобной загрузки системы и сильную длинную парольную фразу на внешнем томе. Вы были слишком ленивы, чтобы напечатать сильную кодовую фразу на каждом ботинке.**

- **Вы зашифровали второй раздел паролем, отличным от пароля системы, потому что не хотите, чтобы кто-то в вашей группе/домене видел ваши данные. Вы не хотели, чтобы эти данные были доступны никому.**

Потратьте некоторое время, чтобы снова прочитать «Возможные объяснения существования двух разделов Veracrypt на одном диске» документации Veracrypt здесь <https://www.veracrypt.fr/en/VeraCrypt%20Hidden%20Operating%20System.html> <sup>[[Archive.org]](https://web.archive.org/web/https://www.veracrypt.fr/en/VeraCrypt%20Hidden%20Operating%20System.html)</sup>

СОБЛЮДАЙТЕ ОСТОРОЖНОСТЬ

- **You should never mount the Hidden Volume from the Decoy OS (NEVER EVER). If you did this, it would create forensic evidence of the Hidden Volume within the Decoy OS which could jeopardize your attempt at plausible deniability**. If you did this anyway (intentionally or by mistake) from the Decoy OS, there are ways to erase forensic evidence that will be explained later at the end of this guide, so this mistake alone isn't a huge deal if you follow the steps in [Some additional measures against forensics](#anti-forensics).

- **Никогда не используйте приманку OS из той же сети (публичная Wi-Fi), что и скрытая OS.**

- **Когда вы монтируете внешний том из приманки OS, не записывайте никакие данные в внешний том. Это может переопределить то, что выглядит как пустое пространство, но на самом деле это ваш скрытый OS. Вы всегда должны монтировать его только для чтения.**

- **Если вы хотите изменить содержимое приманки внешнего тома, вы должны использовать клавишу Live OS USB, которая будет запускать Veracrypt.**

- **Обратите внимание, что вы не будете использовать скрытый OS для выполнения конфиденциальных действий, это будет сделано позже из VM в скрытом OS. Скрытый OS предназначен только для защиты вас от мягких законных злоумышленников, которые могут получить доступ к вашему ноутбуку и заставить вас раскрыть свой пароль.**

- **Будьте осторожны с любым вмешательством в работу вашего ноутбука. Атаки злой горничной могут раскрыть ваш скрытый OS.**

### Virtualbox на вашем Host OS { #virtualbox-host }

Помните о [виртуализации](#virtualization).

Этот шаг и следующие шаги должны выполняться из Host OS. Это может быть ваш Host OS с простым шифрованием (Windows/Linux/macOS) или ваш скрытый OS с правдоподобным отрицанием (только Windows).

В этом маршруте вы будете широко использовать бесплатное программное обеспечение Oracle Virtualbox. Это программное обеспечение для виртуализации, в котором вы можете создать Virtual Machines, которое эмулирует компьютер с определенным OS (если вы хотите использовать что-то еще, например, Xen, Qemu, KVM или VMWARE, не стесняйтесь делать это, но эта часть руководства охватывает Virtualbox только для удобства).[^348]

Таким образом, вы должны знать, что Virtualbox не является программным обеспечением для виртуализации с лучшим послужным списком с точки зрения безопасности. Некоторые из зарегистрированных проблем не были полностью исправлены до настоящего времени. Если вы используете Linux и у вас есть немного больше технических навыков, вам следует рассмотреть возможность использования KVM, следуя руководству, доступному по адресу Whonix здесь <https://www.whonix.org/wiki/KVM> <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/KVM)</sup> и здесь <z> <sup>[[Archive.org]](https://web.archive.org/web/z)</sup>[^349][^350]

Во всех случаях следует предпринять некоторые шаги:

**Все ваши конфиденциальные действия будут выполняться гостем Virtual Machine под управлением Windows 10/11 Pro (на этот раз не Home), Linux или macOS.**

У этого есть несколько преимуществ, которые помогут вам сохранить анонимность:

- Это должно предотвратить прямой доступ гостевого VM OS (Windows/Linux/macOS), приложений и любой телеметрии в VMs к вашему оборудованию. Даже если ваш VM скомпрометирован вредоносным ПО, вредоносное ПО не сможет получить доступ к Host OS и скомпрометировать вашу реальную машину.

- Это позволит нам заставить весь сетевой трафик из вашего VM проходить через другой шлюз VM, который будет направлять весь трафик через сеть Tor. Это сетевой «выключатель». Ваш VM полностью потеряет сетевое соединение и перейдет в автономный режим, если целевая сеть VM потеряет соединение с сетью Tor.

- Сам VM, который имеет подключение к Интернету только через сетевой шлюз Tor, подключится к вашей оплаченной наличными услуге VPN через Tor.

- Утечки DNS будут невозможны, потому что VM находится в изолированной сети, которая должна проходить через Tor несмотря ни на что.

### Выберите способ подключения { #whonix-connectivity }

В рамках этого маршрута есть семь возможностей:

- **Рекомендуем и предпочитаем:**

    - **Используйте только Tor (Пользователь > Tor > Интернет)**

    - **Используйте VPN вместо Tor (Пользователь > Tor > VPN > Интернет) в конкретных случаях**

    - **Используйте VPS с собственным хостингом VPN/Proxy поверх Tor (User > Tor > Self-Hosted VPN/Proxy > Internet) в конкретных случаях**

- Возможно, если того требует контекст:

    - Используйте VPN вместо Tor вместо VPN (Пользователь > VPN > Tor > VPN > Интернет)

    - Используйте Tor поверх VPN (Пользователь > VPN > Tor > Интернет)

- Не рекомендуется и рискованно:

    - Используйте только VPN (Пользователь > VPN > Интернет)

    - Используйте VPN поверх VPN (Пользователь > VPN > VPN > Интернет)

- **Не рекомендуется и очень рискованно (но возможно)**

    - Нет VPN и нет Tor (Пользователь > Интернет)

![image23](../media/image23.png)

#### Только Tor { #whonix-tor-only }

Это предпочтительное и наиболее рекомендуемое решение.

![image24](../media/image24.png)

С помощью этого решения вся ваша сеть проходит через Tor, и этого должно быть достаточно, чтобы гарантировать вашу анонимность в большинстве случаев.

Есть один главный недостаток: **Некоторые сервисы блокируют/блокируют узлы Tor Exit напрямую и не позволят создавать учетные записи из них.**

Чтобы смягчить это, вам, возможно, придется рассмотреть следующий вариант: VPN по сравнению с Tor, но рассмотрите некоторые риски, связанные с этим, описанные в следующем разделе.

#### VPN/Прокси через Tor { #whonix-vpn-over-tor }

Это решение может принести некоторые преимущества в некоторых конкретных случаях по сравнению с использованием Tor только там, где доступ к службе назначения будет невозможен с узла выхода Tor. Это связано с тем, что многие сервисы просто прямо запрещают, затрудняют или блокируют узлы выхода Tor (см. <https://gitlab.torproject.org/legacy/trac/-/wikis/org/doc/ListOfServicesBlockingTor> <sup>[[Archive.org]](https://web.archive.org/web/https://gitlab.torproject.org/legacy/trac/-/wikis/org/doc/ListOfServicesBlockingTor)</sup>).

Это решение может быть реализовано двумя способами:

- Платный VPN по сравнению с Tor (самый простой)

- Платный VPS Self-Hosted, настроенный как VPN/Proxy (наиболее эффективный способ избежать онлайн-препятствий, таких как капча, но требующий больше навыков с Linux)

Как вы можете видеть на этой иллюстрации, если ваш денежный (предпочтительный)/Monero оплаченный VPN/Proxy скомпрометирован злоумышленником (несмотря на их заявление о конфиденциальности и политику отсутствия регистрации), они найдут только анонимный денежный/Monero оплаченный VPN/Proxy аккаунт, подключающийся к их услугам с узла Tor Exit.

![image25](../media/image25.png)

Если злоумышленнику также удастся скомпрометировать сеть Tor, он обнаружит только IP-адрес случайного публичного Wi-Fi, который не привязан к вашей личности.

Если злоумышленник каким-либо образом скомпрометирует ваш VM OS (например, с помощью вредоносного ПО или эксплойта), он окажется в ловушке во внутренней сети Whonix и не сможет раскрыть IP-адрес общедоступного Wi-Fi.

** Однако у этого решения есть один основной недостаток: помехи при изоляции потока Tor**.[^351]

Изоляция потока - это метод смягчения последствий, используемый для предотвращения некоторых корреляционных атак с помощью различных схем Tor для каждого приложения. Вот иллюстрация, чтобы показать, что такое изоляция потока:

![image26](../media/image26.png)

(Иллюстрация Марсело Мартинса, <https://stakey.club/en/decred-via-tor-network/> <sup>[[Archive.org]](https://web.archive.org/web/https://stakey.club/en/decred-via-tor-network/)</sup>)

VPN/Proxy через Tor попадает на правую сторону, что означает использование VPN/Proxy через Tor заставляет Tor использовать одну цепь для всех действий вместо нескольких цепей для каждой. Это означает, что использование VPN/Proxy вместо Tor может снизить эффективность Tor в некоторых случаях и поэтому должно использоваться только в некоторых конкретных случаях:[^352]

- Когда служба назначения не разрешает узлы выхода Tor.

- Когда вы не возражаете против использования общей схемы Tor для различных услуг. Например, при использовании различных аутентифицированных сервисов.

**You should however consider not using this method when your aim is just to browse random various unauthenticated websites as you will not benefit from Stream Isolation and this could make correlation attacks easier over time for an adversary between each of your sessions (see [Your Anonymized Tor/VPN traffic](#traffic-anonymization)). If your goal however is to use the same identity at each session on the same authenticated services, the value of Stream isolation is lessened as you can be correlated through other means.**

Вы также должны знать, что изоляция потока не обязательно настроена по умолчанию на рабочей станции Whonix. Он предварительно настроен только для некоторых приложений (включая Tor Browser).

Кроме того, обратите внимание, что изоляция потока не обязательно меняет все узлы в вашей цепи Tor. Иногда он может изменить только один или два. Во многих случаях изоляция потока (например, в Tor Browser) изменяет только ретрансляционный (средний) узел и выходной узел, сохраняя при этом тот же защитный (входной) узел.

More information at:

- <https://www.whonix.org/wiki/Stream_Isolation> <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Stream_Isolation)</sup>

- <https://tails.boum.org/contribute/design/stream_isolation/> <sup>[[Archive.org]](https://web.archive.org/web/https://tails.boum.org/contribute/design/stream_isolation/)</sup>

- <https://www.whonix.org/wiki/Tunnels/Introduction#Comparison_Table> <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Tunnels/Introduction#Comparison_Table)</sup>

#### Tor поверх VPN { #whonix-tor-over-vpn }

Вы можете задаться вопросом: а как насчет использования Tor вместо VPN вместо VPN вместо Tor? Ну, мы бы не обязательно рекомендовали его:

- Недостатки:

    - Ваш провайдер VPN - это просто еще один интернет-провайдер, который затем узнает ваш исходный IP-адрес и при необходимости сможет деанонимизировать вас. Мы им не доверяем. Мы предпочитаем ситуацию, когда ваш провайдер VPN не знает, кто вы. Это не добавляет много с точки зрения анонимности.

    - Это приведет к тому, что вы подключитесь к различным службам, используя IP-адрес выходного узла Tor, который запрещен/помечен во многих местах. Это не помогает с точки зрения удобства.

- Преимущества:

    - **Основным преимуществом является то, что если вы находитесь во враждебной среде, где доступ к Tor невозможен/опасен/подозрителен, но VPN в порядке.**

    - Этот метод также не нарушает изоляцию потока Tor.

    - Это также скрывает ваши действия Tor от вашего основного интернет-провайдера.

Обратите внимание, что если у вас возникли проблемы с доступом к сети Tor из-за блокировки/цензуры, вы можете попробовать использовать мосты Tor. См. [Использование мостов Tor во враждебных средах](#tor-bridges).

Также можно рассмотреть ** VPN вместо Tor вместо VPN (Пользователь > VPN > Tor > VPN > Интернет)**, используя вместо этого два наличных/Monero оплаченных VPN. Это означает, что вы подключите Host OS к первому VPN от вашего публичного Wi-Fi, затем Whonix подключится к Tor, и, наконец, ваш VM подключится ко второму VPN через Tor через VPN (см. <https://www.whonix.org/wiki/Tunnels/Connecting_to_a_VPN_before_Tor> <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Tunnels/Connecting_to_a_VPN_before_Tor)</sup>).

Это, конечно, окажет значительное влияние на производительность и может быть довольно медленным, но Tor необходим где-то для достижения разумной анонимности.

Достичь этого технически легко в рамках этого маршрута, вам нужны две отдельные анонимные учетные записи VPN и вы должны подключиться к первому VPN из Host OS и следовать маршруту.

Заключение: Делайте это только в том случае, если вы считаете, что использование только Tor рискованно/невозможно, но VPN в порядке. Или просто потому, что вы можете, и почему бы и нет. Этот метод не снизит вашу безопасность/конфиденциальность/анонимность.

#### Только VPN { #whonix-vpn-only }

Этот маршрут не будет объяснен или рекомендован.

**Если вы можете использовать VPN, то вы сможете добавить слой Tor поверх него. И если вы можете использовать Tor, то вы можете добавить анонимный VPN вместо Tor, чтобы получить предпочтительное решение.**

Just using a VPN or even a VPN over VPN makes no sense as those can be traced back to you over time. One of the VPN providers will know your real origin IP (even if it is in a safe public space) and even if you add one over it, the second one will still know you were using that other first VPN service. This will only slightly delay your de-anonymization. Yes, it is an added layer ... but it is a persistent centralized added layer, and you can be de-anonymized over time. This is just chaining 3 ISPs that are all subject to lawful requests.

Для получения дополнительной информации ознакомьтесь со следующими рекомендациями:

- <https://www.whonix.org/wiki/Comparison_Of_Tor_with_CGI_Proxies,_Proxy_Chains,_and_VPN_Services#Tor_and_VPN_Services_Comparison> <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Comparison_Of_Tor_with_CGI_Proxies,_Proxy_Chains,_and_VPN_Services)</sup>

- <https://www.whonix.org/wiki/Why_does_Whonix_use_Tor> <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Why_does_Whonix_use_Tor)</sup>

- <https://www.researchgate.net/publication/324251041_Anonymity_communication_VPN_and_Tor_a_comparative_study> <sup>[[Archive.org]](https://web.archive.org/web/https://www.researchgate.net/publication/324251041_Anonymity_communication_VPN_and_Tor_a_comparative_study)</sup>

- <https://gist.github.com/joepie91/5a9909939e6ce7d09e29#file-vpn-md> <sup>[[Archive.org]](https://web.archive.org/web/https://gist.github.com/joepie91/5a9909939e6ce7d09e29)</sup>

- <https://schub.wtf/blog/2019/04/08/very-precarious-narrative.html> <sup>[[Archive.org]](https://web.archive.org/web/https://schub.wtf/blog/2019/04/08/very-precarious-narrative.html)</sup>

**В контексте этого руководства Tor требуется где-то для достижения разумной и безопасной анонимности, и вы должны использовать его, если можете.**

#### № VPN/Tor { #whonix-no-vpn-tor }

Если вы не можете использовать VPN или Tor там, где вы находитесь, вы, вероятно, находитесь в очень враждебной среде, где наблюдение и контроль чрезвычайно высоки.

Только не стоит, это не стоит и слишком рискованно. Вы можете быть деанонимизированы почти мгновенно любым мотивированным злоумышленником, который может добраться до вашего физического местоположения за считанные минуты.

Не забудьте проверить [Злоумышленники (угрозы)](# adversarial-considerations) и [Проверьте свою сеть на наличие слежки/цензуры с помощью OONI](#ooni-censorship-check).

Если у вас нет другого выбора и вы все еще хотите что-то сделать, см. [Как насчет того, когда Tor и VPN невозможны?](# tor-vpn-not-possible) **(на свой страх и риск) и вместо этого рассмотрите [маршрут Tails](# tails-route).**

| Тип соединения | Анонимность | Простота доступа к онлайн-ресурсам | Изоляция потока Tor | Безопаснее там, где Tor подозрителен/опасен | Скорость      | Стоимость                      | Рекомендуется                                      |
|------------------------------------|-----------|------------------------------------|----------------------|-----------------------------------------|------------|---------------------------|--------------------------------------------------|
| Tor Alone                          | **Хорошо**  | **Средне**                         | **Возможно**         | **Нет**                                  | **Средне** | **Бесплатно**                  | **Да**                                          |
| Tor по сравнению с VPN | * * Хорошо+ * * | * * Средне * * | * * Возможно * * | * * Да * *                                 | **Средне** | **Около 50 €/г**          | **При необходимости (Tor недоступно)**                 |
| Tor по сравнению с VPN по сравнению с Tor | ** Лучший ** | ** Средний ** | ** Возможный * * | * * Да * * | * * Плохой * * | * *Около 50 €/год**          | **Да**                                          |
| VPN по сравнению с Tor | * * Хорошо- * * | * * Хорошо * * | * * Нет * * | * * Нет * *                                  | **Средний** | **Около 50 €/год**          | **При необходимости (удобство)**                      |
| Self-Hosted VPS VPN/Proxy over Tor | **Хорошо-** | **Очень хорошо**                      | **Нет**               | **Да**                                 | **Средний** | **Около 50 €/год**          | **При необходимости (удобство)**                      |
| VPN/Proxy over Tor over VPN        | **Хорошо-** | **Хорошо**                           | **Нет**               | **Да**                                 | **Плохо**   | **Около 100 €/г**         | **При необходимости (удобство и недоступность Tor)** |
| VPN/Proxy Alone                    | **Плохо**   | **Хорошо**                           | **Н/Д**              | **Да**                                 | **Хорошо**   | **Около 50 €/год**          | **Нет.**                                          |
| Нет Tor и VPN                     | **Плохо**   | **Неизвестно**                        | **Н/Д**              | **Нет**                                  | **Хорошо**   | **Около 100 € (антенна)** | **Нет **                                          |

К сожалению, использование только Tor вызовет подозрение у платформ многих направлений. Вы столкнетесь со многими препятствиями (капчи, ошибки, сложности при регистрации), если будете использовать только Tor. Кроме того, использование Tor там, где вы находитесь, может поставить вас в беду только за это. Но Tor по-прежнему является лучшим решением для анонимности и должен быть где-то для анонимности.

- If you intend to create persistent shared and authenticated identities on various services where access from Tor is hard, we recommend the **VPN over Tor** and **VPS VPN/Proxy over Tor** options (or VPN over Tor over VPN if needed). It might be a bit less secure against correlation attacks due to breaking Tor Stream isolation but provides much better convenience in accessing online resources than just using Tor. It is an "acceptable" trade-off IMHP if you are careful enough with your identity.

    - **Note: It is becoming more common that mainstream services and CDNS are also blocking or hindering VPN users with captchas and other various obstacles**. **In that case, a self-hosted VPS with a VPN/Proxy over Tor is the best solution for this as having your own dedicated VPS guarantees you are the sole user of your IP and encounter little to no obstacles.** Consider a [Self-hosted VPN/Proxy on a Monero/Cash-paid VPS (for users more familiar with Linux)](#anonymous-self-hosted) if you want the least amount of issues (this will be explained in the next section in more details).

- Однако, если вы намерены просто анонимно просматривать случайные сервисы без создания конкретных общих идентификаторов, используйте дружественные сервисы; или если вы не хотите принимать этот компромисс в более раннем варианте. **Затем мы рекомендуем использовать только маршрут Tor, чтобы сохранить все преимущества изоляции потока (или Tor по сравнению с VPN, если это необходимо).**

- Если стоимость является проблемой, мы рекомендуем вариант Tor Only, если это возможно.

- Если доступ к Tor и VPN невозможен или опасен, у вас нет выбора, кроме как безопасно полагаться на общедоступный Wi-Fi. См. [What about when Tor and VPNs are not possible?](#tor-vpn-not-possible)

Для получения дополнительной информации вы также можете ознакомиться с обсуждениями здесь, которые могут помочь вам принять решение:

- Tor Проект: <https://gitlab.torproject.org/legacy/trac/-/wikis/doc/TorPlusVPN> <sup>[[Archive.org]](https://web.archive.org/web/https://gitlab.torproject.org/legacy/trac/-/wikis/doc/TorPlusVPN)</sup>

- Документация Tails:

    - <https://gitlab.tails.boum.org/tails/blueprints/-/wikis/vpn_support/> <sup>[[Archive.org]](https://web.archive.org/web/https://gitlab.tails.boum.org/tails/blueprints/-/wikis/vpn_support/)</sup>

    - <https://tails.boum.org/support/faq/index.en.html#index20h2> <sup>[[Archive.org]](https://web.archive.org/web/https://tails.boum.org/support/faq/index.en.html)</sup>

- Документация Whonix (в следующем порядке):

    - <https://www.whonix.org/wiki/Tunnels/Introduction> <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Tunnels/Introduction)</sup>

    - <https://www.whonix.org/wiki/Tunnels/Connecting_to_Tor_before_a_VPN> <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Tunnels/Connecting_to_Tor_before_a_VPN)</sup>

    - <https://www.whonix.org/wiki/Tunnels/Connecting_to_a_VPN_before_Tor> <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Tunnels/Connecting_to_a_VPN_before_Tor)</sup>

- Некоторые документы по этому вопросу:

    - <https://www.researchgate.net/publication/324251041_Anonymity_communication_VPN_and_Tor_a_comparative_study> <sup>[[Archive.org]](https://web.archive.org/web/https://www.researchgate.net/publication/324251041_Anonymity_communication_VPN_and_Tor_a_comparative_study)</sup>

### Получение анонимного VPN/Proxy { #whonix-anon-vpn }

**Пропустите этот шаг, если вы хотите использовать только Tor.**

См. [Получение анонимного VPN/Proxy](#anonymous-vpn-proxy)

### Whonix { #whonix }

**Пропустите этот шаг, если вы не можете использовать Tor.**

Этот маршрут будет использовать виртуализацию и Whonix как часть процесса анонимизации. Whonix - это распределение Linux, состоящее из двух Virtual Machines:[^353]

- Рабочая станция Whonix (это VM, где вы можете проводить конфиденциальные мероприятия)

- Шлюз Whonix (этот VM установит соединение с сетью Tor и направит весь сетевой трафик с Рабочей станции через сеть Tor).

Таким образом, в этом руководстве будут предложены два варианта этого маршрута:

- Маршрут только Whonix, где весь трафик маршрутизируется через сеть Tor (только Tor или Tor через VPN).

![image27](../media/image27.png)

- Гибридный маршрут Whonix, в котором весь трафик направляется через наличный (предпочтительный)/Monero оплаченный VPN по сети Tor (VPN по Tor или VPN по Tor по VPN).

![image28](../media/image28.png)

Вы сможете решить, какой аромат использовать, основываясь на моих рекомендациях. Мы рекомендуем второй, как объяснялось ранее.

Whonix хорошо обслуживается и имеет обширную и невероятно подробную документацию.

#### Примечание по снимкам Virtualbox { #virtualbox-snapshots }

Позже вы создадите и запустите несколько Virtual Machines в Virtualbox для ваших конфиденциальных действий. Virtualbox предоставляет функцию под названием «Снимки», которая позволяет сохранять состояние VM в любой момент времени. Если по какой-либо причине позже вы захотите вернуться в это состояние, вы можете восстановить этот снимок в любой момент.[^354]

**Настоятельно рекомендуем использовать эту функцию, создав снимок после первоначальной установки/обновления каждого VM. Этот снимок должен быть сделан до его использования для любой конфиденциальной/анонимной деятельности.**

This will allow you to turn your VMs into a kind of disposable "Live Operating Systems" (like Tails discussed earlier). Meaning that you will be able to erase all the traces of your activities within a VM by restoring a Snapshot to an earlier state. Of course, this will not be "as good" as Tails (where everything is stored in memory) as there might be traces of this activity left on your hard disk. Forensics studies have shown the ability to recover data from a reverted VM. Fortunately, there will be ways to remove those traces after the deletion or reverting to an earlier snapshot. Such techniques will be discussed in the [Some additional measures against forensics](#anti-forensics) section of this guide.[^355]

#### Скачать утилиты Virtualbox и Whonix { #download-virtualbox-whonix }

Вы должны скачать несколько вещей в хозяине OS:

- Последняя версия установщика Virtualbox согласно вашему Host OS <https://www.virtualbox.org/wiki/Downloads> <sup>[[Archive.org]](https://web.archive.org/web/https://www.virtualbox.org/wiki/Downloads)</sup>

- (Пропустите это, если вы не можете использовать Tor самостоятельно или через VPN) Последняя стабильная **Whonix 18.x** OVA от:
    - [Выпуски GitHub](https://github.com/Whonix/whonix-gw-ga/releases/latest) <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Download/VirtualBox)</sup>
    - Или официальное зеркало загрузки: <https://download.whonix.org/> (XFCE Desktop рекомендуется для начинающих)
- (Необязательно) [Whonix Text Client](https://www.whonix.org/wiki/Install#Text_Client_Version) <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Install)</sup> доступен для продвинутых пользователей, которые предпочитают минимальную настройку.

**Примечание к Whonix 18.x**: согласно руководству v1.2.5, Whonix был обновлен с версии 17 до 18 (Whonix 18.1.4.x). См. [[Обновление до Whonix 18]](#qubes-whonix18) для пути обновления, если вы в настоящее время используете Whonix 17.x.

На этом подготовка завершится, и теперь вы должны быть готовы приступить к созданию окончательной среды, которая защитит вашу анонимность в Интернете.

#### Упрочнение виртуальной коробки (Whonix 17.x и 18.x) { #virtualbox-hardening }

Для идеальной безопасности следуйте [Руководству по упрочнению Whonix](https://www.whonix.org/wiki/Virtualization_Platform_Security#VirtualBox_Hardening) <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Virtualization_Platform_Security)</sup> со следующими дополнительными примечаниями:

**Рекомендуемые настройки (применяются ко всем VMs):**
- Отключить аудио
- Не включать общие папки
- Отключить 2D-ускорение: `VBoxManage modifyvm "vm-name" --accelerate2dvideo off`
- Отключить 3D-ускорение
- Отключить последовательный порт
- Извлеките дискеты и CD/DVD-дисководы (или установите их в нефункциональное состояние)
- Отключить сервер удаленного отображения
- Включить PAE/NX для функций безопасности
- Отключить ACPI

**Сетевое время Desync:**
Отключите часы VM для предотвращения атак синхронизации (см. [[Whonix Documentation - Network Time Synchronization]](https://www.whonix.org/wiki/Network_Time_Synchronization) <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Network_Time_Synchronization)</sup>):

    ```sh
    # Пример смещения (выберите разные значения для каждого VM)
    VBoxManage modifyvm "Whonix-Gateway-XFCE" --biossystemtimeoffset -35017
    VBoxManage modifyvm "Whonix-Workstation-XFCE" --biossystemtimeoffset +27931
    ```

** Смягчение последствий призрака/расплавления:** (опционально, может повлиять на производительность)
Для получения подробной информации об укреплении Spectre/Meltdown см. <https://www.whonix.org/wiki/Spectre_Meltdown><sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Spectre_Meltdown)</sup>.

**Дополнительное обеспечение:** (Whonix 18.x+)
- Рассмотрите возможность включения AppArmor на рабочей станции Whonix: <https://www.whonix.org/wiki/AppArmor><sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/AppArmor)</sup>
- Обзор рекомендаций [DoNot](https://www.whonix.org/wiki/DoNot)<sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/DoNot)</sup>

- Отключите контроллер USB, который включен по умолчанию. Установите указательное устройство в положение «PS/2 Mouse» (Мышь PS/2), иначе изменения будут возвращены.

Наконец, также следуйте этой рекомендации, чтобы рассинхронизировать часы, вы являетесь вашим VM по сравнению с вашим хостом OS <https://www.whonix.org/wiki/Network_Time_Synchronization#Spoof_the_Initial_Virtual_Hardware_Clock_Offset><sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Network_Time_Synchronization)</sup>

Это смещение должно находиться в диапазоне 60000 миллисекунд и должно быть различным для каждого VM, и вот несколько примеров (которые позже могут быть применены к любому VM):

- ```VBoxManage modifyvm "Whonix-Gateway-XFCE" --biossystemtimeoffset -35017```

- ```VBoxManage modifyvm "Whonix-Gateway-XFCE" --biossystemtimeoffset +27931```

- ```VBoxManage modifyvm "Whonix-Workstation-XFCE" --biossystemtimeoffset -35017```

- ```VBoxManage modifyvm "Whonix-Workstation-XFCE" --biossystemtimeoffset +27931```

Кроме того, рассмотрите возможность применения этих смягчений из VirtualBox для смягчения уязвимостей Spectre/Meltdown, выполнив эту команду из каталога программ VirtualBox. Все это описано здесь: <https://www.whonix.org/wiki/Spectre_Meltdown> <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Spectre_Meltdown)</sup> (имейте в виду, что это может серьезно повлиять на производительность вашего VMs, но должно быть сделано для лучшей безопасности).[^356][^357]

Наконец, рассмотрим советы по безопасности от самих Virtualbox здесь <https://www.virtualbox.org/manual/ch13.html> <sup>[[Archive.org]](https://web.archive.org/web/https://www.virtualbox.org/manual/ch13.html)</sup>

### Tor поверх VPN { #whonix-setup-tor-over-vpn }

**Пропустите этот шаг, если вы не намерены использовать Tor вместо VPN и намерены использовать только Tor или не можете.**

Если вы намерены использовать Tor вместо VPN по какой-либо причине. Сначала вы должны настроить службу VPN на своем хосте OS.

Помните, что в этом случае мы рекомендуем иметь два счета VPN. Оба оплачены наличными/Monero (см. [Получение анонимного VPN/Proxy](#anonymous-vpn-proxy)). Один будет использоваться в Host OS для первого соединения VPN. Другой может быть использован в VM для достижения VPN по сравнению с Tor по сравнению с VPN (Пользователь > VPN > Tor > VPN).

Если вы намерены использовать только Tor через VPN, вам понадобится только одна учетная запись VPN.

Инструкции см. в разделе [Установка VPN на VM или Host OS](# vpn-installation).

### Whonix Virtual Machines { #whonix-vms }

**Пропустите этот шаг, если вы не можете использовать Tor.**

- Запустите Virtualbox на Host OS.

- Импорт OVA Whonix в Virtualbox: См. [VirtualBox/XFCE](https://www.whonix.org/wiki/VirtualBox/XFCE) <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/VirtualBox/XFCE)</sup>
    - Вы также можете использовать версию текстового клиента для продвинутых пользователей

- Запуск Whonix VMs

На этом этапе помните, что если у вас возникли проблемы с подключением к Tor из-за цензуры или блокировки, вам следует рассмотреть возможность подключения с использованием мостов, как описано в [Bridges](https://www.whonix.org/wiki/Bridges) <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Bridges)</sup>.

- Обновите Whonix VMs, следуя инструкциям на [Программное обеспечение и обновления операционной системы](https://www.whonix.org/wiki/Operating_System_Software_and_Updates#Updates) <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Operating_System_Software_and_Updates)</sup>

**Примечание:** Для пользователей Qubes OS обратитесь к разделу [[Обновление до Whonix 18]](#qubes-whonix18) для заметок о миграции.

- Shutdown Whonix VMs

- Сделайте снимок обновленного Whonix VMs в Virtualbox (выберите VM и нажмите кнопку «Сделать снимок»). Подробнее об этом позже.

- Следующий шаг

**Важное примечание: вы также должны прочитать эти очень хорошие рекомендации <https://www.whonix.org/wiki/DoNot> ** <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/DoNot)</sup> **, поскольку большинство из этих принципов также будут применяться к этому руководству. Вы также должны прочитать их общую документацию здесь <https://www.whonix.org/wiki/Documentation>** <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Documentation)</sup> **, которая также предоставит тонны советов, подобных этому руководству.**

### Whonix 18.x Усовершенствования и передовая практика { #whonix-18-improvements }

**Ключевые изменения в Whonix 18.x:**
- Автоматизированный процесс обновления версии для плавных переходов с Whonix 17.x
- Улучшенная интеграция AppArmor для расширенной песочницы приложений в системах на основе Debian
- Улучшенная конфигурация сети с улучшенными возможностями подключения Tor
- Обновленные руководства по усилению безопасности с актуальными рекомендациями
- Улучшенная интеграция и совместимость с Qubes OS

**Рекомендации для пользователей Whonix 18.x:**

1. **Всегда делайте снимок** перед применением любых обновлений системы или изменений конфигурации
2. **Проверка целостности системы ** после обновления с помощью команд `sudo checkvm`
3. ** Регулярно просматривайте страницу DoNot**, чтобы быть в курсе рекомендаций по безопасности
4. **Обновляйте свой Whonix VMs **, используя автоматизированный процесс обновления, когда он доступен
5. **Рассмотрим KVM вместо VirtualBox**

**Для пользователей Qubes OS:**
Поддерживается Qubes R4.2+ с Whonix 18. Всегда проверяйте целостность системы после обновления с помощью `systemcheck`. Подробные инструкции по миграции см. в разделе [[Обновление до Whonix 18]](# qubes-whonix18).

### Выберите гостевую рабочую станцию Virtual Machine { #guest-vm-choice }

Использование Whonix/Linux потребует больше навыков с вашей стороны, поскольку это дистрибутивы Linux. Вы также столкнетесь с большими трудностями, если собираетесь использовать определенное программное обеспечение, которое может быть сложнее использовать на Whonix/Linux. Настройка VPN поверх Tor на Whonix также будет более сложной, чем на Windows.

#### Если вы можете использовать Tor { #guest-tor-yes }

Вы можете решить, предпочитаете ли вы выполнять свои конфиденциальные действия с рабочей станции Whonix, представленной в предыдущем разделе **(настоятельно рекомендуется)**, или с пользовательского VM, который будет использовать шлюз Whonix, такой как рабочая станция Whonix (менее безопасный, но может потребоваться в зависимости от того, что вы собираетесь делать).

#### Если вы не можете использовать Tor { #guest-tor-no }

Если вы не можете использовать Tor, вы можете использовать пользовательский VM по вашему выбору, который в идеале будет использовать анонимный VPN, если это возможно, для подключения к сети Tor. Или вы можете пойти по рискованному пути: см. [What about when Tor and VPNs are not possible?](#tor-vpn-not-possible)

### Linux Virtual Machine (Whonix или Linux) { #linux-vm }

#### Рабочая станция Whonix* *(рекомендуемая и предпочтительная)** { #whonix-workstation }

**Пропустите этот шаг, если вы не можете использовать Tor.**

Просто используйте прилагаемую рабочую станцию Whonix VM. **Это самый безопасный и надежный способ передвижения по этому маршруту.**

**Это также единственный VM, который будет предоставлять изоляцию потока, предварительно настроенную для большинства приложений по умолчанию****.**[^358]

Если вам нужно дополнительное программное обеспечение на рабочей станции (например, другой браузер), следуйте их руководству здесь <https://www.whonix.org/wiki/Install_Software> <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Install_Software)</sup>

Рассмотрите возможность запуска Whonix в режиме реального времени, если для дополнительной защиты от вредоносного ПО см. <https://www.whonix.org/wiki/Anti-Forensics_Precautions><sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Anti-Forensics_Precautions)</sup>

Не забудьте применить рекомендации по закалке VM здесь: [рекомендации по закалке Virtualbox].

Рассмотрите возможность использования AppArmor на своих рабочих станциях Whonix, следуя этому руководству: <https://www.whonix.org/wiki/AppArmor><sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/AppArmor)</sup>

#### Linux (любой дистрибутив) { #linux-any-distro }

**Будьте осторожны, любая настройка, которую вы сделаете для Whonix Guest VMs (раскладка клавиатуры, язык, часовой пояс, разрешение экрана или другое), может быть использована для снятия отпечатков пальцев с вашего VMs позже. См.<https://www.whonix.org/wiki/VM_Fingerprinting>* *<sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/VM_Fingerprinting)</sup>

##### Если вы можете использовать Tor (изначально или поверх VPN) { #linux-vm-tor }

Используйте дистрибутив Linux по вашему выбору. Мы бы порекомендовали Ubuntu или Fedora для удобства, но любой другой тоже подойдет. Не включайте телеметрию.

Подробные инструкции см. в этом руководстве<https://www.whonix.org/wiki/Other_Operating_Systems> <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Other_Operating_Systems)</sup>.

Рассмотрите возможность закалки VM, как рекомендовано в [Закалка Linux].

##### Если вы не можете использовать Tor { #linux-vm-no-tor }

Используйте дистрибутив Linux по вашему выбору. Мы бы порекомендовали Ubuntu или Fedora для удобства, но любой другой тоже подойдет. Не включайте телеметрию. Вы можете пойти по рискованному пути: см. [What about when Tor and VPNs are not possible?](#tor-vpn-not-possible)

##### Выберите браузер в VM { #linux-vm-browser }

На этот раз мы порекомендуем браузер Brave.

Узнайте, почему здесь: [What browser to use in your Guest VM/Disposable VM](#guest-vm-browser-choice)

См. также [Hardening your Browsers](# hardening-browsers).

### Windows 10/11 Virtual Machine { #windows-vm }

**Будьте осторожны, любая настройка, которую вы сделаете для Whonix Guest VMs (раскладка клавиатуры, язык, часовой пояс, разрешение экрана или другое), может быть использована для снятия отпечатков пальцев с вашего VMs позже. См.<https://www.whonix.org/wiki/VM_Fingerprinting>* *<sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/VM_Fingerprinting)</sup>

#### Windows 10 и 11 ISO скачать { #windows-iso-download }

Идите с официальным Windows 10/11 Pro VM и закаляйте его самостоятельно: см. [Windows Installation Media Creation](#win-installation-media) и идите по маршруту ISO.

#### Если вы можете использовать Tor (изначально или поверх VPN) { #windows-vm-tor }

Подробные инструкции см. в этом руководстве<https://www.whonix.org/wiki/Other_Operating_Systems> <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Other_Operating_Systems)</sup>.

##### Установка { #windows-vm-install }

- Выключите шлюз Whonix Gateway VM (это помешает Windows отправлять телеметрию и позволит вам создать локальную учетную запись).

- Открыть Virtualbox

- Выберите Machine > New > Select Windows 10 или Windows 11 64bit

- Выделите минимальное количество 2 ГБ для Windows 10 и 4 ГБ для Windows 11

- Создайте виртуальный диск в формате VDI и выберите Dynamically Allocated

- Держите размер диска на уровне 50 ГБ для Windows 10 и 80 ГБ для Windows 11 (это максимум; он не должен достигать такого уровня)

- Убедитесь, что PAE/NX включен в System > Processor

- Выберите VM и нажмите Настройки, перейдите на вкладку Сеть

- Выберите «Внутренняя сеть» в поле «Прикреплено к» и выберите Whonix.

- Перейдите на вкладку Storage (Хранилище), выберите Empty CD (Пустой компакт-диск) и нажмите значок рядом с SATA Port 1 (Порт S

- Нажмите «Выбрать файл диска» и выберите Windows ISO, который вы ранее загрузили

- Нажмите OK и запустите VM

- Virtualbox предложит вам либо нажать кнопку для загрузки ISO, либо спросить, что загружать, выбрать ISO или нажать.

- Выполните действия в Windows Installation](#windows-installation)

- Запуск шлюза Whonix VM

##### Настройки сети { #windows-vm-network }

- Вернуться к Windows

- Windows 10: Вернитесь в Настройки, затем Сеть и Интернет. Windows 11: Зайдите в настройки, нажмите на верхнее левое меню и выберите «Сеть и Интернет»

- Windows 10: Свойства клика (ниже Ethernet). Windows 11: Нажмите Ethernet

- Windows 10: Изменение настроек IP. Windows 11: Редактирование назначения IP.

- Windows 10: Включите IPv4 и установите следующее, Windows 11: Переключитесь с DHCP на ручной режим и установите следующее:

    - IP-адрес ```10.152.152.50`ZPROT2QQ (увеличьте этот IP-адрес на один для любого другого VM)

    - Длина префикса подсети ```18``` (``ZPROT4QQ``)

    - Шлюз ```10.152.152.10`ZPROT2QQ (это шлюз Whonix)

    - (Windows 10) DNS ```10.152.152.10`ZPROT2QQ (это снова шлюз Whonix)

    - (Windows 11) выйдите из назначения IP и выберите назначение DNS-сервера и установите его на ```10.152.152.10``` (это снова шлюз Whonix)

    - Сохранить

- Windows может подсказывать, хотите ли вы быть «обнаруживаемым» в этой сети. Нажмите «нет». Всегда оставайтесь в «общедоступной сети», если появится соответствующий запрос.

**Каждый раз, когда вы будете включать этот VM в будущем, вы должны обязательно менять его MAC-адрес Ethernet перед каждой загрузкой. Вы можете сделать это в Virtualbox > Настройки > Сеть > Дополнительно > Нажмите кнопку обновления рядом с адресом MAC. Вы можете сделать это только при выключенном VM.**

#### Если вы не можете использовать Tor { #windows-vm-no-tor }

См. [What about when Tor and VPNs are not possible?](#tor-vpn-not-possible)

##### Установка { #windows-vm-no-tor-install }

- Открыть Virtualbox

- Выберите Machine > New > Select Windows 10 or 11 64bit (Машина > Новая > Выберите Windows

- Выделите минимальное количество 4 ГБ RAM для 11 , 2 ГБ RAM для 10.

- Создайте виртуальный диск в формате VDI и выберите Dynamically Allocated

- На вкладке Система/Процессор убедитесь, что включена функция PAE/NX.

- Держите размер диска на уровне 80 ГБ для 11, 50 ГБ для 10 (это максимум; он не должен достигать такого размера)

- Перейдите на вкладку Storage (Хранилище), выберите Empty CD (Пустой компакт-диск) и нажмите значок рядом с SATA Port 1 (Порт S

- Нажмите «Выбрать файл диска» и выберите Windows ISO, который вы ранее загрузили

- Нажмите OK и запустите VM

- Virtualbox предложит вам либо нажать кнопку для загрузки ISO, либо спросить, что загружать, выбрать ISO или нажать.

- Выполните действия, описанные в разделе [Установка Windows](#windows-installation)

##### Настройки сети { #windows-vm-no-tor-network }

- Windows предложит вам, если вы хотите, чтобы вас можно было обнаружить в этой сети. Нажмите NO.

**Каждый раз, когда вы будете включать этот VM в будущем, вы должны обязательно менять его MAC-адрес Ethernet перед каждой загрузкой. Вы можете сделать это в Virtualbox > Настройки > Сеть > Дополнительно > Нажмите кнопку обновления рядом с адресом MAC. Вы можете сделать это только при выключенном VM.**

#### Выберите браузер в VM { #windows-vm-browser }

На этот раз мы порекомендуем браузер Brave.

Узнайте, почему здесь: [What browser to use in your Guest VM/Disposable VM](#guest-vm-browser-choice)

См. также [Hardening your Browsers](# hardening-browsers).

#### Дополнительные настройки конфиденциальности в Windows 10/11 { #windows-vm-privacy }

См. [Дополнительные настройки конфиденциальности Windows](#win-additional-privacy)

### Android Virtual Machine { #android-vm }

Потому что иногда вы хотите запустить мобильный Apps анонимно. Вы также можете настроить Android VM для этой цели. Как и в других случаях, в идеале, этот VM также будет находиться за шлюзом Whonix для сетевого подключения Tor. Но это также можно настроить как VPN вместо Tor вместо VPN

#### Если вы можете использовать Tor (изначально или поверх VPN) { #android-vm-tor }

Позже в настройках VM во время создания перейдите в Сеть и выберите Внутренняя сеть, Whonix.

Затем на самом Android:

- Выберите Wi-Fi

- Выберите VirtWifi для подключения

- Перейти к расширенным свойствам Wi-Fi

- Переключение с DHCP на статический

    - IP-адрес ```10.152.152.50`ZPROT2QQ (увеличьте этот IP-адрес на один для любого другого VM)

    - Длина префикса подсети ```18``` (``ZPROT4QQ``)

    - Шлюз ```10.152.152.10`ZPROT2QQ (это шлюз Whonix)

    - DNS ```10.152.152.10`ZPROT2QQ (это снова шлюз Whonix)

#### Если вы не можете использовать Tor { #android-vm-no-tor }

Просто используйте учебники в том виде, в котором они есть, и посмотрите [What about when Tor and VPNs are not possible?](#tor-vpn-not-possible)

#### Установка { #android-vm-install }

Две возможности: AnBox или Android-x86

Лично мы бы порекомендовали AnBox вместо Android-x86, но для этого требуется Linux

##### AnBox { #anbox }

В основном следуйте инструкциям по установке AnBox на рабочей станции Whonix: <https://www.whonix.org/wiki/Anbox> <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Anbox)</sup> для запуска Android Applications в AnBox VM.

Или следуйте инструкциям здесь <https://anbox.io/> для установки на любой другой VM **(только Linux)**

##### Android-x86 { #android-x86 }

В основном, следуйте инструкциям здесь: <https://www.android-x86.org/documentation/virtualbox.html> <sup>[[Archive.org]](https://web.archive.org/web/https://www.android-x86.org/documentation/virtualbox.html)</sup>

- Загрузите ISO-файл по вашему выбору

- Создайте новый VM.

- Выберите Linux и Linux 2.6 / 3.x / 4.x 64 бит.

- In System

    - Выделить не менее 2048 МБ (2 ГБ) памяти

    - Снимите флажок с накопителя на гибких дисках

    - На вкладке Processor (Процессор) выберите по крайней мере 1 или более CPUs

    - Включить PAE/NX

- В настройках дисплея измените адаптер на VBoxVGA

- В настройках аудио перейдите на Intel HD Audio

- Запустите VM

- Выберите Advanced (Дополнительно), если вы хотите сохранить, Live (Прямой эфир), если вы хотите одноразовую загрузку (и пропустите следующие шаги).

- Выберите Auto Install on Selected Hard Disk (Автоматическая установка на выбранный жесткий

- Выберите Запустить Android.

- Настройте по своему усмотрению (отключите все подсказки для сбора данных). **Рекомендую использовать TaskBar Home.**

- Перейдите в Настройки, Параметры Android-x86 и отключите все коллекции.

- Подключитесь к сети VirtWifi Wi-Fi **(см. раздел выше, если вы стоите за Whonix и хотите использовать Tor)**

Теперь вы можете установить любое приложение для Android.

### macOS Virtual Machine { #macos-vm }

Да, вы можете запустить macOS в Virtualbox (на хост-системах Windows/Linux/macOS), если хотите использовать macOS. Вы можете запустить любую версию macOS.

#### Если вы можете использовать Tor (изначально или поверх VPN) { #macos-vm-tor }

Во время следующих уроков перед запуском macOS VM убедитесь, что вы поместили macOS VMs в сеть Whonix.

- Выберите VM и нажмите Настройки, перейдите на вкладку Сеть

- Выберите «Внутренняя сеть» в поле «Прикреплено к» и выберите Whonix

После этого и во время установки вам нужно будет ввести IP-адрес вручную, чтобы подключиться через шлюз Whonix.

Используйте следующие настройки при появлении запроса в процессе установки macOS:

- IP-адрес ```10.152.152.50`ZPROT2QQ (увеличьте этот IP-адрес на один для любого другого VM)

- Длина префикса подсети ```18``` (``ZPROT4QQ``)

- Шлюз ```10.152.152.10`ZPROT2QQ (это шлюз Whonix)

- DNS ```10.152.152.10`ZPROT2QQ (это снова шлюз Whonix)

#### Если вы не можете использовать Tor { #macos-vm-no-tor }

Просто используйте учебники в том виде, в котором они есть, и посмотрите [What about when Tor and VPNs are not possible?](#tor-vpn-not-possible)

#### Установка { #macos-vm-install }

- Windows Host OS:

    - Учебник по Virtualbox Catalina: <https://www.wikigain.com/install-macos-catalina-on-virtualbox-on-windows/><sup>[[Archive.org]](https://web.archive.org/web/https://www.wikigain.com/install-macos-catalina-on-virtualbox-on-windows/)</sup>

    - Учебник по Virtualbox Big Sur: <https://www.wikigain.com/how-to-install-macos-big-sur-on-virtualbox-on-windows-pc/><sup>[[Archive.org]](https://web.archive.org/web/https://www.wikigain.com/how-to-install-macos-big-sur-on-virtualbox-on-windows-pc/)</sup>

    - Учебное пособие по Virtualbox Monterey: <https://www.wikigain.com/install-macos-monterey-on-virtualbox/><sup>[[Archive.org]](https://web.archive.org/web/https://www.wikigain.com/install-macos-monterey-on-virtualbox/)</sup>

- macOS Host OS:

    - Просто используйте те же инструкции, что и выше, но выполняйте различные команды в терминале. Он должен работать без проблем.

- Linux Host OS:

    - Просто используйте те же инструкции, что и выше, но выполняйте различные команды в терминале. Он должен работать без проблем.

There are some drawbacks to running macOS on Virtual Machines. The main one is that they do not have a serial number (0 by default) and you will be unable to log in to any Apple-provided service (iCloud, iMessage...) without a genuine ID. You can set such IDs using this script: <https://github.com/myspaghetti/macos-virtualbox> <sup>[[Archive.org]](https://web.archive.org/web/https://github.com/myspaghetti/macos-virtualbox)</sup> but keep in mind that randomly generated IDs will not work and using the ID of someone else will break their Terms of Services and could count as impersonation (and therefore could be illegal).

Примечание. Мы также столкнулись с несколькими проблемами при их запуске на процессорах AMD. Это можно исправить, поэтому вот конфигурация Weused, которая отлично работала с Catalina, Big Sur и Monterey, которая скажет Virtualbox эмулировать процессор Intel вместо этого:

- ```VBoxManage modifyvm "macOSCatalina" ---cpuidset 00000001 000106e5 00100800 0098e3fd bfebfbff```

- ```VBoxManage setextradata "macOSCatalina" "VBoxInternal/Devices/efi/0/Config/DmiSystemProduct" "MacBookPro15,1" ```

- ```VBoxManage setextradata "macOSCatalina" "VBoxInternal/Devices/efi/0/Config/DmiBoardProduct" "Mac-551B86E5744E2388"```

- ```VBoxManage setextradata "macOSCatalina" "VBoxInternal/Devices/smc/0/Config/DeviceKey" "ourhardworkbythesewordsguardedpleasedontsteal(c)AppleComputerInc"```

- ```VBoxManage setextradata "macOSCatalina" "VBoxInternal/Devices/smc/0/Config/GetKeyFromRealSMC" 1```

- ```VBoxManage modifyvm "macOSCatalina" --cpu-profile "Intel Core i7-6700K"```

- ```VBoxManage setextradata "macOSCatalina" VBoxInternal2/EfiGraphicsResolution 1920x1080```

#### Закалка macOS { #macos-vm-hardening }

См. [Закалка macOS].

#### Выберите браузер в VM { #macos-vm-browser }

На этот раз мы порекомендуем браузер Brave.

Узнайте, почему здесь: [What browser to use in your Guest VM/Disposable VM](#guest-vm-browser-choice)

См. также [Hardening your Browsers](# hardening-browsers).

### KeepassXC { #keepassxc }

Вам понадобится что-то для хранения ваших данных (логины/пароли, удостоверения личности и информация TOTP).[^359]

Для этой цели мы настоятельно рекомендуем KeePassXC из-за его интегрированной функции TOTP. Это возможность создавать записи для аутентификации 2FA с помощью функции аутентификации.[^360]

Помните, что в идеале он должен быть установлен на вашем гостевом VM, а не на Host OS. Вы никогда не должны выполнять какие-либо деликатные действия из своего Host OS.

Вот учебные пособия:

- Tails: KeePassXC интегрирован по умолчанию

- Whonix: <https://www.whonix.org/wiki/Keepassxc> <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Keepassxc)</sup>

- Linux:

    - Загрузить с <https://keepassxc.org/download/> <sup>[[Archive.org]](https://web.archive.org/web/https://keepassxc.org/download/)</sup>

    - Следуйте инструкциям здесь <https://keepassxc.org/docs/KeePassXC_GettingStarted.html#_linux> <sup>[[Archive.org]](https://web.archive.org/web/https://keepassxc.org/docs/KeePassXC_GettingStarted.html)</sup>

- Windows:

    - Загрузить с <https://keepassxc.org/download/> <sup>[[Archive.org]](https://web.archive.org/web/https://keepassxc.org/download/)</sup>

    - Следуйте инструкциям здесь <https://KeePassXC.org/docs/KeePassXC_GettingStarted.html#_microsoft_windows/> <sup>[[Archive.org]](https://web.archive.org/web/https://keepassxc.org/docs/KeePassXC_GettingStarted.html)</sup>

- macOS:

    - Загрузить с <https://keepassxc.org/download/> <sup>[[Archive.org]](https://web.archive.org/web/https://keepassxc.org/download/)</sup>

    - Следуйте инструкциям здесь <https://keepassxc.org/docs/KeePassXC_GettingStarted.html#_macos> <sup>[[Archive.org]](https://web.archive.org/web/https://keepassxc.org/docs/KeePassXC_GettingStarted.html)</sup>

Проверьте, что KeePassXC работает, прежде чем переходить к следующему шагу.

### Установка клиента VPN (оплачено наличными/Monero) { #vpn-client-install }

**Если вы решили не использовать оплаченный наличными VPN и просто хотите использовать Tor, пропустите этот шаг.**

**Если вы вообще не можете использовать VPN во враждебной среде, пропустите этот шаг.**

В противном случае см. [Установка VPN на ваш VM или Host OS](#vpn-installation), чтобы установить клиент VPN на ваш клиент VM.

На этом маршрут должен завершиться, и теперь вы должны быть готовы.

#### О VPN Client Data Mining/Leaks { #vpn-client-leaks }

Вы можете спросить себя, заслуживают ли доверия эти клиенты VPN, чтобы не сливать какую-либо информацию о вашей локальной среде провайдеру VPN при использовании их в контексте «VPN через Tor».

Это серьезная проблема, но ее следует принимать с недоверием.

Remember that all VPN activities are happening from a sandboxed VM on an internal network behind a Network Gateway (the Whonix Gateway). It does not matter much if the VPN client leaves some identifiers on your guest VM. The guest VM is still sandboxed and walled-off from the Host OS. The attack surface is small especially when using the reputable and recommended VPN providers within the guides (iVPN, Mullvad, Proton VPN, and maybe Safing.io).

В лучшем случае клиент VPN будет знать ваш локальный IP-адрес (внутренний IP-адрес) и некоторые рандомизированные идентификаторы, но не сможет получить что-либо от Host OS. И теоретически клиент VPN не должен отправлять какую-либо телеметрию обратно провайдеру VPN. Если ваш клиент VPN делает это или спрашивает об этом, вам следует рассмотреть возможность смены поставщика.

### (Дополнительно) VM аварийный выключатель { #vm-kill-switch }

Этот шаг позволит вам настроить Host OS таким образом, чтобы только шлюз Whonix VM имел доступ к Интернету. Таким образом, это предотвратит любую «утечку» из вашего Host OS, позволяя шлюзу Whonix установить подключение Tor. Другая VMs (рабочая станция Whonix или любая другая VM, установленная за ней, не будет затронута)

Есть три основных способа сделать это: 

- Ленивый путь (не рекомендуется): не поддерживается Whonix и может иметь некоторые последствия для безопасности, поскольку вы предоставите шлюз Whonix VM в публичную сеть Wi-Fi. Мы не рекомендуем этого делать, если вы не торопитесь или не ленитесь.

    - **Этот метод не будет работать с порталами Wi-Fi, требующими какой-либо регистрации для подключения.**

- Лучший способ (см. далее): все еще не поддерживается Whonix, но он не предоставит шлюз Whonix VM публичной сети Wi-Fi. Это должно держать ситуацию под контролем с точки зрения безопасности.

- Лучший способ: использовать внешний ключ USB Wi-Fi и просто отключить Wi-Fi на Host OS/Computer.

#### Ленивый путь { #kill-switch-lazy }

> Не поддерживается Whonix

**Этот путь не поддерживается проектом Whonix **, но я все равно дам эту опцию. Это полезно для предотвращения утечки любой информации из вашего Host OS во время использования Whonix VMs.[^361]

**Обратите внимание, что эта опция как есть будет работать только на Wi-Fis без кэптивного портала (где вы должны ввести некоторую информацию, чтобы разблокировать доступ).**

На приведенном ниже рисунке показан результат этого шага:

![image29](../media/image29.png)

##### Конфигурация шлюза Whonix VM { #lazy-whonix-gw-config }

Чтобы это работало, нам нужно будет изменить некоторые конфигурации на шлюзе Whonix VM. Нам нужно будет добавить DHCP-клиент на шлюз Whonix для получения IP-адресов из сети. Для внесения этих изменений Host OS по-прежнему должен иметь доступ в Интернет.

Версия:

- Убедитесь, что ваш Host OS подключен к безопасному Wi-Fi.

- Через VirtualBox запустите шлюз Whonix VM

- Запустите терминал на VM

- Установите DHCP-клиент на шлюз Whonix VM с помощью следующей команды:

    - ```sudo apt install dhcpcd5```

- Теперь отредактируйте конфигурацию сети Whonix Gateway VM с помощью следующей команды:

    - ```sudo nano /etc/network/interfaces.d/30_non-qubes-whonix```

- В файле измените следующие строки:

    - ```# auto eth0``` до ``ZPROT4QQ``

    - ```# iface eth0 inet dhcp``` до ``ZPROT4QQ``

    - ```iface eth0 inet static``` до ``ZPROT4QQ``

    - ``` address 10.0.2.15``` до ``ZPROT4QQ``

    - ``` netmask 255.255.255.0``` до ``ZPROT4QQ``

    - ``` gateway 10.0.2.2``` до ``ZPROT4QQ``

- Сохранить (используя Ctrl+X и подтвердить с помощью Y) и выключить VM из верхнего левого меню

- Перейдите в VirtualBox App и выберите шлюз Whonix VM

- Откроется окно Угрозы .

- Перейдите на вкладку Network (Сеть

- Для адаптера 1 измените значение «Присоединено к» с «NAT» на «Мостовой адаптер»

- В качестве "Имя" выберите сетевой адаптер Wi-Fi

- Нажмите OK, и вы закончите с частью конфигурации VM

##### Конфигурация Host OS { #lazy-host-config }

Теперь вы должны заблокировать доступ в Интернет со своего Host OS, все еще позволяя VM подключаться. Это будет сделано путем подключения к Wi-Fi с помощью Host OS, но без назначения себе IP-адреса. Затем VM будет использовать вашу ассоциацию Wi-Fi для получения IP-адреса.

###### Windows Host OS { #lazy-windows-host }

Цель здесь - подключиться к сети Wi-Fi без подключения к Интернету. Вы достигнете этого, удалив шлюз из подключения после подключения:

- Сначала подключитесь к сейфу Wi-Fi по вашему выбору

- Откройте командную строку администратора (щелкните правой кнопкой мыши на командной строке и запустите от имени администратора)

- Выполните следующую команду: ```route delete 0.0.0.0``` (это удалит шлюз из вашей конфигурации IP)

- Готово, ваш Host OS теперь не сможет получить доступ к Интернету, пока он все еще подключен к Wi-Fi

    - Обратите внимание, что это будет сбрасываться при каждом отключении/повторном подключении к сети, и вам придется снова удалять маршрут. Это не навсегда.

- Теперь вы можете запустить шлюз Whonix Gateway VM, который теперь должен автоматически получать IP-адрес из сети Wi-Fi и должен предоставлять сеть другому VMs сзади (рабочая станция Whonix или другая).

- И, наконец, после этого вы можете запустить Whonix Workstation VM (или любой другой VM, который вы настроили для работы за Whonix Gateway VM), и он должен быть подключен к Интернету через Tor.

###### Linux Host OS { #lazy-linux-host }

Цель здесь - подключиться к сети Wi-Fi без подключения к Интернету. Вы достигнете этого, удалив шлюз из подключения после подключения:

- Сначала подключитесь к сейфу Wi-Fi по вашему выбору

- Открыть терминал

- Выполните следующую команду: ```sudo ip route del default``` (это удалит шлюз из вашей конфигурации IP)

- Готово, ваш Host OS теперь не сможет получить доступ к Интернету, пока он все еще подключен к Wi-Fi

    - Обратите внимание, что это будет сбрасываться при каждом отключении/повторном подключении к сети, и вам придется снова удалять маршрут. Это не навсегда.

- Теперь вы можете запустить шлюз Whonix Gateway VM, который теперь должен автоматически получать IP-адрес из сети Wi-Fi и должен предоставлять сеть другому VMs сзади (рабочая станция Whonix или другая).

- И, наконец, после этого вы можете запустить Whonix Workstation VM (или любой другой VM, который вы настроили для работы за Whonix Gateway VM), и он должен быть подключен к Интернету через Tor.

###### macOS Host OS { #lazy-macos-host }

Цель здесь - подключиться к сети Wi-Fi без подключения к Интернету. Вы достигнете этого, удалив шлюз из подключения после подключения:

- Сначала подключитесь к сейфу Wi-Fi по вашему выбору

- Открыть терминал

- Выполните следующую команду: ```sudo route delete default``` (это удалит шлюз из вашей конфигурации IP)

- Готово, ваш Host OS теперь не сможет получить доступ к Интернету, пока он все еще подключен к Wi-Fi

    - Обратите внимание, что это будет сбрасываться при каждом отключении/повторном подключении к сети, и вам придется снова удалять маршрут. Это не навсегда.

- Теперь вы можете запустить шлюз Whonix Gateway VM, который теперь должен автоматически получать IP-адрес из сети Wi-Fi и должен предоставлять сеть другому VMs сзади (рабочая станция Whonix или другая).

- И, наконец, после этого вы можете запустить Whonix Workstation VM (или любой другой VM, который вы настроили для работы за Whonix Gateway VM), и он должен быть подключен к Интернету через Tor.

#### Лучший способ (рекомендуется) { #kill-switch-better }

Этот способ не будет противоречить рекомендациям Whonix (поскольку он не будет раскрывать шлюз Whonix для Host OS) и будет иметь то преимущество, что позволит соединениям не только открывать Wi-Fis, но и подключаться к порталу Captive, где вам нужно ввести некоторую информацию для доступа в Интернет.

Тем не менее, это все еще не будет поддерживаться проектом Whonix, но это нормально, поскольку основная проблема для более раннего Lazy Way заключается в том, чтобы шлюз Whonix VM был открыт для сети Host, и здесь этого не будет.

Эта опция потребует, чтобы дополнительный VM между Host OS и шлюзом Whonix выступал в качестве сетевого моста.

Для этого я порекомендую использовать легкий Linux Distro. Любой подойдет, но самым простым будет дистрибутив на основе Ubuntu, и я бы порекомендовал легкий XUbuntu, так как его будет чрезвычайно легко настроить.

Почему именно XUbuntu, а не Ubuntu или KUbuntu? Поскольку XUbuntu использует среду рабочего стола XFCE, которая является легкой, и этот VM будет служить только прокси-сервером и ничем другим.

Конечно, вы также можете достичь этого с любым другим дистрибутивом Linux, если решите, что вам не нравится XUbuntu.

Вот как это будет выглядеть в конце:

![image30](../media/image30.png)

##### Установка XUbuntu VM { #xubuntu-install }

XUbuntu был выбран из-за производительности XFCE.

Убедитесь, что вы подключены к безопасному Wi-Fi для этой операции.

Сначала вам нужно будет загрузить последнюю версию XUbuntu Stable release ISO из <https://xubuntu.org/download/>

Когда вы закончите загрузку, пришло время создать новый VM:

- Запуск менеджера VirtualBox

- Создайте новый VM и назовите его так, как вы хотите, например, «Мост XUbuntu»

- Выберите тип "Linux"

- Выберите версию "Ubuntu (64-bit)"

- Оставьте другие параметры по умолчанию и нажмите Создать.

- На следующем экране оставьте параметры по умолчанию и нажмите Создать.

- Выберите вновь созданный VM и нажмите Настройки

- Выберите сеть

- Для адаптера 1 переключитесь в мостовой режим и выберите адаптер Wi-Fi в поле Имя

- Выберите Адаптер 2 и включите его

- Прикрепите его к «Внутренней сети» и назовите «Мост XUbuntu»

- Выберите хранилище

- Выберите дисковод для пустых компакт-дисков

- В правой части нажмите на значок компакт-диска и выберите «Выбрать файл диска»

- Выберите ISO XUbuntu, который вы загрузили ранее, и нажмите OK

- Запустите VM

- Выберите Start XUbuntu

- Выберите Установить XUbuntu

- Выберите раскладку клавиатуры и нажмите Продолжить.

- Выберите Минимальная установка и загрузка обновлений при установке XUbuntu

- Выберите Erase Disk (Стереть диск) и установите XUbuntu, а затем нажмите Install Now (Установить сейчас)

- Выберите часовой пояс и нажмите Продолжить.

- Выберите несколько случайных имен, не связанных с вами (мое любимое имя пользователя - "NoSuchAccount")

- Выберите пароль и потребуйте пароль для входа в систему

- Нажмите Продолжить и дождитесь завершения установки и перезагрузки

- После перезагрузки войдите в систему

- Нажмите на верхний правый значок соединения (он выглядит как две вращающиеся сферы)

- Нажмите Редактировать подключения.

- Выберите проводное соединение 2 (адаптер 2 ранее настроен в настройках VirtualBox)

- Выберите вкладку IPv4

- Измените Метод на «Общий доступ к другим компьютерам» и нажмите Сохранить

- Вы завершили настройку моста XUbuntu Bridge VM

##### Настройка шлюза Whonix VM { #better-whonix-gw-config }

По умолчанию шлюз Whonix не имеет DHCP-клиента и ему потребуется получить IP-адрес из общей сети, настроенной ранее:

- Через VirtualBox запустите шлюз Whonix VM

- Запустите терминал на VM

- Установите DHCP-клиент на шлюз Whonix VM с помощью следующей команды:

    - ```sudo apt install dhcpcd5```

- Теперь отредактируйте конфигурацию сети Whonix Gateway VM с помощью следующей команды:

    - ```sudo nano /etc/network/interfaces.d/30_non-qubes-whonix```

- В файле измените следующие строки:

    - ```# auto eth0``` до ``ZPROT4QQ``

    - ```# iface eth0 inet dhcp``` до ``ZPROT4QQ``

    - ```iface eth0 inet static``` до ``ZPROT4QQ``

    - ``` address 10.0.2.15``` до ``ZPROT4QQ``

    - ``` netmask 255.255.255.0``` до ``ZPROT4QQ``

    - ``` gateway 10.0.2.2``` до ``ZPROT4QQ``

- Сохранить (используя Ctrl+X и подтвердить с помощью Y) и выключить VM из верхнего левого меню

- Перейдите в VirtualBox App и выберите шлюз Whonix VM

- Откроется окно Угрозы .

- Перейдите на вкладку Network (Сеть

- Для адаптера 1 измените значение "Attached To" с "NAT" на "Internal Network"

- В качестве "Name" выберите внутреннюю сеть "XUbuntu Bridge", которую вы создали ранее, и нажмите OK

- Перезагрузите шлюз Whonix VM

- В верхнем левом меню выберите System (Система), Tor Control Panel (Панель управления Tor) и убедитесь, что вы подключены (вы должны быть)

- Вы завершили настройку шлюза Whonix VM

##### Конфигурация Host OS { #better-host-config }

Теперь вы должны заблокировать доступ в Интернет со своего Host OS, все еще позволяя подключаться к мосту XUbuntu VM. Это будет сделано путем подключения к Wi-Fi с помощью Host OS, но без назначения себе адреса шлюза. Затем VM будет использовать вашу ассоциацию Wi-Fi для получения IP-адреса.

При необходимости с моста XUbuntu Bridge VM вы сможете запустить Браузер для ввода информации в любой кэптивный/регистрационный портал в сети Wi-Fi.

Только XUbuntu Bridge VM должен иметь доступ к Интернету. Host OS будет ограничен только местным трафиком.

###### Windows Host OS { #better-windows-host }

Цель здесь - подключиться к сети Wi-Fi без подключения к Интернету. Вы достигнете этого, удалив шлюз из подключения после подключения:

- Сначала подключитесь к сейфу Wi-Fi по вашему выбору

- Откройте командную строку администратора (щелкните правой кнопкой мыши на командной строке и запустите от имени администратора)

- Выполните следующую команду: ```route delete 0.0.0.0``` (это удалит шлюз из вашей конфигурации IP)

- Готово, ваш Host OS теперь не сможет получить доступ к Интернету, пока он все еще подключен к Wi-Fi

    - Обратите внимание, что это будет сбрасываться при каждом отключении/повторном подключении к сети, и вам придется снова удалять маршрут. Это не навсегда.

- Теперь вы можете запустить мост XUbuntu Bridge VM, который теперь должен автоматически получать IP-адрес из сети Wi-Fi и должен предоставлять сеть другому VMs позади (рабочая станция Whonix или другая).

- При необходимости вы можете использовать браузер XUbuntu Bridge VM для заполнения любой информации на любом портале регистрации/регистрации для доступа к Wi-Fi.

- После этого вы можете запустить шлюз Whonix VM, который должен получить подключение к Интернету от моста XUbuntu VM.

- И, наконец, после этого вы можете запустить Whonix Workstation VM (или любой другой VM, который вы настроили для работы за Whonix Gateway VM), и он должен быть подключен к Интернету через Tor.

###### Linux Host OS { #better-linux-host }

Цель здесь - подключиться к сети Wi-Fi без подключения к Интернету. Вы достигнете этого, удалив шлюз из подключения после подключения:

- Сначала подключитесь к сейфу Wi-Fi по вашему выбору

- Open a Terminal

- Выполните следующую команду: ```sudo ip route del default``` (это удалит шлюз из вашей конфигурации IP)

- Готово, ваш Host OS теперь не сможет получить доступ к Интернету, пока он все еще подключен к Wi-Fi

    - Обратите внимание, что это будет сбрасываться при каждом отключении/повторном подключении к сети, и вам придется снова удалять маршрут. Это не навсегда.

- Теперь вы можете запустить мост XUbuntu Bridge VM, который теперь должен автоматически получать IP-адрес из сети Wi-Fi и должен предоставлять сеть другому VMs позади (рабочая станция Whonix или другая).

- При необходимости вы можете использовать браузер XUbuntu Bridge VM для заполнения любой информации на любом портале регистрации/регистрации для доступа к Wi-Fi.

- После этого вы можете запустить шлюз Whonix VM, который должен получить подключение к Интернету от моста XUbuntu VM.

- И, наконец, после этого вы можете запустить Whonix Workstation VM (или любой другой VM, который вы настроили для работы за Whonix Gateway VM), и он должен быть подключен к Интернету через Tor.

###### macOS Host OS { #better-macos-host }

The goal here is to associate with a Wi-Fi network without having an internet connection. You will achieve this by deleting the Gateway from the connection after you are connected:

- Сначала подключитесь к сейфу Wi-Fi по вашему выбору

- Открыть терминал

- Выполните следующую команду: ```sudo route delete default``` (это удалит шлюз из вашей конфигурации IP)

- Готово, ваш Host OS теперь не сможет получить доступ к Интернету, пока он все еще подключен к Wi-Fi

    - Обратите внимание, что это будет сбрасываться при каждом отключении/повторном подключении к сети, и вам придется снова удалять маршрут. Это не навсегда.

- Теперь вы можете запустить мост XUbuntu Bridge VM, который теперь должен автоматически получать IP-адрес из сети Wi-Fi и должен предоставлять сеть другому VMs позади (рабочая станция Whonix или другая).

- If necessary, you can use the XUbuntu Bridge VM Browser to fill in any information on any captive/registration portal to access the Wi-Fi.

- После этого вы можете запустить шлюз Whonix VM, который должен получить подключение к Интернету от моста XUbuntu VM.

- И, наконец, после этого вы можете запустить Whonix Workstation VM (или любой другой VM, который вы настроили для работы за Whonix Gateway VM), и он должен быть подключен к Интернету через Tor.

#### Лучший способ { #kill-switch-best }

This way will not go against Whonix recommendations (as it will not expose the Whonix Gateway to the Host OS) and will have the advantage of allowing connections not only to open Wi-Fis but also to the ones with a Captive Portal where you need to enter some information to access the internet. Yet this will still not be supported by the Whonix project, but it is fine as the main concern for the earlier Lazy Way is to have the Whonix Gateway VM exposed to the Host Network, and it will not be the case here. This option is the best because the network will be completely disabled on the Host OS from booting up.

Эта опция потребует дополнительного VM между Host OS и шлюзом Whonix для выполнения функций сетевого моста и подключения к сети Wi-Fi. **Для этого варианта требуется работающий ключ USB Wi-Fi, который будет пропущен через мост VM.**

Для этого я порекомендую использовать легкий Linux Distro. Любой подойдет, но самым простым будет дистрибутив на основе Ubuntu, и я бы порекомендовал легкий XUbuntu, так как его будет чрезвычайно легко настроить.

Why XUbuntu and not Ubuntu or KUbuntu? Because XUbuntu uses an XFCE desktop environment which is lightweight and this VM will only serve as a proxy and nothing else.

Конечно, вы также можете достичь этого с любым другим дистрибутивом Linux, если решите, что вам не нравится XUbuntu.

Вот как это будет выглядеть в конце:

![image31](../media/image31.png)

##### Конфигурация Host OS { #best-host-config }

- Полностью отключите сеть на своем Host OS (полностью отключите встроенный Wi-Fi)

- Подключите и установите ключ USB Wi-Fi. Подключите его к безопасному публичному Wi-Fi. Это должно быть легко и автоматически установлено любым недавним OS (Windows 10/11, macOS, Linux).

##### Настройка шлюза Whonix VM { #best-whonix-gw-config }

По умолчанию шлюз Whonix не имеет DHCP-клиента и ему потребуется получить IP-адрес из общей сети, которую вы настроите позже, на мосту VM:

- Через VirtualBox запустите шлюз Whonix VM

- Запустите терминал на VM

- Установите DHCP-клиент на шлюз Whonix VM с помощью следующей команды:

    - ```sudo apt install dhcpcd5```

- Теперь отредактируйте конфигурацию сети Whonix Gateway VM с помощью следующей команды:

    - ```sudo nano /etc/network/interfaces.d/30_non-qubes-whonix```

- В файле измените следующие строки:

    - ```# auto eth0``` to ```auto eth0```

    - ```# iface eth0 inet dhcp``` до ``ZPROT4QQ``

    - ```iface eth0 inet static``` до ``ZPROT4QQ``

    - ``` address 10.0.2.15``` до ``ZPROT4QQ``

    - ``` netmask 255.255.255.0``` до ``ZPROT4QQ``

    - ``` gateway 10.0.2.2``` до ``ZPROT4QQ``

- Save (using Ctrl+X and confirm with Y) and power off the VM from the top left menu

##### Installing XUbuntu VM { #best-xubuntu-install }

Make sure you are connected to a safe Wi-Fi for this operation.

First, you will need to download the latest XUbuntu Stable release ISO from <https://xubuntu.org/download/>

When you are done with the download, it is time to create a new VM:

- Disconnect your host OS from the Wi-Fi you previously connected to with the dongle and forget the network.

- Start VirtualBox Manager

- Create a new VM and name it as you want, for example, "XUbuntu Bridge"

- Выберите тип "Linux"

- Выберите версию "Ubuntu (64-bit)"

- Leave other options to default and click Create

- On the next screen, leave the default options and click Create

- Select the newly create VM and click Settings

- Select Network

- Для адаптера 1 присоедините его к «Внутренней сети» и назовите «Мост XUbuntu»

- Выберите хранилище

- Выберите дисковод для пустых компакт-дисков

- On the right side, click the CD icon and select "Choose a disk file"

- Выберите ISO XUbuntu, который вы загрузили ранее, и нажмите OK

- Выберите вкладку USB

- On the right side, click the USB icon with a + sign (the second from the top)

- Выберите ключ адаптера Wi-Fi из списка и убедитесь, что он установлен (оставьте параметры USB по умолчанию)

- Запустите VM

- Выберите Start XUbuntu

- Выберите Установить XUbuntu

- Выберите раскладку клавиатуры и нажмите Продолжить.

- Select Minimal Installation and do not check the Download Updates during the install option

- Select Erase Disk and install XUbuntu and click Install Now

- Выберите часовой пояс и нажмите Продолжить.

- Pick some random names unrelated to you (my favorite username is "NoSuchAccount")

- Выберите пароль и потребуйте пароль для входа в систему

- Нажмите Продолжить и дождитесь завершения установки и перезагрузки

- После перезагрузки войдите в систему

- Нажмите на верхний правый значок соединения (он выглядит как две вращающиеся сферы)

- Нажмите Редактировать подключения.

- Select Wired Connection 1 (normally there should only be one)

- Выберите вкладку IPv4

- Change the Method to "Shared to other computers" and click Save

- Again, click the upper right connection icon

- Подключитесь к выбранному вами сейфу Wi-Fi и при необходимости введите необходимую информацию в Captive Portal.

- Вы завершили настройку моста XUbuntu Bridge VM

На этом этапе ваше Host OS должно вообще не иметь сети, а ваше XUbuntu VM должно иметь полностью рабочее соединение Wi-Fi, и это соединение Wi-Fi будет совместно использоваться с внутренней сетью "XUbuntu Bridge".

##### Additional configuration of the Whonix Gateway VM { #best-whonix-gw-extra }

Теперь пришло время настроить шлюз Whonix VM для получения доступа из общей сети с моста VM, который вы только что сделали на более раннем шаге:

- Go into the VirtualBox Application and select the Whonix Gateway VM

- Откроется окно Угрозы .

- Click the Network Tab

- For Adapter 1, change the "Attached To" value from "NAT" to "Internal Network"

- As "Name", select the internal network "XUbuntu Bridge" you created earlier and click OK

- Перезагрузите шлюз Whonix VM

- From the upper left menu, select System, Tor Control Panel, and check that you are connected (you should be)

- You are done configuring the Whonix Gateway VM

На этом этапе ваш шлюз Whonix VM должен получать доступ в Интернет от моста XUbuntu VM, который, в свою очередь, получает доступ в Интернет от ключа Wi-Fi и делится им. Ваш Host OS вообще не должен иметь сетевого подключения.

Все VMs за шлюзом Whonix теперь должны работать нормально без дополнительной настройки.

**Сделайте снимок вашего VMs после установки VirtualBox.**

You are done and can now skip the rest to go to the [Getting Online](#getting-online) part.

