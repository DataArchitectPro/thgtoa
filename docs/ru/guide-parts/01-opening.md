---
title: "The Hitchhiker's Guide"
description: We are the maintainers of the Hitchhiker's Guide and the PSA Matrix space.
hide:
  - navigation
schema:
  "@context": https://schema.org
  "@type": Organization
  "@id": https://anonymousplanet.net/
  name: Anonymous Planet
  url: https://anonymousplanet.net/guide/
  logo: ../media/profile.png
  sameAs:
    - https://github.com/Anon-Planet
    - https://opencollective.com/anonymousplanetorg
---

<div class="guide-intro-lead" markdown="1">

1. **Do you want to understand the current state of online privacy and anonymity, while not necessarily getting too technical about it?**
    - Read the [Introduction](#introduction), [Requirements](#requirements-limitations), understanding some basics beginning with [your network](#network), and [the final notes](#final-note).

2. **Do you want to learn, but also learn how to remove some online information about you?**
    - All of the items in no. 1 and [how to clean your identities from search engines and other platforms](#removing-identities) to get a good idea of how to clean your data off the web.

3. **Do you want to do the above and create online anonymous identities online safely and securely.**
    - Read the whole thing. A specific list of the most vital things to read in the guide will be coming later, but you should read the whole thing.

## Precautions while reading this guide and accessing the various links { #precautions }

- **YouTube Videos** have a **[Invidious]** link next to them for accessing content through an Invidious Instance (in this case yewtu.be hosted in the Netherlands) for increased privacy. It is recommended to use these links when possible. See <https://github.com/iv-org/invidious> <sup>[[Archive.org]](https://web.archive.org/web/https://github.com/iv-org/invidious)</sup> for more information.

- **Twitter** links have a **[Nitter]** link next to them for accessing content through a Nitter Instance (in this case nitter.net) for increased privacy. It is recommended to use these links when possible. See <https://github.com/zedeus/nitter> <sup>[[Archive.org]](https://web.archive.org/web/https://github.com/zedeus/nitter)</sup> for more information.

- **Wikipedia** links have a **[Wikiless]** link next to them for accessing content through a Wikiless Instance (in this case wikiless.tiekoetter.com) for increased privacy. It is recommended to use these links when possible. See <https://codeberg.org/orenom/wikiless> <sup>[[Archive.org]](https://web.archive.org/web/https://codeberg.org/orenom/wikiless)</sup> for more information.

- **Medium** links have **[Scribe.rip]** link next to them for accessing content through a Scribe.rip Instance for increased privacy. Again, it is recommended to use these links when possible. See <https://scribe.rip/> <sup>[[Archive.org]](https://web.archive.org/web/https://scribe.rip/)</sup> for more information.

You could also install the [LibRedirect](https://libredirect.github.io/) extension on your browser to ease the redirects. <sup>[[Archive.org]](https://web.archive.org/web/20220509220021/https://libredirect.github.io/)</sup>:

- Firefox: <https://addons.mozilla.org/en-US/firefox/addon/libredirect/>

- Chromium-based browsers (Chrome, Brave, Edge): <https://github.com/libredirect/libredirect/blob/master/chromium.md>

**If you are having trouble accessing any of the many academic articles referenced in this guide due to paywalls, feel free to use Sci-Hub (<https://en.wikipedia.org/wiki/Sci-Hub>** <sup>[[Wikiless]](https://wikiless.tiekoetter.com/wiki/Sci-Hub)</sup> <sup>[[Archive.org]](https://web.archive.org/web/https://en.wikipedia.org/wiki/Sci-Hub)</sup>**) or LibGen (<https://en.wikipedia.org/wiki/Library_Genesis>** <sup>[[Wikiless]](https://wikiless.tiekoetter.com/wiki/Library_Genesis)</sup> <sup>[[Archive.org]](https://web.archive.org/web/https://en.wikipedia.org/wiki/Library_Genesis)</sup>**) for finding and reading them. Because Science should be free. All of it. If you are faced with a paywall accessing some resources, consider using <https://12ft.io/>.**

Finally note that this guide does mention and even recommends various commercial services (such as VPNs, CDNs[^43], e-mail providers, hosting providers...) **but is not endorsed or sponsored by any of them in any way. There are no referral links and no commercial ties with any of these providers. This project is 100% non-profit and only relying on donations.**

</div>

## Requirements & Limitations { #requirements-limitations }

- Understanding of the English language (in this case American English).

- Be a permanent resident in Germany where the courts have upheld the legality of not using real names on online platforms (§13 VI of the German Telemedia Act of 2007[^1]'[^2]). **Alternatively, be a resident of any other country where you can confirm and verify the legality of this guide yourself.**

- This guide will assume you already have access to some (Windows/Linux/macOS) laptop computer - ideally not a work/shared device - and a basic understanding of how computers work.

- Have patience, as this process could take several weeks to complete if you want to go through all the content.

- Have some free time on your hands to dedicate to this process (depending on which route you pick).

- Be prepared to read a lot of references (do read them), guides (do not skip them), and tutorials thoroughly (do not skip them either).

- Don't be evil (for real this time)[^3].

- Understand that there is no common path that will be both quick and easy.

This guide is not intended for:

- Creating bot accounts of any kind.

- Creating impersonation accounts of existing people (such as identity theft).

- Helping malicious actors conduct unethical, criminal, or illicit activities (such as trolling, stalking, disinformation, misinformation, harassment, bullying, or fraud).

- Use by minors.

## Introduction { #introduction }

**TLDR for the whole guide: "A strange game. The only winning move is not to play"** [^4]**.**

Making a social media account with a pseudonym or artist/brand name is easy. And it is enough in most use cases to protect your identity as the next George Orwell. There are plenty of people using pseudonyms all over Facebook/Instagram/Twitter/LinkedIn/TikTok/Snapchat/Reddit/... But the vast majority of those are anything but anonymous and can easily be traced to their real identity by your local police officers, random people within the OSINT[^5] community, and trolls[^6] on 4chan[^7].

This is a good thing as most criminals/trolls are not tech-savvy and will usually be identified with ease. But this is also a terrible thing as most political dissidents, human rights activists and whistleblowers can also be tracked rather easily.

This guide aims to provide an introduction to various de-anonymization techniques, tracking techniques, ID verification techniques, and optional guidance to creating and maintaining **reasonably and truly** online anonymous identities including social media accounts safely. This includes mainstream platforms and not only the privacy-friendly ones.

It is important to understand that the purpose of this guide is anonymity and not just privacy but much of the guidance you will find here will also help you improve your privacy and security even if you are not interested in anonymity. There is an important overlap in techniques and tools used for privacy, security, and anonymity but they differ at some point:

- **Privacy is about people knowing who you are but not knowing what you are doing.**

- **Anonymity is about people knowing what you are doing but not knowing who you are** [^8]**.**

![image01](../media/image01.png)

(Illustration from[^9])

Will this guide help you protect yourself from the NSA, the FSB, Mark Zuckerberg, or the Mossad if they are out to find you? Probably not ... Mossad will be doing "Mossad things" [^10] and will probably find you no matter how hard you try to hide[^11].

You must consider your threat model[^12] before going further.

![image02](../media/image02.png)

(Illustration by Randall Munroe, xkcd.com, licensed under CC BY-NC 2.5)

Will this guide help you protect your privacy from OSINT researchers like Bellingcat[^13], Doxing[^14] trolls on 4chan[^15], and others that have no access to the NSA toolbox? More likely. Tho we would not be so sure about 4chan.

Here is a basic simplified threat model for this guide:

![image40](../media/image40.png)

(Note that the "magical amulets/submarine/fake your own death" jokes are quoted from the excellent article "This World of Ours" by James Mickens, 2014.[^10])

Отказ от ответственности: Шутки в сторону (магический амулет...). Конечно, существуют и продвинутые способы смягчения атак на таких продвинутых и опытных противников, но они выходят за рамки данного руководства. Крайне важно, чтобы вы понимали ограничения модели угроз, описанной в этом руководстве. И поэтому это руководство не будет увеличиваться вдвое, чтобы помочь с этими расширенными мерами по смягчению последствий, поскольку это слишком сложно и потребует чрезвычайно высокого уровня знаний и навыков, чего не ожидается от целевой аудитории этого руководства.

The EFF provides a few security scenarios of what you should consider depending on your activity. While some of those tips might not be within the scope of this guide (more about Privacy than Anonymity), they are still worth reading as examples. See <https://ssd.eff.org/en/module-categories/security-scenarios> <sup>[[Archive.org]](https://web.archive.org/web/https://ssd.eff.org/en/module-categories/security-scenarios)</sup>.

If you want to go deeper into threat modeling, see [Threat modeling resources](#threat-modeling-resources).

You might think this guide has no legitimate use but there are many[^16]'[^17]'[^18]'[^19]'[^20]'[^21]'[^22] such as:

- Evading Online Censorship[^23]
- Evading Online Oppression
- Уклонение от онлайн-преследований, доксинга и преследований
- Уклонение от незаконного государственного надзора в Интернете
- Anonymous Online Whistle Blowing
- Anonymous Online Activism
- Анонимная онлайн-журналистика
- Anonymous Online Legal Practice
- Anonymous Online Academic Activities (e.g., accessing country-blocked scientific research)

Это руководство написано с надеждой на тех **людей с добрыми намерениями**, которые, возможно, недостаточно осведомлены, чтобы рассмотреть общую картину.

**Lastly, use it at your own risk. Anything in here is not legal advice and you should verify compliance with your local law before use (IANAL**[^24]**). "Trust but verify"**[^25] **all the information yourself (or even better, "Never Trust, always verify"**[^391]**). We strongly encourage you to inform yourself and do not hesitate to check any information in this guide with outside sources in case of doubt. Please do report any mistake you spot to us as we welcome criticism. Even harsh but sound criticism is welcome and will result in having the necessary corrections made as quickly as possible.**

**А вот неисчерпывающий список некоторых из множества способов, которыми вас можно отследить и деанонимизировать:**

## Your Network { #network }

### Your IP address { #ip-addresses }

**Disclaimer: this whole paragraph is about your public-facing Internet IP and not your local network IP.**

Your IP address[^26] is the most known and obvious way you can be tracked. That IP is the IP you are using at the source. This is where you connect to the internet. That IP is usually provided by your ISP (xDSL, Mobile, Cable, Fiber, Cafe, Bar, Friend, Neighbor). Most countries have data retention regulations[^27] that mandate keeping logs of who is using what IP at a certain time/date for up to several years or indefinitely. Your ISP can tell a third party that you were using a specific IP at a specific date and time, years after the fact. If that IP (the original one) leaks at any point for any reason, it can be used to track down you directly. In many countries, you will not be able to have internet access without providing some form of identification to the provider (address, ID, real name, e-mail ...).

Needless to say, that most platforms (such as social networks) will also keep (sometimes indefinitely) the IP addresses you used to sign-up and sign into their services.

Вот несколько онлайн-ресурсов, которые вы можете использовать, чтобы найти информацию о вашем текущем **публичном IP-адресе** прямо сейчас:

- Find your IP:

    - <https://resolve.rs/>

    - <https://www.dnsleaktest.com/> (Bonus, check your IP for DNS leaks)

- Find your IP location or the location of any IP:

    - <https://resolve.rs/ip/geolocation.html>

- Узнайте, является ли IP-адрес «подозрительным» (в черных списках) или загружал ли он «вещи» на каких-то общедоступных ресурсах:

- <https://mxtoolbox.com/blacklists.aspx>

    - <https://www.virustotal.com/gui/home/search>

- <https://iknowwhatyoudownload.com> (Относитесь к этому с долей скепсиса, он может не показать ничего интересного и имеет ограниченные источники данных. Это больше для развлечения, чем для чего-то серьезного.)

- Регистрационная информация об IP-адресе (скорее всего, о вашем интернет-провайдере или интернет-провайдере вашего подключения, который, скорее всего, знает, кто использует этот IP-адрес в любое время):

    - <https://whois.domaintools.com/>

- Check for open-services or open devices on an IP (especially if there are leaky Smart Devices on it):

- <https://www.shodan.io/host/185.220.101.134> (замените IP на свой IP или любой другой, либо измените в поле поиска, в этом примере IP является выходным узлом Tor)

- Various tools to check your IP such as block-lists checkers and more:

- <https://browserleaks.com/ip>

    - <https://www.whatismyip.com>

- Хотите знать, подключаетесь ли вы через Tor?

- <https://check.torproject.org>

По этим причинам вам придется запутать и скрыть исходный IP-адрес (тот, который привязан к вашей идентификации) или скрыть его с помощью комбинации различных средств:

- Использование общедоступного сервиса Wi-Fi (бесплатно).

- Использование анонимной сети Tor[^28] (бесплатно).

- Анонимное использование услуг VPN[^29] (анонимно с оплатой наличными или Monero).

Обратите внимание, что, к сожалению, эти решения не идеальны, и у вас возникнут проблемы с производительностью[^30].

Все это будет объяснено позже в этом руководстве.

### Ваши запросы DNS и IP { #dns-requests }

DNS[^31] is the internet's address book: every time your browser opens a connection to `www.google.com`, it first asks a DNS server to translate that name into an IP address. Your browser, and most other apps on your device, do this constantly in the background.

Визуальное представление о том, как работает DNS, см. в разделе <https://www.youtube.com/watch?v=vrxwXXytEuI> <sup>[[Invidious]](https://yewtu.be/watch?v=vrxwXXytEuI)</sup>.

#### The default DNS problem { #dns-default-problem }

По умолчанию ваши DNS-запросы направляются на преобразователь вашего интернет-провайдера. Это создает несколько проблем с компаундированием:

- **Ведение журнала.** Интернет-провайдеры часто подчиняются законам о хранении данных и могут регистрировать каждый разрешенный вами домен, создавая полную запись вашей истории посещений. Этот журнал можно вызвать в суд, продать или взломать.
- **Цензура.** Блокировка DNS является наиболее распространенным механизмом цензуры во всем мире[^32][^33] - Интернет-провайдеры просто возвращают ложный адрес для заблокированных доменов.
- **Вмешательство.** Даже если вы настроите частный преобразователь DNS, ваш интернет-провайдер может перехватывать и перезаписывать ответы DNS при передаче, поскольку стандартный трафик DNS не зашифрован.
- **Жестко заданные преобразователи.** Многие устройства полностью обходят системные настройки DNS. Примерно 70% телевизоров Smart TV и 46% игровых консолей[^34] используют жестко закодированные DNS-серверы, которые нельзя изменить в настройках ОС — их необходимо заблокировать на сетевом уровне[^35] или принять раскрытие.

#### Зашифрованный DNS (DoH/DoT) { #dns-encrypted }

Шифрование ваших DNS-запросов с помощью DoH (DNS через HTTPS)[^36] или DoT (DNS через TLS)[^37] не позволяет вашему интернет-провайдеру прочитать или изменить их при передаче. Вы можете запустить это:

- **Локально**, с помощью собственного преобразователя, такого как Pi-hole[^38].
- **Удаленно** через поставщика услуг, обеспечивающего конфиденциальность, например nextdns.io.
- **Автоматически** через DNS вашего VPN-провайдера или через сеть Tor.

Это значительное улучшение по сравнению с открытым текстовым DNS, но одного этого недостаточно.

> **Примечание.** Это руководство не поддерживает и не рекомендует услуги Cloudflare. Cloudflare упоминается здесь только в техническом контексте.

#### Утечка SNI и ECH { #dns-sni-ech }

Даже при использовании зашифрованного DNS само подтверждение TLS передает имя целевого домена через индикацию имени сервера (SNI)[^39]. Наблюдатель, наблюдающий за вашим соединением — ваш интернет-провайдер, сетевой монитор или мошенническая точка доступа — может увидеть, к какому домену вы подключаетесь, из поля SNI, даже если сам DNS-запрос был зашифрован.

![](../media/image04.png)

Зашифрованное приветствие клиента (ECH)[^40] (ранее eSNI[^41]) является исправлением: оно шифрует поле SNI, поэтому целевой домен скрыт от сетевых наблюдателей[^42]. Однако ECH имеет существенные ограничения при развертывании[^44]:

- Только браузеры на базе Firefox поддерживают ECH. По умолчанию он не включен и его необходимо включать вручную.
- ECH only works with sites hosted behind Cloudflare's CDN. It is not supported by most major platforms, including Amazon (AWS, Twitch), Microsoft (Azure, OneDrive, Office 365), Google (Gmail, Google Cloud), Apple (iCloud, iMessage), Reddit, YouTube, Facebook, Instagram, Twitter, and GitHub.
- Сообщается, что Россия[^45] и Китай[^46] блокируют рукопожатия ECH на сетевом уровне, предотвращая подключения к любой службе, для работы которой требуется ECH.

#### OCSP leakage { #dns-ocsp }

A separate leak occurs during TLS certificate validation. Firefox-based browsers use OCSP[^47] to check whether a site's certificate has been revoked. This check sends the certificate's serial number to a third-party OCSP responder - and that serial number can be matched against public certificate databases to identify exactly which site you are visiting[^48].

Сшивание OCSP[^49] смягчает эту проблему, поскольку сервер включает предварительно подписанный ответ OCSP в подтверждение TLS, устраняя необходимость в браузере делать отдельный запрос. Firefox поддерживает сшивание OCSP, но не применяет его, и не все серверы его реализуют. Браузеры на базе Chromium вместо этого используют CRLSets[^50][^51], что, возможно, является более чистым подходом.

Сравнение браузеров: <https://www.ssl.com/blogs/how-do-browsers-handle-revoked-ssl-tls-certificates/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.ssl.com/blogs/how-do-browsers-handle-revoked-ssl-tls-certificates/)</sup>

![](../media/image05.png)

#### Traffic analysis defeats all of the above { #dns-traffic-analysis }

Even with encrypted DNS, ECH, and OCSP stapling all in place, traffic analysis[^52] can still identify the sites you visit by matching IP addresses - since most websites have unique IPs - or by fingerprinting traffic patterns. DNS over Tor shows the strongest DNS privacy in current research, but it can still be defeated by other methods (see [Traffic Anonymization](#traffic-anonymization)).

Для DNS существуют две дополнительные опции, выходящие за рамки стандартного DoH/DoT:

- **Tor Hidden DNS / ODoH** (забывчивый DNS через HTTPS[^53]): отделяет запрос от запрашивающей стороны, поэтому ни одна сторона не знает, кто запрашивает и что они запрашивают. В настоящее время предлагается только Cloudflare[^54], который вводит собственный компромисс между доверием. ODoH не защищает от глобального пассивного злоумышленника (GPA), который может наблюдать за трафиком между клиентским преобразователем и рекурсивным преобразователем, между рекурсивным преобразователем и преобразователем ODNS или между преобразователем ODNS и полномочным сервером.
- **DoHoT** (DNS через HTTPS через Tor): маршрутизация зашифрованных DNS-запросов через Tor для большей анонимности. Требуется Linux и дополнительная техническая настройка. См. <https://github.com/alecmuffett/dohot> <sup>[[Archive.org]](https://web.archive.org/web/https://github.com/alecmuffett/dohot)</sup>.

![](../media/image06.png)

#### Выбор браузера { #dns-browser-choice }

Для повседневного неконфиденциального использования: только браузеры на базе Firefox поддерживают ECH, а ECH помогает только для сайтов, размещенных на Cloudflare. Если вы предпочитаете браузер на базе Chromium, Brave — вариант, наиболее сохраняющий конфиденциальность: он поддерживает все расширения Chrome, добавляя при этом значимую защиту, которой нет в Chrome.

#### IP-адреса остаются остаточной утечкой { #dns-ip-residual }

Независимо от шифрования DNS, IP-адрес, к которому подключается ваше устройство, виден сетевым наблюдателям. Поскольку большинство веб-сайтов имеют уникальные общеизвестные IP-адреса[^89], злоумышленник может сопоставить места назначения вашего подключения с базой данных известных IP-адресов сайтов и сделать вывод, какие сайты вы посещаете, даже не затрагивая ваш DNS-трафик. Сшивание OCSP, ECH и зашифрованный DNS не предотвращают этого.

Вот почему руководство в конечном итоге рекомендует Tor в сочетании с виртуализированной многоуровневой архитектурой (см. [Виртуализация](#virtualization)) как единственное реалистичное средство смягчения последствий: VPN через Tor скрывает как DNS-запросы, так и IP-адреса. Альтернативные конфигурации (Tor через VPN, только VPN, без Tor/VPN) рассматриваются ниже, но менее рекомендуются для использования с высокой чувствительностью.

### Ваши устройства с поддержкой RFID { #rfid-devices }

RFID означает радиочастотную идентификацию[^55], это технология, используемая, например, для бесконтактных платежей и различных систем идентификации. Конечно, ваш смартфон входит в число этих устройств и имеет возможность бесконтактной оплаты RFID через NFC[^56]. Как и все остальное, такие возможности могут использоваться для отслеживания различными субъектами.

But unfortunately, this is not limited to your smartphone, and you also probably carry some amount of RFID enabled device with you all the time such as:

- Your contactless-enabled credit/debit cards
- Your store loyalty cards
- Your transportation payment cards
- Your work-related access cards
- Your car keys
- Your national ID or driver license
- Your passport
- The price/anti-theft tags on object/clothing

While all these cannot be used to de-anonymize you from a remote online adversary, they can be used to narrow down a search if your approximate location at a certain time is known. For instance, you cannot rule out that some stores will effectively scan (and log) all RFID chips passing through the door. They might be looking for their loyalty cards but are also logging others along the way. Such RFID tags could be traced to your identity and allow for de-anonymization.

More information over at Wikipedia: <https://en.wikipedia.org/wiki/Radio-frequency_identification#Security_concerns> <sup>[[Wikiless]](https://wikiless.tiekoetter.com/wiki/Radio-frequency_identification)</sup> <sup>[[Archive.org]](https://web.archive.org/web/https://web.archive.org/web/20220530073225/https://en.wikipedia.org/wiki/Radio-frequency_identification)</sup> and <https://en.wikipedia.org/wiki/Radio-frequency_identification#Privacy> <sup>[[Wikiless]](https://wikiless.tiekoetter.com/wiki/Radio-frequency_identification)</sup> <sup>[[Archive.org]](https://web.archive.org/web/https://web.archive.org/web/20220530073225/https://en.wikipedia.org/wiki/Radio-frequency_identification)</sup>

The only way to mitigate this problem is to have no RFID tags on you or to shield them again using a type of Faraday cage. You could also use specialized wallets/pouches that specifically block RFID communications. Many of those are now made by well-known brands such as Samsonite[^57]. You should just not carry such RFID devices while conducting sensitive activities.

See [Warning about smartphones and smart devices](#smartphones-warning)

### The Wi-Fi and Bluetooth devices around you { #wifi-bluetooth-tracking }

Geolocation is not only done by using mobile antennas triangulation. It is also done using the Wi-Fi and Bluetooth devices around you. Operating systems makers like Google (Android[^58]) and Apple (IOS[^59]) maintain a convenient database of most Wi-Fi access points, Bluetooth devices, and their location. When your Android smartphone or iPhone is on (and not in Plane mode), it will scan actively (unless you specifically disable this feature in the settings) Wi-Fi access points, and Bluetooth devices around you and will be able to geolocate you with more precision than when using a GPS.

This active and continuous probing can then be sent back to Google/Apple/Microsoft as part of their Telemetry. The issue is that this probing is unique and can be used to uniquely identify a user and track such user. Shops, for example, can use this technique to fingerprint customers including when they return, where they go in the shop and how long they stay at a particular place. There are several papers[^60]'[^61] and articles[^62] describing this issue in depth.

This allows them to provide accurate locations even when GPS is off, but it also allows them to keep a convenient record of all Wi-Fi Bluetooth devices all over the world. Which can then be accessed by them or third parties for tracking.

Note: If you have an Android smartphone, Google probably knows where it is no matter what you do. You cannot really trust the settings. The whole operating system is built by a company that wants your data. Remember that if it is free then you are the product.

But that is not what all those Wi-Fi access points can do. Recently developed techs could even allow someone to track your movements accurately just based on radio interferences. What this means is that it is possible to track your movement inside a room/building based on the radio signals passing through. This might seem like a tinfoil hat conspiracy theory claim but here are the references[^63] with demonstrations showing this tech in action: <http://rfpose.csail.mit.edu/> <sup>[[Archive.org]](https://web.archive.org/web/http://rfpose.csail.mit.edu/)</sup> and the video here: <https://www.youtube.com/watch?v=HgDdaMy8KNE> <sup>[[Invidious]](https://yewtu.be/watch?v=HgDdaMy8KNE)</sup>

Other researchers have found a way to count the people in a defined space using only Wi-Fi, see <https://www.news.ucsb.edu/2021/020392/dont-fidget-wifi-will-count-you> <sup>[[Archive.org]](https://web.archive.org/web/https://www.news.ucsb.edu/2021/020392/dont-fidget-wifi-will-count-you)</sup>

You could therefore imagine many use cases for such technologies like recording who enters specific buildings/offices (hotels, hospitals, or embassies for instance) and then discover who meets who and thereby tracking them from outside. Even if they have no smartphone on them.

![](../media/image07.png)

Again, such an issue could only be mitigated by being in a room/building that would act as a Faraday cage.

Here is another video of the same kind of tech in action: <https://www.youtube.com/watch?v=FDZ39h-kCS8> <sup>[[Invidious]](https://yewtu.be/watch?v=FDZ39h-kCS8)</sup>

See: [Warning about smartphones and smart devices](#smartphones-warning).

There is not much you can do about these. Besides being non-identifiable in the first place.

### Rogue Wi-Fi Access Points { #rogue-wifi }

These have been used at least since 2008 using an attack called "Jasager"[^64] and can be done by anyone using self-built tools or using commercially available devices such as Wi-Fi Pineapple[^65].

Here are some videos explaining more about the topic:

- HOPE 2020, <https://archive.org/details/hopeconf2020/20200725_1800_Advanced_Wi-Fi_Hacking_With_%245_Microcontrollers.mp4>

- YouTube, Hak5, Wi-Fi Pineapple Mark VII <https://www.youtube.com/watch?v=7v3JR4Wlw4Q> <sup>[[Invidious]](https://yewtu.be/watch?v=7v3JR4Wlw4Q)</sup>

These devices can fit in a small bag and can take over the Wi-Fi environment of any place within their range. For instance, a Bar/Restaurant/Café/Hotel Lobby. These devices can force Wi-Fi clients to disconnect from their current Wi-Fi (using de-authentication, disassociation attacks[^66]) while spoofing the normal Wi-Fi networks at the same location. They will continue to perform this attack until your computer, or you decide to try to connect to the rogue AP.

These devices can then mimic a captive portal[^67] with the exact same layout as the Wi-Fi you are trying to access (for instance an Airport Wi-Fi registration portal). Or they could just give you unrestricted access internet that they will themselves get from the same place.

Once you are connected through the Rogue AP, this AP will be able to execute various man-in-the-middle attacks to perform analysis on your traffic. These could be malicious redirections or simple traffic sniffing. These can then easily identify any client that would for instance try to connect to a VPN server or the Tor Network.

This can be useful when you know someone you want to de-anonymize is in a crowded place, but you do not know who. This would allow such an adversary to possibly fingerprint any website you visit despite the use of HTTPS, DoT, DoH, ODoH, VPN, or Tor using traffic analysis as pointed above in the DNS section.

These techniques can also be employed to design sophisticated phishing websites aimed at capturing your credentials or persuading you to install a malicious certificate. Such a certificate could enable attackers to intercept and decrypt your encrypted traffic.

How to mitigate those? If you do connect to a public wi-fi access point, use Tor, or use a VPN and then Tor or even VPN over Tor to obfuscate your traffic from the rogue AP while still using it.

In addition, you should see the BlackHat USA conference talk, [Surveilling the Masses with Wi-Fi Positioning Systems](https://www.youtube.com/watch?v=hlbjUvkoyBA) <sup>[[Invidious]](https://yewtu.be/watch?v=hlbjUvkoyBA)</sup>. The talk details a critical vulnerability in the Wi-Fi positioning API by Apple, which can be used to geofence the population using unique identifiers. See: [Warning about smartphones and smart devices](#smartphones-warning). Your neighbors' iPhones are a unique threat, too.

### Traffic Anonymization { #traffic-anonymization }

Tor and VPNs are not silver bullets. Many advanced techniques have been developed and studied to de-anonymize encrypted Tor traffic over the years[^68]. Most of those techniques are Correlation attacks that will correlate your network traffic in one way or another to logs or datasets. Here are some examples:

- **Correlation Fingerprinting Attack:** As illustrated (simplified) below, this attack will fingerprint your encrypted Tor traffic (like the websites you visited) based on the analysis of your encrypted traffic without decrypting it. Some of those methods can do so with a 96% success rate **in a closed-world setting**. **The efficacy of those methods in a real open-world setting** **has not been demonstrated yet and would probably require tremendous resources computing power making it very unlikely that such techniques would be used by a local adversary in the near future.** Such techniques could however hypothetically be used by an advanced and probably global adversary with access to your source network to determine some of your activity. Examples of those attacks are described in several research papers[^69]'[^70]'[^71] as well as their limitations[^72]. The Tor Project itself published an article about these attacks with some mitigations: <https://blog.torproject.org/new-low-cost-traffic-analysis-attacks-mitigations> <sup>[[Archive.org]](https://web.archive.org/web/https://blog.torproject.org/new-low-cost-traffic-analysis-attacks-mitigations)</sup>.

![](../media/image08.png)

- **Correlation Timing Attacks:** As illustrated (simplified) below, an adversary that has access to network connection logs (IP or DNS for instance, remember that most VPN servers and most Tor nodes are known and publicly listed) at the source and the destination could correlate the timings to de-anonymize you without requiring any access to the Tor or VPN network in between. A real use case of this technique was done by the FBI in 2013 to de-anonymize[^73] a bomb threat hoax at Harvard University.

![](../media/image09.png)

- **Correlation Counting Attacks:** As illustrated (simplified) below, an adversary that has no access to detailed connection logs (cannot see that you used Tor or Netflix) but has access to data counting logs could see that you have downloaded 600MB on a specific time/date that matches the 600MB upload at the destination. This correlation can then be used to de-anonymize you over time.

![](../media/image10.png)

There are ways to mitigate these such as:

- Do not use Tor/VPNs to access services that are on the same network (ISP) as the destination service. For example, do not connect to Tor from your University Network to access a University Service anonymously. Instead, use a different source point (such as a public Wi-Fi) that cannot be correlated easily by an adversary.

- Do not use Tor/VPN from an obviously heavily monitored network (such as a corporate/governmental network) but instead try to find an unmonitored network such as a public Wi-Fi or a residential Wi-Fi.

- Consider the use of multiple layers (such as what will be recommended in this guide later: VPN over Tor) so that an adversary might be able to see that someone connected to the service through Tor but will not be able to see that it was you because you were connected to a VPN and not the Tor Network.

Be aware again that this might not be enough against a motivated global adversary[^74] with wide access to global mass surveillance. Such an adversary might have access to logs no matter where you are and could use those to de-anonymize you. Usually, these attacks are part of what is called a Sybil Attack[^75]. **These adversaries are out of the scope of this guide.**

Be also aware that all the other methods described in this guide such as Behavioral analysis can also be used to deanonymize Tor users indirectly (also see [Your Digital Footprint](#digital-footprint).

I also strongly recommend reading this very good, complete, and thorough (and more detailed) guide on most known Attack Vectors on Tor: <https://github.com/Attacks-on-Tor/Attacks-on-Tor> <sup>[[Archive.org]](https://web.archive.org/web/https://github.com/Attacks-on-Tor/Attacks-on-Tor)</sup> as well as this recent research publication <https://www.researchgate.net/publication/323627387_Shedding_Light_on_the_Dark_Corners_of_the_Internet_A_Survey_of_Tor_Research> <sup>[[Archive.org]](https://web.archive.org/web/https://www.researchgate.net/publication/323627387_Shedding_Light_on_the_Dark_Corners_of_the_Internet_A_Survey_of_Tor_Research)</sup>

As well as this great series of blog posts: <https://www.hackerfactor.com/blog/index.php?/archives/906-Tor-0day-The-Management-Vulnerability.html> <sup>[[Archive.org]](https://web.archive.org/web/https://www.hackerfactor.com/blog/index.php?/archives/906-Tor-0day-The-Management-Vulnerability.html)</sup>

Recently, one of these attacks was attempted on the Tor Network with more information here: <https://arstechnica.com/information-technology/2014/07/active-attack-on-tor-network-tried-to-decloak-users-for-five-months/> <sup>[[Archive.org]](https://web.archive.org/web/https://arstechnica.com/information-technology/2014/07/active-attack-on-tor-network-tried-to-decloak-users-for-five-months/)</sup>

Lastly, do remember that using Tor can already be considered suspicious activity[^76], and its use could be considered malicious by some[^77].

This guide will later propose some mitigations to such attacks by changing your origin from the start (using public wi-fi's for instance). Remember that such attacks are usually carried by highly skilled, highly resourceful, and motivated adversaries and are out of scope from this guide. It is also recommended that you learn about practical correlation attacks, as performed by intelligence agencies: <https://officercia.mirror.xyz/WeAilwJ9V4GIVUkYa7WwBwV2II9dYwpdPTp3fNsPFjo> <sup>[[Archive.org]](https://web.archive.org/web/20220516000616/https://officercia.mirror.xyz/WeAilwJ9V4GIVUkYa7WwBwV2II9dYwpdPTp3fNsPFjo)</sup>

**Disclaimer: it should also be noted that Tor is not designed to protect against a global adversary.**[^550]

### Traffic analysis and the limits of Tor { #traffic-analysis-tor }

**Note: This section expands on the [Traffic Anonymization](#traffic-anonymization) above. What follows is a more detailed treatment of the specific attack classes that matter in practice.**

Tor[^28] provides strong anonymity against most adversaries most of the time. It is not, however, unconditional. Understanding what that means in practice, and who realistically is such an adversary, is more useful than either dismissing the concern or being paralyzed by it.

#### Timing correlation attacks { #timing-correlation }

The foundational attack against anonymity networks is traffic correlation: if an adversary can observe the traffic entering the Tor network from your computer and the traffic exiting toward a destination, they can correlate the two streams by timing, volume, and packet patterns - without ever breaking Tor's encryption.

Murdoch and Danezis demonstrated in 2005[^551] that a relatively low-resource adversary controlling even a small number of Tor nodes could use timing analysis to identify which node a hidden service was using, dramatically narrowing the anonymity set. This was an early result and the Tor network has evolved significantly since, but the underlying principle - that correlation across observation points does not require decrypting anything - has only been confirmed by subsequent research.

**RAPTOR**[^552] (2015) showed that Autonomous System (AS) level adversaries - large ISPs and internet exchanges, not just intelligence agencies - could perform traffic analysis by observing BGP routing and inferring path overlap between a Tor user and their destination. The key insight is that the same AS may carry both the user's traffic to the guard node and the exit node's traffic to the destination, making correlation possible without any Tor node compromise.

**DeepCorr** (2018) used deep learning to correlate Tor flows with significantly higher accuracy than prior methods, achieving correlation rates above 96% in controlled conditions. The authors are careful to note that their evaluation was performed in a closed-world lab setting - a fixed set of websites, controlled conditions - and that real-world performance against a large open network with diverse traffic would be substantially harder. This distinction matters: closed-world accuracy figures are frequently misquoted as if they apply to real-world deployments. They do not, at least not yet.

#### Who is a global passive adversary in practice? { #global-passive-adversary }

A true global passive adversary - one who can observe arbitrary internet traffic worldwide simultaneously - does not exist in the form often imagined. What does exist is a collection of national intelligence agencies with broad but not unlimited visibility into internet traffic (GCHQ's TEMPORA, NSA's PRISM and upstream collection programmes), large ISPs and internet exchanges that carry a disproportionate share of global traffic, and cloud providers whose infrastructure spans most of the world's AS paths.

For the vast majority of Tor users, none of these entities are targeting them specifically. For a journalist communicating with a source inside a country whose intelligence services have close partnerships with major Western agencies, or an activist whose traffic transits only a small number of AS paths, the picture is more concerning. The honest answer is: **if a Five Eyes agency is specifically targeting you, Tor alone is probably not sufficient. For everyone else, Tor provides strong protection.**

#### Website fingerprinting { #website-fingerprinting }

Website fingerprinting attacks attempt to identify which website a Tor user is visiting by analysing the pattern of encrypted traffic - packet sizes, timing, direction sequences - without decrypting it. Accuracy in closed-world evaluations (where the attacker knows the user is visiting one of N monitored sites) has reached high levels in research settings. In open-world conditions, where the user may be visiting any of millions of sites, false positive rates make these attacks far less practical. WTF-PAD and related padding defences, partially deployed in Tor Browser, further degrade fingerprinting accuracy. This is an active research area and the situation will evolve.

#### Guard node persistence and what it means { #guard-node-persistence }

Tor uses **guard nodes** - a small, stable set of entry nodes that your client reuses over weeks - specifically to limit timing correlation exposure. If you used a random entry node for every circuit, an adversary who controls even a modest fraction of Tor nodes would eventually observe you entering the network directly. By persisting a small guard set, Tor limits the probability that any given adversary controls your entry point. The tradeoff is that if your guard node is malicious or observed, it remains so for the duration of the guard period. On balance, the Tor Project's research shows guard persistence improves anonymity for most people most of the time.

#### When Tor is and is not sufficient { #tor-sufficiency }

Tor is sufficient against: local network observers (your ISP, your university, a café Wi-Fi), most law enforcement agencies without intelligence partnerships, commercial data brokers, and advertisers.

Tor is not sufficient against: a targeted operation by a well-resourced national intelligence agency with upstream internet visibility, an adversary who controls both your guard node and the destination's exit node simultaneously, or an adversary who can correlate your Tor usage timing with known real-world events (you were the only person in a particular location at a particular time).

The most practical mitigation beyond Tor itself is changing your entry point: connecting to Tor from public Wi-Fi rather than your home connection removes the most reliable correlation anchor - your ISP-assigned IP - from the equation entirely. This guide recommends this approach for high-sensitivity activities throughout.

### Some Devices can be tracked even when offline { #offline-tracking }

You have seen this in action/spy/Sci-Fi movies and shows, the protagonists always remove the battery of their phones to make sure it cannot be used. Most people would think that's overkill. Well, unfortunately, no, this is now becoming true at least for some devices:

- iPhones and iPads (IOS 13 and above)[^78]'[^79]

- Samsung Phones (Android 10 and above)[^80]

- MacBooks (macOS 10.15 and above)[^81]

Such devices will continue to broadcast identity information to nearby devices even when offline using Bluetooth Low-Energy[^82]. They do not have access to the devices directly (which are not connected to the internet) but instead use BLE to find them through other nearby devices[^83]. They are using peer-to-peer short-range Bluetooth communication to broadcast their status through nearby online devices.

They could now find such devices and keep the location in some database that could then be used by third parties or themselves for various purposes (including analytics, advertising, or evidence/intelligence gathering).

See [Warning about smartphones and smart devices](#smartphones-warning)

TLDR: Do not take such devices with you when conducting sensitive activities.

## Your Hardware Identifiers { #hardware-identifiers }

### Windows USB bus telemetry (device enumeration history) { #usb-bus-telemetry }

Windows keeps a permanent enumeration history of every USB device ever connected, independent of whether the device is currently attached.

!!! danger "Deanonymization vector"
    Each USB mass storage device exposes a Vendor ID, Product ID, and, for most drives, a unique serial number at the descriptor level during enumeration. Windows records this under:

    - `HKLM\SYSTEM\CurrentControlSet\Enum\USBSTOR`
    - `HKLM\SYSTEM\CurrentControlSet\Enum\USB`
    - `SetupAPI.dev.log`

    This creates a durable, cross-reinstall link between a specific physical USB drive, phone, hardware key, or dongle, and every OS install it has ever touched, because the identifying data lives in the device's own firmware/descriptor, not in the OS.

How it's exploited:

- Physical device correlation. The same USB drive used across a "clean" VM and a personal machine carries its VID/PID/serial into both installs' registries, creating a link forensic analysis, or malware with sufficient privilege, can recover even if the OS itself was reinstalled or the VM rebuilt.
- First-connected timestamps. Registry key metadata records first- and last-connected times per device, which can corroborate or contradict claimed usage timelines.
- Persists across OS reinstall of the host, not the device. Reinstalling Windows resets the host's own identifiers, including the GDID, but does nothing to the USB device's own serial. Replugging it into a new install just writes a fresh, correlatable entry referencing the same hardware ID.

Mitigations:

- Never share USB storage media, security keys, or peripherals between anonymous and identified environments.
- Where sharing is unavoidable, prefer devices that don't expose a unique serial in their descriptor, and treat any device that has ever touched an identified machine as burned for anonymous use.
- Use write-blockers or a live OS (Tails) for cases where a USB device's provenance itself is sensitive, since USB enumeration history is written by the host OS regardless of read/write intent.

### Your IMEI and IMSI { #imei-imsi }

The IMEI and the IMSI are unique numbers created by cell phone manufacturers and cell phone operators.

The IMEI is tied directly to the phone you are using. This number is known and tracked by the cell phone operators and known by the manufacturers. Every time your phone connects to the mobile network, it will register the IMEI on the network along with the IMSI (if a SIM card is inserted but that is not even needed). It is also used by many applications (Banking apps abusing the phone permission on Android for instance[^86]) and smartphone Operating Systems (Android/IOS) for identification of the device[^87]. It is possible but difficult (and not illegal in many jurisdictions[^88]) to change the IMEI on a phone but it is probably easier and cheaper to just find and buy some old (working) Burner phone for a few Euros (this guide is for Germany remember) at a flea market or some random small shop.

The IMSI is tied directly to the mobile subscription or pre-paid plan you are using and is tied to your phone number by your mobile provider. The IMSI is hardcoded directly on the SIM card and cannot be changed. Remember that every time your phone connects to the mobile network, it will also register the IMSI on the network along with the IMEI. Like the IMEI, the IMSI is also being used by some applications and smartphone Operating systems for identification and is being tracked. Some countries in the EU for instance maintain a database of IMEI/IMSI associations for easy querying by Law Enforcement.

Today, giving away your (real) phone number is the same or better than giving away your Social Security number/Passport ID/National ID.

The IMEI and IMSI can be traced back to you in at least six ways:

- The mobile operator subscriber logs will usually store the IMEI along with the IMSI and their subscriber information database. If you use a prepaid anonymous SIM (anonymous IMSI but with a known IMEI), they could see this cell belongs to you if you used that cell phone before with a different SIM card (different anonymous IMSI but same known IMEI).

- The mobile operator antenna logs will conveniently keep a log of which IMEI. IMSI also keep some connection data. They know and log for instance that a phone with this IMEI/IMSI combination connected to a set of mobile antennas and how powerful the signal to each of those antennas were, allowing easy triangulation/geolocation of the signal. They also know which other phones (your real one for instance) connected at the same time to the same antennas with the same signal. This makes it possible to know precisely that this "burner phone" was always connected at the same place/time than this other "known phone" which shows up every time the burner phone is being used. This information can/is used by various third parties to geolocate/track you quite precisely[^89]'[^90].

- The manufacturer of the Phone can trace back the sale of the phone using the IMEI if that phone was bought in a non-anonymous way. Indeed, they will have logs of each phone sale (including serial number and IMEI), to which shop/person to whom it was sold. And if you are using a phone that you bought online (or from someone that knows you). It can be traced to you using that information. Even if they do not find you on CCTV[^91] and you bought the phone using cash, they can still find what other phone (your real one in your pocket) was there (in that shop) at that time/date by using the antenna logs.

- The IMSI alone can be used to find you as well because most countries now require customers to provide an ID when buying a SIM card (subscription or pre-paid). The IMSI is then tied to the identity of the buyer of the card. In the countries where the SIM can still be bought with cash (like the UK), they still know where (which shop) it was bought and when. This information can then be used to retrieve information from the shop itself (such as CCTV footage as for the IMEI case). Or again the antenna logs can also be used to figure out which other phone was there at the moment of the sale.

- The smartphone OS makers (Google/Apple for Android/IOs) also keep logs of IMEI/IMSI identifications tied to Google/Apple accounts and which user has been using them. They too can trace back the history of the phone and to which accounts it was tied in the past[^92].

- Government agencies around the world interested in your phone number can and do use[^93] special devices called "IMSI catchers"[^94] like the Stingray[^95] or more recently the Nyxcell[^96]. These devices can impersonate (to spoof) a cell phone Antenna and force a specific IMSI to connect to it to access the cell network. Once they do, they will be able to use various MITM[^97] that will allow them to:

    - Tap your phone (voice calls and SMS).

    - Sniff and examine your data traffic.

    - Impersonate your phone number without controlling your phone.

Here is also a good YouTube video on this topic: [DEFCON Safe Mode - Cooper Quintin - Detecting Fake 4G Base Stations in Real-Time](https://www.youtube.com/watch?v=siCk4pGGcqA) <sup>[[Invidious]](https://yewtu.be/watch?v=siCk4pGGcqA)</sup>

 **For these reasons, it is crucial to get a dedicated anonymous phone number and/or an anonymous burner phone with a cash-bought pre-paid sim card that is not tied to you in any way (past or present) for conducting sensitive activities. It is also possible to get an anonymous pre-paid but preferably dedicated number from free and paid online services accepting anonymous cryptocurrencies like Monero. Get more practical guidance here: [Getting an anonymous Phone number](#anonymous-phone).**

While there are some smartphones manufacturers like Purism with their Librem series[^98] who claim to have your privacy in mind, they still do not allow IMEI randomization which we believe is a key anti-tracking feature that should be provided by such manufacturers. While this measure will not prevent IMSI tracking within the SIM card, it would at least allow you to keep the same "burner phone" and only switch SIM cards instead of having to switch both for privacy.

See [Warning about smartphones and smart devices](#smartphones-warning)

### Your Wi-Fi or Ethernet MAC address { #mac-address }

The MAC address[^99] is a unique identifier tied to your physical Network Interface (Wired Ethernet or Wi-Fi) and could of course be used to track you if it is not randomized. As it was the case with the IMEI, manufacturers of computers and network cards usually keep logs of their sales (usually including things like serial number, IMEI, Mac Addresses, ...) and it is possible again for them to track where and when the computer with the MAC address in question was sold and to whom. Even if you bought it with cash in a supermarket, the supermarket might still have CCTV (or a CCTV just outside that shop) and again the time/date of sale could be used to find out who was there using the Mobile Provider antenna logs at that time (IMEI/IMSI).

Operating Systems makers (Google/Microsoft/Apple) will also keep logs of devices and their MAC addresses in their logs for device identification (Find my device type services for example). Apple can tell that the MacBook with this specific MAC address was tied to a specific Apple Account before. Maybe yours before you decided to use the MacBook for sensitive activities. Maybe to a different user who sold it to you but remembers your e-mail/number from when the sale happened.

Your home router/Wi-Fi access point keeps logs of devices that are registered on the Wi-Fi, and these can be accessed too to find out who has been using your Wi-Fi. Sometimes this can be done remotely (and silently) by the ISP depending on if that router/Wi-Fi access point is being "managed" remotely by the ISP (which is often the case when they provide the router to their customers).

Some commercial devices will keep a record of MAC addresses roaming around for various purposes such as road congestion[^100].

**So, it is important again not to bring your phone along when/where you conduct sensitive activities. If you use your own laptop, then it is crucial to hide that MAC address (and Bluetooth address) anywhere you use it and be extra careful not to leak any information. Thankfully many recent OSes now feature or allow the possibility to randomize MAC addresses (Android, IOS, Linux, and Windows 10/11)** with the notable exception of macOS which does not support this feature even in its latest Big Sur version.

See [Warning about smartphones and smart devices](#smartphones-warning)

### Your Bluetooth MAC address { #bluetooth-mac }

Your Bluetooth MAC is like the earlier MAC address except it is for Bluetooth. Again, it can be used to track you as manufacturers and operating system makers keep logs of such information. It could be tied to a sale place/time/date or accounts and then could be used to track you with such information, the shop billing information, the CCTV, or the mobile antenna logs in correlation.

Operating systems have protections in place to randomize those addresses but are still subject to vulnerabilities[^101].

For this reason, and unless you really need those, you should just disable Bluetooth completely in the BIOS/UEFI settings if possible or in the Operating System otherwise.

On Windows 10, you will need to disable and enable the Bluetooth device in the device manager itself to force randomization of the address for next use and prevent tracking.

In general, this should not be too much of a concern compared to MAC Addresses. BT Addresses are randomized quite often.

See [Warning about smartphones and smart devices](#smartphones-warning)

## Your CPU { #cpu }

All modern CPUs[^102] are now integrating hidden management platforms such as the now infamous Intel Management Engine (IME)[^103] and the AMD Platform Security Processor (PSP)[^104].

Those management platforms are small operating systems running directly on your CPU as long as they have power. These systems have full access to your computer's network and could be accessed by an adversary to de-anonymize you in various ways (using direct access or using malware for instance) as shown in this enlightening video: BlackHat, How to Hack a Turned-Off Computer, or Running Unsigned Code in IME <https://www.youtube.com/watch?v=9fhNokIgBMU> <sup>[[Invidious]](https://yewtu.be/watch?v=mYsTBPqbya8)</sup>.

These have already been affected by several security vulnerabilities in the past[^105] that allowed malware to gain control of target systems. These are also accused by many privacy actors including the EFF and Libreboot of being a backdoor into any system[^106].

There are some not so straightforward ways[^107] to disable the IME on some CPUs and you should do so if you can. For some AMD laptops, you can disable it within the BIOS settings by disabling PSP.

Note that, to AMD's defense, there were no security vulnerabilities found for ASP and no backdoors either. See <https://www.youtube.com/watch?v=bKH5nGLgi08&t=2834s> <sup>[[Invidious]](https://yewtu.be/watch?v=bKH5nGLgi08&t=2834s)</sup>. In addition, AMD PSP does not provide any remote management capabilities contrary to IME.

If you are feeling a bit more adventurous, you could install your own BIOS using Coreboot[^108] or Libreboot (a distribution of Coreboot) if your laptop supports it. Coreboot allows you to add your own microcode or other firmware blobs in order for the machine to function, but this is based upon user choice, and as of Dec 2022, Libreboot has adopted a similar pragmatic approach in order to support newer devices in the Coreboot tree. (Thanks, kind Anon who corrected previous information in this paragraph.)

Check yourself:

- If you are using Linux you can check the vulnerability status of your CPU to Spectre/Meltdown attacks by using <https://github.com/speed47/spectre-meltdown-checker> <sup>[[Archive.org]](https://web.archive.org/web/https://github.com/speed47/spectre-meltdown-checker)</sup> which is available as a package for most Linux distros including Whonix. Spectre is a transient execution attack. There is also PoC code for Spectre v1 and v2 on iPhone devices here: <https://github.com/cispa/BranchDifferent> <sup>[[Archive.org]](https://web.archive.org/web/20220814122148/https://github.com/cispa/BranchDifferent)</sup> and here <https://misc0110.net/files/applespectre_dimva22.pdf> <sup>[[Archive.org]](https://web.archive.org/web/20220814122652/https://misc0110.net/files/applespectre_dimva22.pdf)</sup>

- If you are using Windows, you can check the vulnerability status of your CPU using inSpectre <https://www.grc.com/inspectre.htm> <sup>[[Archive.org]](https://web.archive.org/web/https://www.grc.com/inspectre.htm)</sup>

Some CPUs have unfixable flaws (especially Intel CPUs) that could be exploited by various malware. Here is a good current list of such vulnerabilities affecting recent widespread CPUs: <https://en.wikipedia.org/wiki/Transient_execution_CPU_vulnerability> <sup>[[Wikiless]](https://wikiless.tiekoetter.com/wiki/Transient_execution_CPU_vulnerability)</sup> <sup>[[Archive.org]](https://web.archive.org/web/https://en.wikipedia.org/wiki/Transient_execution_CPU_vulnerability)</sup>

Some of these can be avoided using Virtualization Software settings that can mitigate such exploits. See this guide for more information [Spectre/Meltdown Hardening](https://www.whonix.org/wiki/Spectre_Meltdown) <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Spectre_Meltdown)</sup> (warning: these can severely impact the performance of your VMs).

This guide won't go too deep into side-channel and microarchitecture attacks but we will highlight some issues with both Intel and AMD CPU architectures that will be mitigated throughout. It's important to recognize hardware is just as susceptible to bugs, and therefore exploitation, regardless of manufacturer.

We will mitigate some of these issues in this guide by recommending the use of virtual machines on a dedicated anonymous laptop for your sensitive activities that will only be used from an anonymous public network.

**In addition, we recommend the use of AMD CPUs instead of Intel CPUs. See [Types of CPU attacks](#cpu-attacks) for more information.**

- CPU vulnerabilities found in the past few years:

    - [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability))
    - [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability))
    - [Æpic](https://aepicleak.com/)
    - [SGAxe](https://en.wikipedia.org/wiki/Software_Guard_Extensions#SGAxe)
    - [LVI](https://en.wikipedia.org/wiki/Software_Guard_Extensions#LVI)
    - [Plundervolt](https://en.wikipedia.org/wiki/Software_Guard_Extensions#Plundervolt)
    - [MicroScope replay attack](https://en.wikipedia.org/wiki/Software_Guard_Extensions#MicroScope_replay_attack)
    - [Enclave](https://en.wikipedia.org/wiki/Software_Guard_Extensions#Enclave_attack)
    - [Prime+Probe](https://en.wikipedia.org/wiki/Software_Guard_Extensions#Prime+Probe_attack)
    - [Crosstalk](https://www.vusec.net/projects/crosstalk/)
    - [Hertzbleed](https://en.wikipedia.org/wiki/Hertzbleed)
    - [Squip attack](https://www.securityweek.com/amd-processors-expose-sensitive-data-new-squip-attack/)
    - [Zenbleed](https://lock.cmpxchg8b.com/zenbleed.html)

## Your OS and App telemetry services { #os-telemetry }

Whether it is Android, iOS, Windows, macOS, or even Ubuntu. Most popular Operating Systems now collect telemetry information by default even if you never opt-in or opted-out[^112] from the start. Some like Windows will not even allow disabling telemetry completely without some technical tweaks. This information collection can be extensive and include a staggering number of details (metadata and data) on your devices and their usage.

Here are good overviews of what is being collected by those five popular OSes in their last versions:

**Android/Google:**

- Just have a read at their privacy policy <https://policies.google.com/privacy> <sup>[[Archive.org]](https://web.archive.org/web/https://policies.google.com/privacy)</sup>
- School of Computer Science & Statistics, Trinity College Dublin, Ireland Mobile Handset Privacy: Measuring The Data iOS and Android Send to Apple And Google <https://www.scss.tcd.ie/doug.leith/apple_google.pdf> <sup>[[Archive.org]](https://web.archive.org/web/https://www.scss.tcd.ie/doug.leith/apple_google.pdf)</sup>

**IOS/Apple:**

- More information at <https://www.apple.com/legal/privacy/en-ww/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.apple.com/legal/privacy/en-ww/)</sup> and <https://support.apple.com/en-us/HT202100> <sup>[[Archive.org]](https://web.archive.org/web/https://support.apple.com/en-us/HT202100)</sup>
- School of Computer Science & Statistics, Trinity College Dublin, Ireland Mobile Handset Privacy: Measuring The Data iOS and Android Send to Apple And Google <https://www.scss.tcd.ie/doug.leith/apple_google.pdf> <sup>[[Archive.org]](https://web.archive.org/web/https://www.scss.tcd.ie/doug.leith/apple_google.pdf)</sup>
- Apple does claim[^109] that they anonymize this data using differential privacy[^110] but you will have to trust them on that.

**Windows/Microsoft:**

- Full list of required diagnostic data: <https://docs.microsoft.com/en-us/windows/privacy/required-windows-diagnostic-data-events-and-fields-2004> <sup>[[Archive.org]](https://web.archive.org/web/https://docs.microsoft.com/en-us/windows/privacy/required-windows-diagnostic-data-events-and-fields-2004)</sup>
- Full list of optional diagnostic data: <https://docs.microsoft.com/en-us/windows/privacy/windows-diagnostic-data> <sup>[[Archive.org]](https://web.archive.org/web/https://docs.microsoft.com/en-us/windows/privacy/windows-diagnostic-data)</sup>

**macOS:**

- More details on <https://support.apple.com/guide/mac-help/share-analytics-information-mac-apple-mh27990/mac> <sup>[[Archive.org]](https://web.archive.org/web/https://support.apple.com/guide/mac-help/share-analytics-information-mac-apple-mh27990/mac)</sup>

**Ubuntu:**

- Ubuntu despite being a Linux distribution also collects Telemetry Data nowadays. This data however is quite limited compared to the others. More details on <https://ubuntu.com/desktop/statistics> <sup>[[Archive.org]](https://web.archive.org/web/https://ubuntu.com/desktop/statistics)</sup>

Not only are Operating Systems gathering telemetry services but so are Apps themselves like Browsers, Mail Clients, and Social Networking Apps installed on your system.

It is important to understand that this telemetry data can be tied to your device and help de-anonymizing you and later can be used against you by an adversary that would get access to this data.

This does not mean for example that Apple devices are terrible choices for good Privacy (tho this might be changing[^111]), but they are certainly not the best choices for (relative) Anonymity. They might protect you from third parties knowing what you are doing but not from themselves. In all likelihood, they certainly know who you are.

Далее в этом руководстве мы будем использовать все имеющиеся в нашем распоряжении средства, чтобы отключить и заблокировать как можно больше телеметрии, чтобы смягчить этот вектор атаки в операционных системах, поддерживаемых в этом руководстве. These will include Windows, macOS, and even Linux in some regard.

See [Warning about smartphones and smart devices](#smartphones-warning)

### Windows COM Class Identifiers (CLSID) and GUIDs { #your-com-class-identifiers }

Windows assigns a 128-bit GUID to every registered COM class (CLSID), interface (IID), and application (AppID). These are enumerable from user space via the registry (`HKEY_CLASSES_ROOT\CLSID\{GUID}`), no admin rights required, and in some cases can be probed from web content.

**Deanonymization vector**: The specific set of CLSIDs registered on a machine reflects the exact installed software: codecs, shell extensions, Office components, VPN client integrations, security tools, browser helper objects. This is as unique a fingerprint as font or plugin enumeration, but it persists across browser profiles and sessions since it lives at the OS level, not in browser storage.

How it's exploited:

- Software inventory fingerprinting. Enumerating registered CLSIDs reveals installed applications with far more granularity than a User-Agent string.
- Presence probing. A site can test for specific CLSIDs or associated custom URI protocol handlers to detect named applications: VPN clients, communication apps, forensic or analysis tools.
- VM/sandbox detection. Certain CLSIDs and related registry artifacts are diagnostic of VirtualBox, VMware, or known anonymity-focused environments.
- Cross-context correlation. Reusing one Windows install across anonymous and identified activity links the two, independent of browser-level compartmentalization.

Mitigations:

- Use a dedicated, minimal-install VM per identity or persona. Do not reuse one Windows install across anonymous and identified contexts.
- Prefer Linux-based isolation (Whonix, Tails, Qubes-Whonix) for high-threat-model use. This attack class is COM/Windows-specific and has no direct equivalent there.
- Revert to a clean snapshot between sessions rather than relying on manual cleanup.
- Treat this as the same fingerprinting category as font and plugin enumeration: the fix is compartmentalization, not registry editing.

### Windows Global Device Identifier (GDID) { #your-global-device-identifiers }

The GDID is a persistent, server-assigned 64-bit device identifier tied to a Windows installation. It is almost entirely undocumented by Microsoft: the only public reference is a single line in the Azure Monitor schema for the `UCDOStatus` (Delivery Optimization) table, describing a `GlobalDeviceId` column as "Microsoft global device identifier. This is an identifier used by Microsoft internally." Independent reverse-engineering, confirmed against Windows 11 build 26200, has since mapped the full chain.

!!! note "Sources"
    - _United States v. Peter Stokes_, N.D. Ill. (2026). Federal criminal complaint; primary source for the GDID's real-world use in a law enforcement investigation. Highly encourage all readers of this document to consider that this obscure device telemetry vector was not documented prior to this court case, and is mentioned in passing.
    - ["Windows GDID Fully Reverse Engineered: MSA Device PUID Exposed"](https://www.devdigest.org/articles/windows-gdid-fully-reverse-engineered-msa-device-puid-exposed), Devdigest.
    - ["You can't fully disable Microsoft's GDID Windows 11 tracker, but these settings limit what it captures"](https://www.windowslatest.com/2026/07/10/you-cant-fully-disable-microsofts-gdid-windows-11-tracker-but-these-settings-limit-what-it-captures/), Windows Latest.
    - [gdid-reversal](https://github.com/SmtimesIWndr/gdid-reversal), independent reverse-engineering write-up with ETW and registry evidence.

    !!! warning "On the gdid-reversal source"
        We have not vetted and will not vet this source, so exercise caution. This repository is user-created and its authorship is unverified. Content may be partly or wholly AI-generated. Treat specific technical claims (registry paths, binary symbols, ETW provider details) as unverified until cross-checked against a real Windows install or a more established source. It's included here because it's one of the only detailed technical accounts of an otherwise undocumented mechanism, not as an authoritative reference.

!!! danger "How it works"
    When a device signs in with a Microsoft Account, `wlidsvc` provisions it against `login.live.com` and gets back a Device PUID (Passport Unique ID): a server-assigned value, not derived from any local hardware serial. This is stored in the registry, read by the Connected Devices Platform (`cdp.dll` / `CDPSvc`), registered into Microsoft's Device Directory Service graph, and reported by Delivery Optimization as `UCDOStatus.GlobalDeviceId` whenever the machine participates in peer-to-peer update sharing.

    Read your own GDID without admin rights:
    ```powershell
    (Get-ItemProperty 'HKCU:\SOFTWARE\Microsoft\IdentityCRL\ExtendedProperties').LID
    ```
    This is what the federal complaint used to place a Scattered Spider suspect at specific times and locations across multiple VPN sessions and four countries. Microsoft records matched a specific GDID to the moment an ngrok account was created, regardless of the VPN in use.

Key properties for the threat model:

- VPN/IP-agnostic. The GDID doesn't change with IP address, VPN provider, or exit node. It correlates sessions on the same OS install, not network paths.
- Not disabled by telemetry opt-outs. It doesn't travel through the classic `DiagTrack` pipeline. Disabling standard diagnostic data settings has no effect on it.
- Server-side persistence. Deleting the local registry value is cosmetic. The same identifier re-syncs from Microsoft's servers on the next authenticated request (opening the Microsoft Store, for example), because the canonical copy lives server-side, not on disk.
- Local accounts don't prevent it. A local, non-MSA install still registers an anonymous device path through the Connected Devices Platform. It just isn't tied to an MSA identity unless one is added later.
- A reinstall gets a new GDID, not a clean slate. A fresh install produces a new identifier, but account, OneDrive, and activation records give Microsoft a documented basis for linking the new GDID back to the old one through the same account.

Mitigations:

- Assume any Windows install signed into a Microsoft Account is linkable across all its sessions regardless of VPN discipline. This is a hard requirement for compartmentalization, not a tuning option.
- For genuinely sensitive activity, don't use Windows at all. Use a Linux-based environment (Whonix, Tails, Qubes-Whonix) where this telemetry chain doesn't exist.
- Never reuse a single Windows install, MSA, or even a "cleaned" reinstall on the same physical machine across separate personas.

Reducing exposure, if Windows must be used:

- Use a local account. CDP still creates an anonymous device path, but the GDID won't be tied to an MSA.
- Block `dds.microsoft.com` and `activity.windows.com` via firewall rules or the hosts file, to cut the reporting channel at the network layer.
- Delete the registry keys under `IdentityCRL` to clear the locally stored PUID. This only clears the local cache. It's recreated identical to before on the next MSA sign-in or even a background service touching a Microsoft app, since the canonical value lives server-side.
- Disable the Delivery Optimization service (`DoSvc`). This service reports the GDID via `UCDOStatus.GlobalDeviceId` and is hardened against normal administrative control: `Stop-Service` and `Set-Service` return access-denied even when run elevated. The only reported workaround is disabling it directly in the registry by setting its `Start` value to `4` under its service key, since the Service Manager's block doesn't extend to direct registry writes. Disabling `DoSvc` alongside `CDPSvc`/`CDPUserSvc` breaks Delivery Optimization peer caching, Phone Link / "Continue on PC," and nearby sharing. These are expected tradeoffs, not bugs.

!!! warning "What this does not do"
    None of the above retracts a GDID already reported to Microsoft, and none of it makes the device anonymous. It only stops the local install from continuing to re-register and re-report going forward. The historical link between the device and any prior identified activity already exists on Microsoft's servers and can't be removed by a local user.

!!! note "Further reading / tooling"
    Independent write-ups and a defensive PowerShell toolkit implementing the steps above (read-only audit, preview mode, revert option) are publicly available and worth reviewing directly rather than treating this section as a complete implementation guide. The service-disabling steps carry real breakage tradeoffs and should be tested on a VM snapshot first.

## Your Smart Devices { #smart-devices }

You got it; your smartphone is an advanced spying/tracking device that:

- Records everything you say at any time ("Hey Siri", "Hey Google").

- Records your location everywhere you go.

- Always records other devices around you (Bluetooth devices, Wi-Fi Access points).

- Records your habits and health data (steps, screen time, exposure to diseases, connected devices data)

- Records all your network locations.

- Records all your pictures and videos (and most likely where they were taken).

- Has most likely access to most of your known accounts including social media, messaging, and financial accounts.

Data is being transmitted even if you opt-out[^112], processed, and stored indefinitely (most likely unencrypted[^113]) by various third parties[^114].

But that is not all, this section is not called "Smartphones" but "Smart devices" because it is not only your smartphone spying on you. It is also every other smart device you could have:

- Your Smart Watch? (Apple Watch, Android Smartwatch ...)

- Your Fitness Devices and Apps[^115]'[^116]? (Strava[^117]'[^118], Fitbit[^119], Garmin, Polar[^120], ...)

- Your Smart Speaker? (Amazon Alexa[^121], Google Echo, Apple Homepod ...)

- Your Smart Transportation? (Car? Scooter?)

- Your Smart Tags? (Apple AirTag, Galaxy SmartTag, Tile...)

- Your Car? (Yes, most modern cars have advanced logging/tracking features these days[^122])

- Any other Smart device? There are even convenient search engines dedicated to finding them online:

    - <https://www.shodan.io/>

    - <https://censys.io/>

    - <https://www.zoomeye.org/>

See [Warning about smartphones and smart devices](#smartphones-warning)

Conclusion: Do not bring your smart devices with you when conducting sensitive activities.

## Yourself { #yourself }

### Your Metadata { #metadata }

What's metadata? Every file you create or share carries metadata - structured data embedded in or alongside the content that describes how, when, where, and with what the file was created. This metadata is invisible in normal use and routinely overlooked. It has burned journalistic sources, identified whistleblowers, and linked anonymous documents to their authors. The tools to strip it exist and are not difficult to use. The failure is almost always one of not knowing it was there.

The most frequently cited case is the 2013 identification of a leaker at a US government contractor through metadata in a Word document sent to The Intercept.[^542] The document's print metadata included a serial number traceable to a specific printer, combined with microdot tracking patterns in the printout itself - but the principle applies equally to digital metadata. Earlier, in 2003, a UK government dossier on Iraqi weapons capabilities was found to contain revision history showing the names of the civil servants who had edited it, causing significant political embarrassment[^543] and demonstrating that the problem predates widespread awareness.

Your metadata is all the information about your activities without the actual content of those activities. For instance, it is like knowing you had a call from an oncologist before then calling your family and friends successively. You do not know what was said during the conversation, but you can guess what it was just from the metadata[^123].

This metadata will also often include your location that is being harvested by Smartphones, Operating Systems (Android[^124]/IOS), Browsers, Apps, Websites. Odds are several companies are knowing exactly where you are at any time[^125] because of your smartphone[^126].

This location data has been used in many judicial cases[^127] already as part of "geofencing warrants" [^128] that allow law enforcement to ask companies (such as Google/Apple) a list of all devices present at a certain location at a certain time. In addition, this location data is even sold by private companies to the military who can then use it conveniently[^129]. These warrants are becoming widely used by law enforcement[^130]'[^131]'[^132].

If you want to experience yourself what a "geofencing warrant" would look like, here is an example: <https://wigle.net/>.

Now let us say you are using a VPN to hide your IP. The social media platform knows you were active on that account on November 4th from 8 am to 1 pm with that VPN IP. The VPN allegedly keeps no logs and cannot trace back that VPN IP to your IP. Your ISP however knows (or at least can know) you were connected to that same VPN provider on November 4th from 7:30 am to 2 pm but does not know what you were doing with it.

The question is: Is there someone somewhere that would have both pieces of information available[^133] for correlation in a convenient database?

Have you heard of Edward Snowden[^134]? Now is the time to google him and read his book[^135]. Also read about XKEYSCORE[^136]'[^137], MUSCULAR[^138], SORM[^139], Tempora[^140] , and PRISM[^141].

See "We kill people based on Metadata"[^142] or this famous tweet from the IDF <https://twitter.com/idf/status/1125066395010699264> <sup>[[Archive.org]](https://web.archive.org/web/20210519061345/https://twitter.com/idf/status/1125066395010699264)</sup> <sup>[[Nitter]](https://nitter.net/idf/status/1125066395010699264)</sup>.

See [Smartphones](#smartphones-warning) for a warning on using smartphones and other smart devices. See [Metadata auditing](#metadata-auditing) for a way to get rid of the metadata - which is probably what brought you to this section anyway.

### Your Digital Footprint { #digital-footprint }

This is the part where you should watch the documentary "The Social Dilemma"[^143] on Netflix as they cover this topic much better than anyone else.

This includes is the way you write (stylometry) [^144]'[^145], the way you behave[^146]'[^147]. The way you click. The way you browse. The fonts you use on your browser[^148]. Fingerprinting is being used to guess who someone is by the way that user is behaving. You might be using specific pedantic words or making specific spelling mistakes that could give you away using a simple Google search for similar features because you typed comparably on some Reddit post 5 years ago using a not so anonymous Reddit account[^149]. The words you type in a search engine alone can be used against you as the authorities now have warrants to find people who used specific keywords in search engines[^150].

Social Media platforms such as Facebook/Google can go a step further and can register your behavior in the browser itself. For instance, they can register everything you type even if you do not send it / save it. Think of when you draft an e-mail in Gmail. It is saved automatically as you type. They can register your clicks and cursor movements as well.

All they need to achieve this in most cases is Javascript enabled in your browser (which is the case in most Browsers including Tor Browser by default). Even with Javascript disabled, there are still ways to fingerprint you[^151].

While these methods are usually used for marketing purposes and advertising, they can also be a useful tool for fingerprinting users. This is because your behavior is unique or unique enough that over time, you could be de-anonymized.

Here are some examples:

- Specialized companies are selling to, for example, law enforcement agencies products for analyzing social network activities such as <https://mediasonar.com/> <sup>[[Archive.org]](https://web.archive.org/web/https://mediasonar.com/)</sup>

- For example, as a basis of authentication, a user's typing speed, keystroke depressions, patterns of error (say accidentally hitting an "l" instead of a "k" on three out of every seven transactions) and mouse movements establish that person's unique pattern of behavior[^152]. Some commercial services such as TypingDNA (<https://www.typingdna.com/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.typingdna.com/)</sup>) even offer such analysis as a replacement for two-factor authentications.

- This technology is also widely used in CAPTCHAS[^371] services to verify that you are "human" and can be used to fingerprint a user.

- See [Counteracting Forensic Linguistics](#forensic-linguistics).

Analysis algorithms could then be used to match these patterns with other people and match you to a different known user. It is unclear whether such data is already used or not by Governments and Law Enforcement agencies, but it might be in the future. And while this is mostly used for advertising/marketing/captchas purposes now. It could and probably will be used for investigations in the short or mid-term future to deanonymize users.

Here is a fun example you try yourself to see some of those things in action: <https://clickclickclick.click> (no archive links for this one sorry). You will see it becoming interesting over time (this requires Javascript enabled).

Here is also a recent example just showing what Google Chrome collects on you: <https://web.archive.org/web/https://pbs.twimg.com/../media/EwiUNH0UYAgLY7V?format=jpg&name=4096x4096>

Here are some other resources on the topic if you cannot see this documentary:

- 2017, Behavior Analysis in Social Networks, <https://link.springer.com/10.1007/978-1-4614-7163-9_110198-1> <sup>[[Archive.org]](https://web.archive.org/web/https://link.springer.com/10.1007/978-1-4614-7163-9_110198-1)</sup>

- 2017, Social Networks and Positive and Negative Affect <https://www.sciencedirect.com/science/article/pii/S1877042811013747/pdf?md5=253d8f1bb615d5dee195d353dc077d46&pid=1-s2.0-S1877042811013747-main.pdf> <sup>[[Archive.today]](https://archive.ph/iuowI)</sup>

- 2015, Using Social Networks Data for Behavior and Sentiment Analysis <https://www.researchgate.net/publication/300562034_Using_Social_Networks_Data_for_Behavior_and_Sentiment_Analysis> <sup>[[Archive.org]](https://web.archive.org/web/https://www.researchgate.net/publication/300562034_Using_Social_Networks_Data_for_Behavior_and_Sentiment_Analysis)</sup>

- 2016, A Survey on User Behavior Analysis in Social Networks <https://www.academia.edu/30936118/A_Survey_on_User_Behaviour_Analysis_in_Social_Networks> <sup>[[Archive.org]](https://web.archive.org/web/https://www.academia.edu/30936118/A_Survey_on_User_Behaviour_Analysis_in_Social_Networks)</sup>

- 2017, DEF CON 25 presentation: [DEF CON 25 - Svea Eckert, Andreas Dewes - Dark Data](https://www.youtube.com/watch?v=1nvYGi7-Lxo) <sup>[[Invidious]](https://yewtu.be/watch?v=1nvYGi7-Lxo)</sup>

- 2019, Influence and Behavior Analysis in Social Networks and Social Media <https://sci-hub.se/10.1007/978-3-030-02592-2> <sup>[[Archive.org]](https://web.archive.org/web/https://web.archive.org/web/https://sci-hub.se/10.1007/978-3-030-02592-2)</sup>

So, how can you mitigate these?

- This guide will provide some technical mitigations using Fingerprinting resistant tools but those might not be sufficient.

- You should apply common sense and try to find your own patterns in your behavior and behave differently when using anonymous identities. This includes:

    - The way you type (speed, accuracy...).

    - The words you use (be careful with your usual expressions).

    - The type of response you use (if you are sarcastic by default, try to have a different approach with your identities).

    - The way you use your mouse and click (try to solve the Captchas differently than your usual way)

    - The habits you have when using some Apps or visiting some Websites (do not always use the same menus/buttons/links to reach your content).

    - ...

You need to act and fully adopt a role as an actor would do for a performance. You need to become a different person, think, and act like that person. This is not a technical mitigation but a human one. You can only rely on yourself for that.

Ultimately, it is mostly up to you to fool those algorithms by adopting new habits and not revealing real information when using your anonymous identities. See [Counteracting Forensic Linguistics](#forensic-linguistics).

### IRL and OSINT { #irl-osint }

These are clues you might give over time that could point to your real identity. You might be talking to someone or posting on some board/forum/Reddit. In those posts, you might over time leak some information about your real life. These might be memories, experiences, or clues you shared that could then allow a motivated adversary to build a profile to narrow their search.

A real use and well-documented case of this was the arrest of the hacker Jeremy Hammond[^153] who shared over time several details about his past and was later discovered.

There are also a few cases involving OSINT at Bellingcat[^154]. Have a look at their very informative (but slightly outdated) toolkit here: <https://docs.google.com/spreadsheets/d/18rtqh8EG2q1xBo2cLNyhIDuK9jrPGwYr9DI2UncoqJQ/edit#gid=930747607> <sup>[[Archive.org]](https://web.archive.org/web/https://docs.google.com/spreadsheets/d/18rtqh8EG2q1xBo2cLNyhIDuK9jrPGwYr9DI2UncoqJQ/edit)</sup>

**We have an OSINT discussion room in our Matrix community. Feel free to join at ```#OSINT:matrix.org```.**

You can also view some convenient lists of some available OSINT tools here if you want to try them on yourself for example:

- <https://github.com/jivoi/awesome-osint> <sup>[[Archive.org]](https://web.archive.org/web/https://github.com/jivoi/awesome-osint)</sup>

- <https://web.archive.org/web/20210426041234/https://jakecreps.com/tag/osint-tools/>

- <https://osintframework.com/>

- <https://recontool.org>

As well as this interesting Playlist on YouTube: <https://www.youtube.com/playlist?list=PLrFPX1Vfqk3ehZKSFeb9pVIHqxqrNW8Sy> <sup>[[Invidious]](https://yewtu.be/playlist?list=PLrFPX1Vfqk3ehZKSFeb9pVIHqxqrNW8Sy)</sup>

As well as those interesting podcasts:

<https://www.inteltechniques.com/podcast.html>

You should never share real individual experiences/details using your anonymous identities that could later lead to finding your real identity. You will see more details about this in the [Creating new identities](#creating-new-identities) section.

### Your Face, Voice, Biometrics, and Pictures { #biometrics }

"Hell is other people", even if you evade every method listed above, you are not out of the woods yet thanks to the widespread use of advanced Face recognition by everyone.

Companies like Facebook have used advanced face recognition for years[^155]'[^156] and have been using other means (GEOINT) to create maps of "people" around the world[^157]. This evolution has been going on for years to the point we can now say "we lost control of our faces"[^158].

If you are walking in a touristy place, you will most likely appear in someone's selfie within minutes without knowing it. That person could then go ahead and upload that selfie to various platforms (Twitter, Google Photos, Instagram, Facebook, Snapchat ...). Those platforms will then apply face recognition algorithms to those pictures under the pretext of allowing better/easier tagging or to better organize your photo library. In addition to this, the same picture will provide a precise timestamp and in most cases geolocation of where it was taken. Even if the person does not provide a timestamp and geolocation, it can still be guessed with other means[^159]'[^160].

Here are a few resources for even trying this yourself:

- Bellingcat, Guide To Using Reverse Image Search For Investigations: <https://www.bellingcat.com/resources/how-tos/2019/12/26/guide-to-using-reverse-image-search-for-investigations/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.bellingcat.com/resources/how-tos/2019/12/26/guide-to-using-reverse-image-search-for-investigations/)</sup>

- Bellingcat, Using the New Russian Facial Recognition Site SearchFace <https://www.bellingcat.com/resources/how-tos/2019/02/19/using-the-new-russian-facial-recognition-site-searchface-ru/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.bellingcat.com/resources/how-tos/2019/02/19/using-the-new-russian-facial-recognition-site-searchface-ru/)</sup>

- Bellingcat, Dali, Warhol, Boshirov: Determining the Time of an Alleged Photograph from Skripal Suspect Chepiga <https://www.bellingcat.com/resources/how-tos/2018/10/24/dali-warhol-boshirov-determining-time-alleged-photograph-skripal-suspect-chepiga/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.bellingcat.com/resources/how-tos/2018/10/24/dali-warhol-boshirov-determining-time-alleged-photograph-skripal-suspect-chepiga/)</sup>

- Bellingcat, Advanced Guide on Verifying Video Content <https://www.bellingcat.com/resources/how-tos/2017/06/30/advanced-guide-verifying-video-content/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.bellingcat.com/resources/how-tos/2017/06/30/advanced-guide-verifying-video-content/)</sup>

- Bellingcat, Using the Sun and the Shadows for Geolocation <https://www.bellingcat.com/resources/2020/12/03/using-the-sun-and-the-shadows-for-geolocation/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.bellingcat.com/resources/2020/12/03/using-the-sun-and-the-shadows-for-geolocation/)</sup>

- Bellingcat, Navalny Poison Squad Implicated in Murders of Three Russian Activists <https://www.bellingcat.com/news/uk-and-europe/2021/01/27/navalny-poison-squad-implicated-in-murders-of-three-russian-activists/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.bellingcat.com/news/uk-and-europe/2021/01/27/navalny-poison-squad-implicated-in-murders-of-three-russian-activists/)</sup>

- Bellingcat, Berlin Assassination: New Evidence on Suspected FSB Hitman Passed to German Investigators <https://www.bellingcat.com/news/2021/03/19/berlin-assassination-new-evidence-on-suspected-fsb-hitman-passed-to-german-investigators/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.bellingcat.com/news/2021/03/19/berlin-assassination-new-evidence-on-suspected-fsb-hitman-passed-to-german-investigators/)</sup>

- Bellingcat, Digital Research Tutorial: Investigating a Saudi-Led Coalition Bombing of a Yemen Hospital <https://www.youtube.com/watch?v=cAVZaPiVArA> <sup>[[Invidious]](https://yewtu.be/watch?v=cAVZaPiVArA)</sup>

- Bellingcat, Digital Research Tutorial: Using Facial Recognition in Investigations <https://www.youtube.com/watch?v=awY87q2Mr0E> <sup>[[Invidious]](https://yewtu.be/watch?v=awY87q2Mr0E)</sup>

- Bellingcat, Digital Research Tutorial: Geolocating (Allegedly) Corrupt Venezuelan Officials in Europe <https://www.youtube.com/watch?v=bS6gYWM4kzY> <sup>[[Invidious]](https://yewtu.be/watch?v=bS6gYWM4kzY)</sup>

### Gait Recognition and Other Long-Range Biometrics { #gait-recognition }

Even if you are not looking at the camera, they can still figure out who you are[^161], make out your emotions[^162], analyze your gait[^163]'[^164]'[^165], read your lips[^166], analyze the behavior of your eyes[^167], and probably guess your political affiliation[^168]'[^169].

Contrary to popular belief and pop culture, modern gait recognition systems aren't fooled by simply changing how you walk (ex. with something uncomfortable in your shoe), as they analyze the way your body's muscles move across your entire body, as you perform certain actions. The best way to fool modern gait recognition is to wear loose clothes that obscure the way your muscles move as you perform actions.

Other things than can be used to identify you include your earlobes, which are actually more identifiable than fingerprints, or even the shape of your skull. As such, soft headcoverings such as balaclavas are not recommendable for obscuring your identity - they make you look incredibly suspicious, while also conforming to the shape of your skull.

![](../media/image11.png)

(Illustration from <https://www.nature.com/articles/s41598-020-79310-1> <sup>[[Archive.org]](https://web.archive.org/web/https://www.nature.com/articles/s41598-020-79310-1.pdf)</sup>)

![](../media/image12.png)

(иллюстрация из <https://rd.springer.com/chapter/10.1007/978-3-030-42504-3_15> <sup>[[Archive.org]](https://web.archive.org/web/https://rd.springer.com/chapter/10.1007/978-3-030-42504-3_15)</sup>)

Those platforms (Google/Facebook) already know who you are for a few reasons:

- Because you have or had a profile with them, and you identified yourself.

- Even if you never made a profile on those platforms, you still have one without even knowing it[^170]'[^171]'[^172]'[^173]'[^174].

- Потому что другие люди отметили вас или опознали вас на своих фотографиях с праздников/вечеринок.

- Потому что другие люди поместили вашу фотографию в свой список контактов, которой затем поделились с ними.

Здесь также представлена ​​подробная демонстрация Microsoft Azure, которую вы можете попробовать сами на сайте <https://azure.microsoft.com/en-us/services/cognitive-services/face/#demo>, где вы сможете распознавать эмоции и сравнивать лица на разных изображениях.

Правительства уже знают, кто вы, потому что у них есть фотографии вашего удостоверения личности/паспорта/водительских прав и они часто добавляют биометрические данные (отпечатки пальцев) в свою базу данных. Те же самые правительства интегрируют эти технологии (часто предоставляемые частными компаниями, такими как израильская Oosto[^175], Clearview AI[^176]'[^177] или NEC[^178]) в свои сети видеонаблюдения для поиска «лиц, представляющих интерес»[^179]. А некоторые государства, находящиеся под усиленным наблюдением, такие как Китай, широко используют распознавание лиц для различных целей[^180]'[^181], включая, возможно, идентификацию этнических меньшинств[^182]. Простая ошибка распознавания лица каким-либо алгоритмом может разрушить вашу жизнь[^183]'[^184].

Вот некоторые ресурсы, подробно описывающие некоторые методы, используемые правоохранительными органами сегодня:

- Видео CCC, объясняющее текущие возможности наблюдения правоохранительных органов: <https://media.ccc.de/v/rc3-11406-spot_the_surveillance#t=761> <sup>[[Archive.org]](https://web.archive.org/web/https://media.ccc.de/v/rc3-11406-spot_the_surveillance)</sup>

- EFF SLS: <https://www.eff.org/sls> <sup>[[Archive.org]](https://web.archive.org/web/https://www.eff.org/sls)</sup>

Apple делает FaceID массовым явлением и продвигает его использование для входа во многие службы, включая банковские системы.

The same goes with fingerprint authentication being mainstreamed by many smartphone makers to authenticate yourself. A simple picture where your fingers appear can be used to de-anonymize you[^185]'[^186]'[^187]'[^188].

То же самое касается вашего голоса, который можно анализировать для различных целей, как показано в недавнем патенте Spotify[^189].

В некоторых местах для идентификации можно использовать даже радужную оболочку [^190].

Мы можем смело представить себе ближайшее будущее, в котором вы не сможете создавать учетные записи или входить где-либо без предоставления уникальных биометрических данных (подходящее время для повторного просмотра Gattaca[^191], Person of Interest[^192] и Minority Report[^193]). И вы можете смело представить, насколько полезными могут быть эти большие биометрические базы данных для некоторых заинтересованных третьих сторон.

Кроме того, вся эта информация также может быть использована против вас (если вы уже деанонимизированы) с помощью deepfake[^194] путем создания ложной информации (изображений, видео, голосовых записей[^195]...) и уже использовалась в таких целях[^196]'[^197]. Для этого есть даже коммерческие сервисы, такие как <https://www.respeecher.com/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.respeecher.com/)</sup> и <https://www.descript.com/overdub> <sup>[[Archive.org]](https://web.archive.org/web/https://www.descript.com/overdub)</sup>.

Посмотрите эту демонстрацию: <https://www.youtube.com/watch?v=t5yw5cR79VA> <sup>[[Invidious]](https://yewtu.be/watch?v=t5yw5cR79VA)</sup>

В настоящее время есть несколько шагов[^198], которые вы можете использовать, чтобы уменьшить (и только уменьшить) распознавание лиц при выполнении конфиденциальных действий, где может присутствовать система видеонаблюдения:

– Носите маску, поскольку доказано, что она превосходит некоторые технологии распознавания лиц[^199], но не все[^200].

- Наденьте бейсболку или шляпу, чтобы не зафиксировать ваше лицо при опознании с помощью камер видеонаблюдения под большим углом (съемка сверху). Помните, что это не поможет против фронтальных камер.

- Носите солнцезащитные очки в дополнение к маске и бейсболке, чтобы не опознать человека по чертам глаз.

– Подумайте о том, чтобы носить специальные солнцезащитные очки (к сожалению, дорогие) под названием "Reflectacles" <https://www.reflectacles.com/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.reflectacles.com/)</sup>. Было проведено небольшое исследование, показывающее их эффективность против систем распознавания лиц IBM и Amazon[^201].

- Все это может оказаться бесполезным из-за упомянутого ранее распознавания походки, но здесь может быть надежда, если у вас есть 3D-принтер: <https://gitlab.com/FG-01/fg-01> <sup>[[Archive.org]](https://web.archive.org/web/https://gitlab.com/FG-01/fg-01)</sup>

(см. [Распознавание походки и другие биометрические данные дальнего действия])

(Обратите внимание: если вы собираетесь использовать их там, где установлены передовые системы распознавания лиц, эти меры сами по себе могут пометить вас как подозрительных и вызвать проверку человеком)

### Фишинг и социальная инженерия { #phishing }

Фишинг[^202] — это атака социальной инженерии[^203], при которой злоумышленник может попытаться получить от вас информацию, притворяясь или выдавая себя за что-то/кого-то другого.

Типичный случай — злоумышленник использует атаку «человек посередине[^97]» или поддельное электронное письмо/звонок с целью запросить ваши учетные данные для службы. Это может быть, например, посредством электронной почты или путем выдачи себя за финансовые услуги.

Такие атаки также могут использоваться для деанонимизации кого-либо, заставляя его загрузить вредоносное ПО или со временем раскрыть личную информацию. Единственная защита от них — не поддаваться им и здравому смыслу.

Они использовались бесчисленное количество раз с момента появления Интернета, и самый обычный из них называется «мошенничеством 419» (см. <https://en.wikipedia.org/wiki/Advance-fee_scam> <sup>[[Wikiless]](https://wikiless.tiekoetter.com/wiki/Advance-fee_scam)</sup> <sup>[[Archive.org]](https://web.archive.org/web/https://en.wikipedia.org/wiki/Advance-fee_scam)</sup>).

Если вы хотите узнать больше о типах фишинга, вот хороший видеоролик: Black Hat, Ихтиология: фишинг как наука <https://www.youtube.com/watch?v=Z20XNp-luNA> <sup>[[Invidious]](https://yewtu.be/watch?v=Z20XNp-luNA)</sup>.

## Вредоносные программы, эксплойты и вирусы { #malware }

### Вредоносное ПО в ваших файлах/документах/электронной почте { #malware-files }

Используя стеганографию или другие методы, можно легко внедрить вредоносное ПО в распространенные форматы файлов, такие как документы Office, изображения, видео, PDF-документы...

Это могут быть как простые ссылки отслеживания в формате HTML, так и сложные целевые вредоносные программы.

These could be simple pixel-sized images[^204] hidden in your e-mails that would call a remote server to try and get your IP address.

These could be exploiting a vulnerability in an outdated format or an outdated reader[^205]. Such exploits could then be used to compromise your system.

See these good videos for more explanations on the matter:

- What is a File Format? <https://www.youtube.com/watch?v=VVdmmN0su6E> <sup>[[Invidious]](https://yewtu.be/watch?v=VVdmmN0su6E)</sup>

- Ange Albertini: Funky File Formats: <https://www.youtube.com/watch?v=hdCs6bPM4is> <sup>[[Invidious]](https://yewtu.be/watch?v=hdCs6bPM4is)</sup>

Всегда следует проявлять крайнюю осторожность. См. раздел [Виртуализация](#virtualization), чтобы предотвратить утечку любой информации даже в случае открытия такого вредоносного файла.

If you want to learn how to try detecting such malware, see [Checking files for malware](#checking-files-malware)

### Malware and Exploits in your apps and services { #malware-apps }

So, you are using Tor Browser or Brave Browser over Tor. You could be using those over a VPN for added security. But you should keep in mind that there are exploits[^206] (hacks) that could be known by an adversary (but unknown to the App/Browser provider). Such exploits could be used to compromise your system and reveal details to de-anonymize you such as your IP address or other details.

A real use case of this technique was the Freedom Hosting[^207] case in 2013 where the FBI inserted malware[^208] using a Firefox browser exploit on a Tor website. This exploit allowed them to reveal details of some users. More recently, there was the notable SolarWinds[^209] hack that breached several US government institutions by inserting malware into an official software update server.

In some countries, Malware is just mandatory and/or distributed by the state itself. This is the case for instance in China with WeChat[^210] which can then be used in combination with other data for state surveillance[^211].

There are countless examples of malicious browser extensions, smartphone apps, and various apps that have been infiltrated with malware over the years.

Here are some steps to mitigate this type of attack:

- You should never have 100% trust in the apps you are using.
- You should always check that you are using the updated version of such apps before use and ideally validate each download using their signature if available.
- You should not use such apps directly from a hardware system but instead, use a Virtual Machine for compartmentalization.

To reflect these recommendations, this guide will therefore later guide you in the use of Virtualization (See [Virtualization](#virtualization) so that even if your Browser/Apps get compromised by a skilled adversary, that adversary will find himself stuck in a sandbox[^212] without being able to access identifying information or compromise your system.

### Malicious USB devices { #malicious-usb }

There are readily available commercial and cheap "badUSB" [^213]devices that can take deploy malware, log your typing, geolocate you, listen to you or gain control of your laptop just by plugging them in. Here are some examples that you can already buy yourself:

- Hak5, USB Rubber Ducky <https://shop.hak5.org/products/usb-rubber-ducky-deluxe> <sup>[[Archive.org]](https://web.archive.org/web/https://shop.hak5.org/products/usb-rubber-ducky-deluxe)</sup>

- Hak5, O.MG Cable <https://www.youtube.com/watch?v=V5mBJHotZv0> <sup>[[Invidious]](https://yewtu.be/watch?v=V5mBJHotZv0)</sup>

- Keelog <https://www.keelog.com/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.keelog.com/)</sup>

- AliExpress <https://www.aliexpress.com/i/4000710369016.html> <sup>[[Archive.org]](https://web.archive.org/web/https://www.aliexpress.com/i/4000710369016.html)</sup>

Such devices can be implanted anywhere (charging cable, mouse, keyboard, USB key ...) by an adversary and can be used to track you or compromise your computer or smartphone. The most notable example of such attacks is probably Stuxnet[^214] in 2005.

While you could inspect a USB key physically, scan it with various utilities, check the various components to see if they are genuine, you will most likely never be able to discover complex malware embedded in genuine parts of a genuine USB key by a skilled adversary without advanced forensics equipment[^215].

To mitigate this, you should never trust such devices and plug them into sensitive equipment. If you use a charging device, you should consider the use of a USB data blocking device that will only allow charging but not any data transfer. Such data blocking devices are now readily available in many online shops. You should also consider disabling USB ports completely within the BIOS of your computer unless you need them (if you can).

### Malware and backdoors in your Hardware Firmware and Operating System { #firmware-backdoors }

This might sound a bit familiar as this was already partially covered previously in the [Your CPU](#cpu) section.

Malware and backdoors can be embedded directly into your hardware components. Sometimes those backdoors are implemented by the manufacturer itself such as the IME in the case of Intel CPUs. And in other cases, such backdoors can be implemented by a third party that places itself between orders of new hardware and customer delivery[^216].

Such malware and backdoors can also be deployed by an adversary using software exploits. Many of those are called rootkits[^217] within the tech world. Usually, these types of malware are harder to detect and mitigate as they are implemented at a lower level than the userspace[^218] and often in the firmware[^219] of hardware components itself.

What is firmware? Firmware is a low-level operating system for devices. Each component in your computer probably has firmware including for instance your disk drives. The BIOS[^220]/UEFI[^221] system of your machine for instance is a type of firmware.

These can allow remote management and are capable of enabling full control of a target system silently and stealthily.

As mentioned previously, these are harder to detect by users but some limited steps that can be taken to mitigate some of those by protecting your device from tampering and use some measures (like re-flashing the bios for example). Unfortunately, if such malware or backdoor is implemented by the manufacturer itself, it becomes extremely difficult to detect and disable those.

**Note: The threats described in this section are almost exclusively relevant to high-value targets of nation-state adversaries. If your threat model is a stalker, a corporate competitor, or even most law enforcement agencies, you can skip this section. If you are a journalist, dissident, or activist operating against a state-level adversary, read it.**

Most guides to anonymity focus on software and network-layer threats. Physical and hardware-level attacks are rarer, more expensive to execute, and require either physical access to your device or interference with your supply chain. That cost means they are not deployed casually. But for the right target, they are devastatingly effective - because no amount of software configuration protects you if the hardware underneath is compromised.

#### Firmware implants { #firmware-implants }

Firmware implants are malicious code inserted into the low-level software that runs before your operating system boots - in the UEFI/BIOS[^544], storage controller firmware, or network card firmware. Because they live below the OS, they survive reinstallation of the operating system, disk wiping, and most forensic examination.

**LoJax**[^545], discovered by ESET in 2018, was the first publicly documented in-the-wild UEFI rootkit, attributed to the APT28 (Fancy Bear) group. It wrote a malicious module directly into the SPI flash memory of the UEFI firmware, persisting across OS reinstalls and even hard drive replacements. **MosaicRegressor**[^546], documented by Kaspersky in 2020, was similarly implanted into UEFI and discovered on devices belonging to NGO staff and journalists in contact with North Korea.

Who faces this threat? In both documented cases, targets were NGO workers, journalists, and diplomatic personnel - people whose devices passed through the hands of state actors, or who were targeted by sophisticated spear-phishing that enabled remote firmware write access. This is not a threat that scales to mass deployment. It is used surgically, against specific high-value individuals.

Mitigations are limited but worth understanding. **UEFI Secure Boot**[^307] verifies the cryptographic signatures of bootloader and OS components before execution, preventing unsigned code from running at boot. It does not, however, protect against a compromise of the firmware itself - if the UEFI has already been modified, Secure Boot can be disabled or bypassed from within. It is a meaningful defence against attackers who have not yet achieved firmware-level access, but it is not a root of trust in the presence of a firmware implant. **Intel Boot Guard** and AMD's equivalent go further by fusing a hash of the initial firmware into the hardware at manufacture time, making firmware modification detectable. **Heads**[^547] is an open-source firmware alternative for supported hardware (primarily Thinkpads and select System76 machines) that provides measured boot, TPM-backed attestation, and tamper detection - and is the most practical option for a high-risk user who needs verifiable firmware integrity. See also: [About Secure Boot](#secure-boot).

#### USB attack hardware { #usb-attack-hardware }

USB-based attack tools are commercially available and widely understood. The **O.MG Cable** is a USB cable with an embedded wireless implant - visually and functionally indistinguishable from a legitimate charging cable - that can execute keystrokes, exfiltrate data, and accept remote commands over Wi-Fi. The **USB Rubber Ducky** and broader Hak5 product family present themselves to a target computer as a keyboard, executing pre-loaded keystroke injection payloads at speeds no human typist could match. See also: [Malicious USB devices](#malicious-usb).

Recognition is difficult. O.MG cables are designed specifically to defeat visual inspection. Practical mitigations include: **never using cables or USB devices you did not purchase yourself and receive sealed**, using a USB data blocker ("USB condom") when charging from untrusted ports, and configuring your operating system to require confirmation before trusting new USB devices (USBGuard on Linux[^548]; this is not natively available on Windows without third-party tools).

#### Evil Maid attacks { #evil-maid }

For more on Evil Maid attacks, see: [Evil Maid attack](#evil-maid-attack).

Mitigations:

- **Never leave your device unattended in a high-risk environment.** This is the only complete mitigation.
- **Measured boot with TPM attestation** (as provided by Heads or a correctly configured UEFI + TPM setup) will detect bootloader tampering by comparing measurements against known-good values stored in the TPM.
- **A tamper-evident seal** on the device chassis (nail varnish applied across screws and photographed, or commercial tamper-evident stickers) provides a low-tech detection layer that is surprisingly effective against unsophisticated adversaries.

#### Supply chain compromise { #supply-chain }

Supply chain attacks target your device before it reaches you - at the manufacturer, distributor, or shipping stage. The NSA's ANT catalogue[^549], leaked by Snowden in 2013, documented hardware implants installed in Cisco routers and other network equipment in transit. For most users, this threat is not realistic. For a senior dissident, human rights lawyer, or intelligence source in a country whose government has influence over hardware supply chains, it deserves consideration.

Practical mitigations are limited. Purchasing devices in person from a retail store (rather than having them shipped) reduces the interception window. Preferring hardware from vendors outside adversary supply chain reach, and using Heads-supported hardware with verified firmware, provides some assurance. For the highest-risk cases, consider that any device that has left your control - even briefly - should be treated as potentially compromised.

#### Physical inspection checklist { #physical-inspection }

For high-risk individuals receiving or returning to a device:

- Inspect port openings (USB, Thunderbolt, SD card slot) for signs of foreign objects or residue.
- Check screws for scratches inconsistent with factory assembly; apply a tamper-evident seal after inspection.
- Compare the cable you are about to use against a known-good reference; if in doubt, discard it.
- On first boot after any period of unattended access, verify firmware measurements if your platform supports it (Heads TPM event log; `tpm2-tools` on Linux).
- If Secure Boot is unexpectedly disabled in UEFI settings, treat the device as compromised.

## Your files, documents, pictures, and videos { #your-files }

### Properties and Metadata { #file-metadata }

This can be obvious to many but not to all. Most files have metadata attached to them. Good examples are pictures that store EXIF[^222] information which can hold a lot of information such as GPS coordinates, which camera/phone model took it, and when it was taken precisely. While this information might not directly give out who you are, it could tell exactly where you were at a certain moment which could allow others to use various sources to find you (CCTV or other footage taken at the same place at the same time during a protest for instance). You must verify any file you would put on those platforms for any properties that might hold any information that might lead back to you.

Here is an example of EXIF data that could be on a picture:

![](../media/image13.png)

(Illustration from Wikipedia)

This also works for videos. Yes, videos too have geo-tagging, and many are very unaware of this. Here Is for instance a very convenient tool to geo-locate YouTube videos: <https://mattw.io/youtube-geofind/location> <sup>[[Archive.org]](https://web.archive.org/web/https://mattw.io/youtube-geofind/location)</sup>

For this reason, you will always have to be incredibly careful when uploading files using your anonymous identities and check the metadata of those files.

**Even if you publish a plain text file, you should always double or triple-check it for any information leakage before publishing. You will find some guidance about this in the [Some additional measures against forensics](#anti-forensics) section at the end of the guide.**

### Watermarking { #watermarking }

#### Pictures, Video and Audio { #media-watermarking }

Pictures/Videos often contain visible watermarks indicating who is the owner/creator but there are also invisible watermarks in various products aiming at identifying the viewer itself.

So, if you are a whistleblower and thinking about leaking some picture/audio/video file. Think twice. There are chances that those might contain invisible watermarking within them that would include information about you as a viewer. Such watermarks can be enabled with a simple switch in like Zoom (Video[^223] or Audio[^224]) or with extensions[^225] for popular apps such as Adobe Premiere Pro. These can be inserted by various content management systems.

For a recent example where someone leaking a Zoom meeting recording was caught because it was watermarked: <https://theintercept.com/2021/01/18/leak-zoom-meeting/> <sup>[[Tor Mirror]](http://27m3p2uv7igmj6kvd4ql3cct5h3sdwrsajovkkndeufumzyfhlfev4qd.onion/2021/01/18/leak-zoom-meeting/)</sup> <sup>[[Archive.org]](https://web.archive.org/web/https://theintercept.com/2021/01/18/leak-zoom-meeting/)</sup>

Such watermarks can be inserted by various products[^226]'[^227]'[^228]'[^229] using Steganography[^230] and can resist compression[^231] and re-encoding[^232]'[^233].

These watermarks are not easily detectable and could allow identification of the source despite all efforts.

In addition to watermarks, the camera used for filming (and therefore the device used for filming) a video can also be identified using various techniques such as lens identification[^234] which could lead to de-anonymization.

Be extremely careful when publishing videos/pictures/audio files from known commercial platforms as they might contain such invisible watermarks in addition to details in the images themselves. There is no guaranteed 100% protection against those. You will have to use common sense.

#### Printer Watermarking { #printer-watermarking }

Did you know your printer is most likely spying on you too? Even if it is not connected to any network? This is usually a known fact by many people in the IT community but few outside people.

Yes ... Your printers can be used to de-anonymize you as well as explained by the EFF here <https://www.eff.org/issues/printers> <sup>[[Archive.org]](https://web.archive.org/web/https://www.eff.org/issues/printers)</sup>

With this (old but still relevant) video explaining how from the EFF as well: <https://www.youtube.com/watch?v=izMGMsIZK4U> <sup>[[Invidious]](https://yewtu.be/watch?v=izMGMsIZK4U)</sup>

Many printers will print an invisible watermark allowing for identification of the printer on every printed page. This is called Printer Steganography[^235]. There is no tangible way to mitigate this but to inform yourself on your printer and make sure it does not print any invisible watermark. This is important if you intend to print anonymously.

Here is an (old but still relevant) list of printers and brands who do not print such tracking dots provided by the EFF <https://www.eff.org/pages/list-printers-which-do-or-do-not-display-tracking-dots> <sup>[[Archive.org]](https://web.archive.org/web/https://www.eff.org/pages/list-printers-which-do-or-do-not-display-tracking-dots)</sup>

Here are also some tips from the Whonix documentation ([Printing and Scanning](https://www.whonix.org/wiki/Printing_and_Scanning)) <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Printing_and_Scanning)</sup>:

**Do not ever print in Color, usually, watermarks are not present without color toners/cartridges**[^236]**.**

### Pixelized or Blurred Information { #pixelized-info }

Did you ever see a document with blurred text? Did you ever make fun of those movies/series where they "enhance" an image to recover seemingly impossible-to-read information?

Well, there are techniques for recovering information from such documents, videos, and pictures.

Here is for example an open-source project you could use yourself for recovering text from some blurred images yourself: <https://github.com/beurtschipper/Depix> <sup>[[Archive.org]](https://web.archive.org/web/https://github.com/beurtschipper/Depix)</sup>

![image14](../media/image14.png)

This is of course an open-source project available for all to use. But you can imagine that such techniques have probably been used before by other adversaries. These could be used to reveal blurred information from published documents that could then be used to de-anonymize you.

There are also tutorials for using such techniques using Photo Editing tools such as GIMP such as <https://medium.com/@somdevsangwan/unblurring-images-for-osint-and-more-part-1-5ee36db6a70b>   <sup>[[Archive.org]](https://web.archive.org/web/https://medium.com/@somdevsangwan/unblurring-images-for-osint-and-more-part-1-5ee36db6a70b)</sup> followed by <https://medium.com/@somdevsangwan/deblurring-images-for-osint-part-2-ba564af8eb5d> <sup>[[Scribe.rip]](https://scribe.rip/@somdevsangwan/deblurring-images-for-osint-part-2-ba564af8eb5d)</sup> <sup>[[Archive.org]](https://web.archive.org/web/https://medium.com/@somdevsangwan/deblurring-images-for-osint-part-2-ba564af8eb5d)</sup>

![image15](../media/image15.png)

Finally, you will find plenty of deblurring resources here: <https://github.com/subeeshvasu/Awesome-Deblurring> <sup>[[Archive.org]](https://web.archive.org/web/https://github.com/subeeshvasu/Awesome-Deblurring)</sup>

Some online services could even help you do this automatically to some extent like MyHeritage.com enhance tool:

<https://www.myheritage.com/photo-enhancer> <sup>[[Archive.org]](https://web.archive.org/web/https://www.myheritage.com/photo-enhancer)</sup>

Here is the result of the above image:

![image16](../media/image16.png)

Of course, this tool is more like "guessing" than really deblurring at this point, but it could be enough to find you using various reverse image searching services.

There are also techniques to deblur/depixelate parts in videos: see <https://positive.security/blog/video-depixelation> <sup>[[Archive.org]](https://web.archive.org/web/https://positive.security/blog/video-depixelation)</sup>

For this reason, it is always extremely important that you correctly redact and curate any document you might want to publish. Blurring is not enough, and you should always completely blacken/remove any sensitive data to avoid any attempt at recovering data from any adversary. Do not pixelized, do not blur, just put a hard black rectangle to redact information.

## Your Crypto Transactions { #crypto-transactions }

Contrary to widespread belief, Crypto transactions (such as Bitcoin and Ethereum) are not anonymous[^237]. Most cryptocurrencies can be tracked accurately through various methods[^238]'[^239].

Remember what they say on their page: <https://bitcoin.org/en/you-need-to-know> <sup>[[Archive.org]](https://web.archive.org/web/https://bitcoin.org/en/you-need-to-know)</sup> and <https://bitcoin.org/en/protect-your-privacy> <sup>[[Archive.org]](https://web.archive.org/web/https://bitcoin.org/en/protect-your-privacy)</sup>: "Bitcoin is not anonymous"

The main issue is not setting up a random Crypto wallet to receive some currency behind a VPN/Tor address (at this point, the wallet is anonymous). The issue is mainly when you want to convert Fiat money (Euros, Dollars ...) to Crypto and then when you want to cash in your Crypto. You will have few realistic options but to transfer those to an exchange (such as Coinbase/Kraken/Bitstamp/Binance). Those exchanges have known wallet addresses and will keep detailed logs (due to KYC[^240] financial regulations) and can then trace back those crypto transactions to you using the financial system[^241].

There are some cryptocurrencies with privacy/anonymity in mind like Monero but even those have some and warnings to consider[^242]'[^243].

Use of "private" mixers, tumblers[^244] (centralized services that specialize in "anonymizing" cryptocurrencies by "mixing them") and coinjoiners are risky as you don't know what's happening on them[^245] and can be trivially de-mixed[^246]. Their centrally-controlled nature could also put you in trouble as they are more susceptible to money-laundering laws[^247].

This does not mean you cannot use Bitcoin anonymously at all. You can actually use Bitcoin anonymously as long as you do not convert it to actual currency, use a Bitcoin wallet from a safe anonymous network, and do not reuse addresses or consolidate outputs that were used when spending at different merchants. Meaning you should avoid KYC/AML regulations by various exchanges, avoid using the Bitcoin network from any known IP address, and use a wallet that provides privacy-preserving tools. See [Anonymous crypto payments](#anonymous-crypto-payments).

**Overall, the best option for using Crypto with reasonable anonymity and privacy is still Monero and you should ideally not use any other for sensitive transactions unless you are aware of the limitations and risks involved. Please do read** [Monero Disclaimer](#monero-disclaimer)**.**

**TLDR: Use Monero!**

## Your Cloud Backup & Sync Services { #cloud-backups }

All companies are advertising their use of end-to-end encryption (E2EE). This is true for almost every messaging app and website (HTTPS). Apple and Google are advertising their use of encryption on their Android devices and their iPhones.

But what about your backups? Those automated iCloud/Google Drive backups you have?

Well, you should know that most of those backups are not fully end-to-end encrypted and will hold some of your information readily available for a third party. You will see their claims that data is encrypted at rest and safe from anyone ... Except they usually do keep a key to access some of the data themselves. These keys are used for them indexing your content, recover your account, collecting various analytics.

There are specialized commercial forensics solutions available (Magnet Axiom[^248], Cellebrite Cloud[^249]) that will help an adversary analyze your cloud data with ease.

Notable Examples:

- Apple iCloud: <https://support.apple.com/en-us/HT202303> <sup>[[Archive.org]](https://web.archive.org/web/https://support.apple.com/en-us/HT202303)</sup> : "Messages in iCloud also uses end-to-end encryption. If you have iCloud Backup turned on**, your backup includes a copy of the key protecting your Messages**. This ensures you can recover your Messages if you lose access to iCloud Keychain and your trusted devices. ".

- Google Drive and WhatsApp: <https://faq.whatsapp.com/android/chats/about-google-drive-backups/> <sup>[[Archive.org]](https://web.archive.org/web/https://faq.whatsapp.com/android/chats/about-google-drive-backups/)</sup>: "**Media and messages you back up aren't protected by WhatsApp end-to-end encryption while in Google Drive**. ". Do however note that Facebook/Whatsapp have announced the rollout of encrypted backups on October 14^th^ 2021 (<https://about.fb.com/news/2021/10/end-to-end-encrypted-backups-on-whatsapp/> <sup>[[Archive.org]](https://web.archive.org/web/https://about.fb.com/news/2021/10/end-to-end-encrypted-backups-on-whatsapp/)</sup>) which should solve this issue.

- Dropbox: <https://www.dropbox.com/privacy#terms> <sup>[[Archive.org]](https://web.archive.org/web/https://www.dropbox.com/privacy)</sup> "To provide these and other features, **Dropbox accesses, stores, and scans Your Stuff**. You give us permission to do those things, and this permission extends to our affiliates and trusted third parties we work with".

- Microsoft OneDrive: <https://privacy.microsoft.com/en-us/privacystatement> <sup>[[Archive.org]](https://web.archive.org/web/https://privacy.microsoft.com/en-us/privacystatement)</sup>: Productivity and communications products, "When you use OneDrive, we collect data about your usage of the service, as well as the content you store, to provide, improve, and protect the services. **Examples include indexing the contents of your OneDrive documents so that you can search for them later and using location information to enable you to search for photos based on where the photo was taken**".

You should not trust cloud providers with your (not previously and locally encrypted) sensitive data and you should be wary of their privacy claims. In most cases, they can access your data and provide it to a third party if they want to[^250].

The only way to mitigate this is to encrypt your data on your side and then only upload it to such services **or just not use them at all.**

## Microarchitectural Side-channel Deanonymization Attacks { #side-channel-attacks }

There was an attack published that can deanonymize users if they have a known alias. For example, an attacker trying to track the activities of a journalist can use that journalist's public Twitter handle to link their anonymous identities with their public one. This breaks compartmentalization of identities and can lead to complete deanonymization, even of users who practice proper OPSEC.

The attack, published at <https://leakuidatorplusteam.github.io/> <sup>[[Archive.org]](https://web.archive.org/web/20220720023429/https://leakuidatorplusteam.github.io/)</sup>, can be mitigated using the well-known [NoScript](https://noscript.net/) extension and will be our preferred recommendation.

One loosely documented attack might take the following approach to fingerprinting: Alice is browsing the web using Firefox. The website she has just visited is using an invisible `iframe` that creates long strings, e.g., sentences or hashes, to produce some non-user-viewable string. These strings are setting a certain font type, Arial. Whether the browser renders this is non-essential, it only matters if the font changes. The `iframe` in this case serves no purpose but to identify whether a user has installed a certain font on their machine. If Alice is using a font that this frame has tried to render, then it is reported back to the website and to the person in control of the website.

The font renders a box with a specific height and width around itself, so that means a specific height and width of the text contained within. The `iframe` keeps doing this for each installed font to create a list of installed fonts for Alice. Because of stylistic differences between each font family, the same string and the same font size will add up to a different height and a different width than Arial. It is used as a fallback font to display text that won't display otherwise, in the case of a user not having that font on their machine and thus non-viewable from their browser.

If a font requested by an `iframe` is not available, Arial will be used to show that text to the user. Every time the font measurement (identified by the dimensions of the box produced) changed, it means the font is present on Alice's browser and her machine. By doing this for hundreds of fonts, websites can use this information to track users using their installed fonts across websites. Imagine a website then selling this “anonymized” information as a dataset to advertisement companies to serve you ads based on the websites you visit, because they know every font you have installed on your machine and can now track your identity across the internet. This attack is demonstrated here: [Everything you always wanted to know about web-based device fingerprinting (but were afraid to ask)](https://www.youtube.com/watch?v=5Y1Y96jC5AA) by Dr. Nick Nikiforakis, PhD in Computer Science from KU Leuven. He explains how his team of researchers identified which sites were using such techniques on Alexa's top 10,000 websites. Primarily, they found that of those, 145 were fingerprinting browsers. They were fingerprinted 100% of the time - whether they were using the Do Not Track header, a popular Privacy & Security setting in many browsers, did not matter.

Attacks such as invisible iframes and media elements can be avoided by blocking all scripts globally by using something like uBlock Origin <https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm> or by using NoScript <https://chrome.google.com/webstore/detail/noscript/doojmbjmlfjjnbmnoijecmcbfeoakpjm>. This is highly encouraged, not only to those wishing to be anonymous, but also to general web users.

**Tor Browser**

**Note: This attack is now prevented by default by an update of [NoScript](https://noscript.net/) (11.4.8 and above) on all security levels in Tor Browser.**

**All others**

Installing the [NoScript](https://noscript.net/) extension will prevent the attack **by default only in private Windows** using their new "TabGuard feature". But can be enabled in the NoScript options to work on all Windows. See:

- Release tweet: <https://twitter.com/ma1/status/1557751019945299969> <sup>[[Archive.org]](https://web.archive.org/web/https://twitter.com/ma1/status/1557751019945299969)</sup>
- User explanation: <https://noscript.net/usage/#crosstab-identity-leak-protection> <sup>[[Archive.org]](https://web.archive.org/web/https://noscript.net/usage/#crosstab-identity-leak-protection)</sup>
- Tor Project Forum Post: <https://forum.torproject.net/t/tor-browser-can-leak-your-identity-through-side-channel-attack/4005/2> <sup>[[Archive.org]](https://web.archive.org/web/https://forum.torproject.net/t/tor-browser-can-leak-your-identity-through-side-channel-attack/4005/2)</sup>
- NoScript extension for Firefox (Firefox, and other Firefox-based browsers except Tor Browser): <https://addons.mozilla.org/en-US/firefox/addon/noscript/>
- NoScript extension for Chromium based browsers (Brave, Chrome, Edge, and other Chromium-based browsers): <https://chrome.google.com/webstore/detail/noscript/doojmbjmlfjjnbmnoijecmcbfeoakpjm?hl=en>

### Alternative to NoScript for all other browsers { #noscript-alternative }

The researches who disclosed the issue also made an extension available below. Again, **nothing is required in Tor Browser**. This path is not our preferred path but is still available if you do not want to use NoScript.

- Leakuidator+ extension for Chromium based browsers (Brave, Chrome, Edge, and other Chromium-based browsers): <https://chrome.google.com/webstore/detail/leakuidator%2B/hhfpajcjkikoocmmhcimllpinjnbedll>
- Leakuidator+ extension for Firefox (Firefox, and other Firefox-based browsers except Tor Browser): <https://addons.mozilla.org/en-US/firefox/addon/leakuidatorplus/>

Separating identities via separate browsers or even with VMs is not enough to avoid this attack. However, another solution is to make sure that when you start working with an anonymous identity, you entirely close all activities linked to other identities. The vulnerability only works if you're actively logged into a non-anonymous identity. The issue with this is that it can hinder effective workflow, as multitasking across multiple identities becomes impossible.

## Local Data Leaks and Forensics { #local-data-leaks }

Most of you have probably seen enough Crime dramas on Netflix or TV to know what forensics are. These are technicians (usually working for law enforcement) that will perform various analysis of evidence. This of course could include your smartphone or laptop.

While these might be done by an adversary when you already got "burned", these might also be done randomly during a routine control or a border check. These unrelated checks might reveal secret information to adversaries that had no prior knowledge of such activities.

Forensics techniques are now very advanced and can reveal a staggering amount of information from your devices even if they are encrypted[^253]. These techniques are widely used by law enforcement all over the world and should be considered.

Here are some recent resources you should read about your smartphone:

- UpTurn, The Widespread Power of U.S. Law Enforcement to Search Mobile Phones <https://www.upturn.org/reports/2020/mass-extraction/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.upturn.org/reports/2020/mass-extraction/)</sup>

- New-York Times, The Police Can Probably Break Into Your Phone <https://www.nytimes.com/2020/10/21/technology/iphone-encryption-police.html> <sup>[[Archive.org]](https://web.archive.org/web/https://www.nytimes.com/2020/10/21/technology/iphone-encryption-police.html)</sup>

- Vice, Cops Around the Country Can Now Unlock iPhones, Records Show <https://www.vice.com/en/article/vbxxxd/unlock-iphone-ios11-graykey-grayshift-police> <sup>[[Archive.org]](https://web.archive.org/web/https://www.vice.com/en/article/vbxxxd/unlock-iphone-ios11-graykey-grayshift-police)</sup>

I also highly recommend that you read some documents from a forensics examiner perspective such as:

- EnCase Forensic User Guide, <http://encase-docs.opentext.com/documentation/encase/forensic/8.07/Content/Resources/External%20Files/EnCase%20Forensic%20v8.07%20User%20Guide.pdf> <sup>[[Archive.org]](https://web.archive.org/web/http://encase-docs.opentext.com/documentation/encase/forensic/8.07/Content/Resources/External%20Files/EnCase%20Forensic%20v8.07%20User%20Guide.pdf)</sup>

- FTK Forensic Toolkit, <https://accessdata.com/products-services/forensic-toolkit-ftk> <sup>[[Archive.org]](https://web.archive.org/web/https://accessdata.com/products-services/forensic-toolkit-ftk)</sup>

- SANS Digital Forensics and Incident Response Videos, <https://www.youtube.com/c/SANSDigitalForensics/videos>

And finally, here is this very instructive detailed paper on the current state of IOS/Android security from the John Hopkins University: https://securephones.io/main.html__PROTECTED_0__.

When it comes to your laptop, the forensics techniques are many and widespread. Many of those issues can be mitigated by using full disk encryption, virtualization (See [Virtualization](#virtualization)), and compartmentalization. This guide will later detail such threats and techniques to mitigate them.

## Bad Cryptography { #on-bad-cryptography }

There is a frequent adage among the infosec community: "Don't roll your own crypto!".

And there are reasons[^255]'[^256]'[^257]'[^258] for that:

We would not want people discouraged from studying and innovating in the crypto field because of that adage. So instead, we would recommend people to be cautious with "Roll your own crypto" because it is not necessarily good crypto:

- Good cryptography is not easy and usually takes years of research to develop and fine-tune.

- Good cryptography is transparent and not proprietary/closed source so it can be reviewed by peers.

- Good cryptography is developed carefully, slowly, and rarely alone.

- Good cryptography is usually presented and discussed in conferences and published in various journals.

- Good cryptography is extensively peer-reviewed before it is released for use in the wild.

- Using and implementing existing good cryptography correctly is already a challenge.

Yet, this is not stopping some from doing it anyway and publishing various production Apps/Services using their self-made cryptography or proprietary closed-source methods:

– Следует проявлять осторожность при использовании приложений/служб, использующих методы шифрования с закрытым исходным кодом или собственные методы. Все хорошие криптостандарты общедоступны и проверены экспертами, и не должно возникнуть проблем с раскрытием того, какой вы используете.

– Вам следует с осторожностью относиться к приложениям/службам, использующим «модифицированный» или собственный криптографический метод[^259].

- By default, you should not trust any "Roll your own crypto" until it was audited, peer-reviewed, vetted, and accepted by the cryptography community[^260]'[^261].

- There is no such thing as "military-grade crypto"[^262]'[^263]'[^264].

Cryptography is a complex topic and bad cryptography could easily lead to your de-anonymization.

In the context of this guide,we recommend sticking to Apps/Services using well-established, published, and peer-reviewed methods.

Итак, чему отдать предпочтение и чего следует избегать в 2021 году? Вам придется самостоятельно посмотреть технические подробности каждого приложения и посмотреть, используют ли они «плохую криптовалюту» или «хорошую криптовалюту». Как только вы получите технические подробности, вы можете проверить эту страницу, чтобы узнать, сколько она стоит: <https://latacora.micro.blog/2018/04/03/cryptographic-right-answers.html> <sup>[[Archive.org]](https://web.archive.org/web/https://latacora.micro.blog/2018/04/03/cryptographic-right-answers.html)</sup>

Here are some examples:

- Хэши:

- Предпочитаю: SHA-3 или BLAKE2[^265]

- Все еще относительно нормально использовать: SHA-2 (например, широко используемые SHA-256 или SHA-512)

- Избегайте: SHA-1, MD5 (к сожалению, все еще широко используются), CRC, MD6 (редко используются).

- File/Disk Encryption:

- Предпочитать:

        + Hardware Accelerated[^266]: AES (Rijndael) 256 Bits with HMAC-SHA-2 or HMAC-SHA-3 (This is what Veracrypt, Bitlocker, Filevault 2, KeepassXC, and LUKS use by default). Prefer SHA-3.

        + Non-Hardware Accelerated: Same as accelerated above or if available consider:

            * ChaCha20[^267] or XChaCha20 (You can use ChaCha20 with Kryptor <https://www.kryptor.co.uk>, unfortunately, it is not available with Veracrypt).

* Змей[^268]

* ДвеРыбы[^269]

    - Avoid: Pretty much anything else

- Password Storage:

    - Prefer: Argon2, scrypt
    - If these aren't options, use bcrypt, or if not possible at least PBKDF2 (only as a last resort)
    - Be skeptical of Argon2d, as it's vulnerable to some forms of side-channels. Prefer Argon2i or Argon2id

    - Avoid: SHA-3, SHA-2, SHA-1, MD5

- Browser Security (HTTPS):

    - Prefer: TLS 1.3 (ideally TLS 1.3 with ECH/eSNI support) or at least TLS 1.2 (widely used)

    - Avoid: Anything Else (TLS =<1.1, SSL =<3)

- Подписание сообщений/файлов с помощью GnuPG (GPG):

    - Prefer ECDSA (ed25519)+ECDH (ec25519) or RSA 4096 Bits*

+ **Рассмотрите более современную**[^270] **альтернативу PGP/GPG: Minisign <https://jedisct1.github.io/minisign/>** <sup>[[Archive.org]](https://web.archive.org/web/https://jedisct1.github.io/minisign/)</sup>

    - Avoid: RSA 2048 bits

- SSH-ключи:

    - ED25519 (preferred) or RSA 4096 Bits*

– Избегайте: RSA 2048 бит.

- **Внимание: RSA и ED25519, к сожалению, не считаются «квантово-устойчивыми»**[^271] **и, хотя они еще не взломаны, они, вероятно, будут взломаны когда-нибудь в будущем. Это всего лишь вопрос времени, а не того, будет ли RSA когда-либо сломан. Таким образом, в этих контекстах они предпочтительнее из-за отсутствия лучшей возможности.**

Вот несколько реальных случаев проблем с плохой криптографией:

- Telegram: <https://democratic-europe.eu/2021/07/20/cryptographers-uncover-four-vulnerabilities-in-telegram/> <sup>[[Archive.org]](https://web.archive.org/web/https://democratic-europe.eu/2021/07/20/cryptographers-uncover-four-vulnerabilities-in-telegram/)</sup>

- Telegram: <https://buttondown.email/cryptography-dispatches/archive/cryptography-dispatches-the-most-backdoor-looking/> <sup>[[Archive.org]](https://web.archive.org/web/https://buttondown.email/cryptography-dispatches/archive/cryptography-dispatches-the-most-backdoor-looking/)</sup>

- Криптокот: <https://web.archive.org/web/20130705051050/https://blog.crypto.cat/2013/07/new-critical-vulnerability-in-cryptocat-details/>

– Некоторые другие примеры можно найти здесь: <https://www.cryptofails.com/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.cryptofails.com/)</sup>

Позже это руководство не будет рекомендовать «плохую криптографию», и, надеюсь, этого будет достаточно, чтобы защитить вас?

## Нет политик журнала { #no-log-policies }

Многие люди полагают, что службы, ориентированные на конфиденциальность, такие как VPN или поставщики электронной почты, безопасны благодаря своей политике отсутствия регистрации или схемам шифрования. К сожалению, многие из этих же людей забывают, что все эти провайдеры являются законными коммерческими организациями, подчиняющимися законам стран, в которых они работают.

Любой из этих провайдеров может быть вынужден молча (без вашего ведома (с использованием, например, постановления суда с запретом на затыкание рта[^272] или письма национальной безопасности[^273]) регистрировать вашу активность, чтобы деанонимизировать вас. В последнее время было несколько таких примеров:

- 2021, Протон, Протон зарегистрировал IP-адрес французского активиста по приказу швейцарских властей (ссылка на источник недоступна).

- 2021, WindScribe, серверы не были зашифрованы, поскольку они должны были допускать атаки MITM со стороны властей[^275].

- 2021 г.: серверы DoubleVPN, журналы и информация об учетных записях конфискованы правоохранительными органами[^276].

- 2021 г. Немецкий почтовый провайдер Tutanota был вынужден следить за определенными учетными записями в течение 3 месяцев[^277].

- 2020 г. Немецкий почтовый провайдер Tutanota был вынужден внедрить бэкдор для перехвата и сохранения копий незашифрованных электронных писем одного пользователя[^278] (они не расшифровали сохраненное электронное письмо).

- В 2017 году PureVPN была вынуждена раскрыть информацию одного пользователя ФБР[^279].

- В 2014 г. пользователь EarthVPN был арестован на основании данных, предоставленных поставщиком журналов полиции Нидерландов[^280].

- 2013 г.: поставщик защищенной электронной почты Lavabit закрывается после нарушения секретного приказа о неразглашении информации[^281].

- В 2011 году пользователь HideMyAss был деанонимизирован, а журналы были предоставлены ФБР[^282].

Некоторые провайдеры внедрили использование Warrant Canary[^283], который позволит их пользователям узнать, были ли они скомпрометированы такими заказами, но, насколько нам известно, это еще не тестировалось.

Finally, it is now well known that some companies might be sponsored front ends for some state adversaries (see the Crypto AG story[^284] and Omnisec story[^285]).

For these reasons, you mustn't trust such providers for your privacy despite all their claims. In most cases, you will be the last person to know if any of your accounts were targeted by such orders and you might never know at all.

To mitigate this, in cases where you want to use a VPN, we will recommend the use of a cash/Monero-paid VPN provider over Tor to prevent the VPN service from knowing any identifiable information about you.

Если провайдер VPN ничего о вас не знает, он должен устранить любую проблему, связанную с тем, что он не регистрирует данные, а все равно регистрирует их.

## Some Advanced targeted techniques { #advanced-techniques }

![image17](../media/image17.png)

(Illustration: an excellent movie we highly recommend: Das Leben der Anderen[^286])

Опытные злоумышленники[^287] могут использовать множество продвинутых методов для обхода ваших мер безопасности, если им уже известно, где находятся ваши устройства. Многие из этих методов подробно описаны здесь <https://cyber.bgu.ac.il/advanced-cyber/airgap> <sup>[[Archive.org]](https://web.archive.org/web/https://cyber.bgu.ac.il/advanced-cyber/airgap)</sup> (страница исследования воздушного зазора, Исследовательский центр кибербезопасности, Университет Бен-Гуриона в Негеве, Израиль), а также в этом отчете <https://www.welivesecurity.com/wp-content/uploads/2021/12/eset_jumping_the_air_gap_wp.pdf> <sup>[[Archive.org]](https://web.archive.org/web/https://www.welivesecurity.com/wp-content/uploads/2021/12/eset_jumping_the_air_gap_wp.pdf)</sup> (ESET, JUMPING THE AIR GAP: 15 лет усилий национального государства) и включают в себя:

- Attacks requiring malware implants:

    - Exfiltration of Data through a Malware infected Router: <https://www.youtube.com/watch?v=mSNt4h7EDKo> <sup>[[Invidious]](https://yewtu.be/watch?v=mSNt4h7EDKo)</sup>

    - Exfiltration of Data through observation of Light variation in a Backlit keyboard with a compromised camera: <https://www.youtube.com/watch?v=1kBGDHVr7x0> <sup>[[Invidious]](https://yewtu.be/watch?v=1kBGDHVr7x0)</sup>

        + Exfiltration of Data through a compromised Security Camera (that could first use the previous attack) <https://www.youtube.com/watch?v=om5fNqKjj2M> <sup>[[Invidious]](https://yewtu.be/watch?v=om5fNqKjj2M)</sup>

        + Communication from outsider to compromised Security Cameras through IR light signals: <https://www.youtube.com/watch?v=auoYKSzdOj4> <sup>[[Invidious]](https://yewtu.be/watch?v=auoYKSzdOj4)</sup>

    - Exfiltration of data from a compromised air-gapped computer through acoustic analysis of the FAN noises with a smartphone <https://www.youtube.com/watch?v=v2_sZIfZkDQ> <sup>[[Invidious]](https://yewtu.be/watch?v=v2_sZIfZkDQ)</sup>

    - Exfiltration of data from a malware-infected air-gapped computer through HD LEDs with a Drone <https://www.youtube.com/watch?v=4vIu8ld68fc> <sup>[[Invidious]](https://yewtu.be/watch?v=4vIu8ld68fc)</sup>

    - Exfiltration of data from a USB malware on an air-gapped computer through electromagnetic interferences <https://www.youtube.com/watch?v=E28V1t-k8Hk> <sup>[[Invidious]](https://yewtu.be/watch?v=E28V1t-k8Hk)</sup>

    - Exfiltration of data from a malware-infected HDD drive through covert acoustic noise <https://www.youtube.com/watch?v=H7lQXmSLiP8> <sup>[[Invidious]](https://yewtu.be/watch?v=H7lQXmSLiP8)</sup>

    - Exfiltration of data through GSM frequencies from a compromised (with malware) air-gapped computer <https://www.youtube.com/watch?v=RChj7Mg3rC4> <sup>[[Invidious]](https://yewtu.be/watch?v=RChj7Mg3rC4)</sup>

    - Exfiltration of data through electromagnetic emissions from a compromised Display device <https://www.youtube.com/watch?v=2OzTWiGl1rM&t=20s> <sup>[[Invidious]](https://yewtu.be/watch?v=2OzTWiGl1rM&t=20s)</sup>

    - Exfiltration of data through magnetic waves from a compromised air-gapped computer to a Smartphone stored inside a Faraday bag <https://www.youtube.com/watch?v=yz8E5n1Tzlo> <sup>[[Invidious]](https://yewtu.be/watch?v=yz8E5n1Tzlo)</sup>

    - Communication between two compromised air-gapped computers using ultrasonic soundwaves <https://www.youtube.com/watch?v=yz8E5n1Tzlo> <sup>[[Invidious]](https://yewtu.be/watch?v=yz8E5n1Tzlo)</sup>

    - Exfiltration of Bitcoin Wallet from a compromised air-gapped computer to a smartphone <https://www.youtube.com/watch?v=2WtiHZNeveY> <sup>[[Invidious]](https://yewtu.be/watch?v=2WtiHZNeveY)</sup>

    - Exfiltration of Data from a compromised air-gapped computer using display brightness <https://www.youtube.com/watch?v=ZrkZUO2g4DE> <sup>[[Invidious]](https://yewtu.be/watch?v=ZrkZUO2g4DE)</sup>

    - Exfiltration of Data from a compromised air-gapped computer through vibrations <https://www.youtube.com/watch?v=XGD343nq1dg> <sup>[[Invidious]](https://yewtu.be/watch?v=XGD343nq1dg)</sup>

    - Exfiltration of Data from a compromised air-gapped computer by turning RAM into a Wi-Fi emitter <https://www.youtube.com/watch?v=vhNnc0ln63c> <sup>[[Invidious]](https://yewtu.be/watch?v=vhNnc0ln63c)</sup>

    - Exfiltration of Data from a compromised air-gapped computer through power lines <https://arxiv.org/pdf/1804.04014.pdf> <sup>[[Archive.org]](https://web.archive.org/web/https://arxiv.org/pdf/1804.04014.pdf)</sup>

- **Attacks not requiring malware:**

    - Observing a blank wall in a room from a distance to figure how many people are in a room and what they are doing[^288]. Publication with demonstration: <http://wallcamera.csail.mit.edu/> <sup>[[Archive.org]](https://web.archive.org/web/http://wallcamera.csail.mit.edu/)</sup>

    - Observing a reflective bag of snacks in a room from a distance to reconstruct the entire room[^289]. Publication with photographic examples: <https://arxiv.org/pdf/2001.04642.pdf> <sup>[[Archive.org]](https://web.archive.org/web/https://arxiv.org/pdf/2001.04642.pdf)</sup>

    - Measuring floor vibrations to identify individuals and determine their health condition and mood[^290]. Publication with demonstration: <https://engineering.cmu.edu/news-events/news/2020/02/17-mauraders-map.html> <sup>[[Archive.org]](https://web.archive.org/web/https://engineering.cmu.edu/news-events/news/2020/02/17-mauraders-map.html)</sup>

    - Observing a light bulb from a distance to listen to the sound in the room[^291] **without any malware**: Demonstration: <https://www.youtube.com/watch?v=t32QvpfOHqw> <sup>[[Invidious]](https://yewtu.be/watch?v=t32QvpfOHqw)</sup>. It should be noted that this type of attack is not new at all and there have been articles about such techniques as far back as 2013[^292] and that you can even buy devices to perform this yourself such as here: <http://www.gcomtech.com/ccp0-prodshow/laser-surveillance-laser-listening.html> <sup>[[Archive.org]](https://web.archive.org/web/http://www.gcomtech.com/ccp0-prodshow/laser-surveillance-laser-listening.html)</sup>

Here is also a good video from the same authors to explain those topics: Black Hat, The Air-Gap Jumpers <https://www.youtube.com/watch?v=YKRtFgunyj4> <sup>[[Invidious]](https://yewtu.be/watch?v=YKRtFgunyj4)</sup>

**Realistically, this guide will be of little help against such adversaries as such malware could be implanted on the devices by a manufacturer, anyone in the middle**[^293]**, or by anyone with physical access to the air-gapped computer but there are still some ways to mitigate such techniques:**

- Do not conduct sensitive activity while connected to an untrusted/unsecured power line to prevent power line leaks.

- Do not use your devices in front of a camera that could be compromised.

- Use your devices in a soundproofed room to prevent sound leaks.

- Use your devices in a Faraday cage to prevent electromagnetic leaks.

- Do not talk about sensitive information where lightbulbs could be seen from outside.

- Buy your devices from different/unpredictable/offline places (shops) where the probability of them being infected with such malware is lower.

- Do not let anyone access your air-gapped computers except trusted people.

## Некоторые бонусные ресурсы { #bonus-resources }

- Have a look at the Whonix Documentation concerning Data Collection techniques here: [Data Collection Techniques](https://www.whonix.org/wiki/Data_Collection_Techniques) <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Data_Collection_Techniques)</sup>

- You might also enjoy looking at this service <https://tosdr.org/> <sup>[[Archive.org]](https://web.archive.org/web/https://tosdr.org/)</sup> (Terms of Services, Didn't Read) that will give you a good overview of the various ToS of many services.

- Have a look at <https://www.eff.org/issues/privacy> <sup>[[Archive.org]](https://web.archive.org/web/https://www.eff.org/issues/privacy)</sup> for some more resources.

- Have a look at <https://en.wikipedia.org/wiki/List_of_government_mass_surveillance_projects> <sup>[[Wikiless]](https://wikiless.tiekoetter.com/wiki/List_of_government_mass_surveillance_projects)</sup> <sup>[[Archive.org]](https://web.archive.org/web/https://en.wikipedia.org/wiki/List_of_government_mass_surveillance_projects)</sup> to have an overview of all known mass-surveillance projects, current, and past.

- Have a look at <https://www.gwern.net/Death-Note-Anonymity> <sup>[[Archive.org]](https://web.archive.org/web/https://www.gwern.net/Death-Note-Anonymity)</sup> (even if you don't know about Death Note).

- Рассмотрите возможность найти и прочитать книгу Майкла Баззелла «Техники разведки с открытым исходным кодом» (восьмое издание на момент написания этой статьи, чтобы узнать больше о последних методах OSINT) <https://inteltechniques.com/book1.html>

– Наконец, проверьте <https://www.freehaven.net/anonbib/date.html> <sup>[[Archive.org]](https://web.archive.org/web/https://www.freehaven.net/anonbib/date.html)</sup>, чтобы найти последние научные статьи, посвященные анонимности в Интернете.

**Примечания**

Если вы все еще не считаете, что такая информация может использоваться различными субъектами для отслеживания вас, вы можете сами просмотреть некоторую статистику для некоторых платформ и иметь в виду, что она учитывает только законные запросы данных и не учитывает такие вещи, как PRISM, MUSCULAR, SORM или XKEYSCORE, описанные ранее:

– Отчет Google о прозрачности <https://transparencyreport.google.com/user-data/overview> <sup>[[Archive.org]](https://web.archive.org/web/https://transparencyreport.google.com/user-data/overview)</sup>

- Отчет о прозрачности Facebook <https://transparency.facebook.com/> <sup>[[Archive.org]](https://web.archive.org/web/https://transparency.facebook.com/)</sup>

- Отчет Apple о прозрачности <https://www.apple.com/legal/transparency/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.apple.com/legal/transparency/)</sup>

- Cloudflare Transparency Report <https://www.cloudflare.com/transparency/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.cloudflare.com/transparency/)</sup>

- Отчет о прозрачности Snapchat <https://www.snap.com/en-US/privacy/transparency> <sup>[[Archive.org]](https://web.archive.org/web/https://www.snap.com/en-US/privacy/transparency)</sup>

- Отчет о прозрачности Telegram <https://t.me/transparency> <sup>[[Archive.org]](https://web.archive.org/web/https://t.me/transparency)</sup> (требуется установленный Telegram)

- Отчет Microsoft о прозрачности <https://www.microsoft.com/en-us/corporate-responsibility/law-enforcement-requests-report> <sup>[[Archive.org]](https://web.archive.org/web/https://www.microsoft.com/en-us/corporate-responsibility/law-enforcement-requests-report)</sup>

- Отчет о прозрачности Amazon <https://www.amazon.com/gp/help/customer/display.html?nodeId=GYSDRGWQ2C2CRYEF> <sup>[[Archive.org]](https://web.archive.org/web/https://www.amazon.com/gp/help/customer/display.html?nodeId=GYSDRGWQ2C2CRYEF)</sup>

- Отчет о прозрачности Dropbox <https://www.dropbox.com/transparency> <sup>[[Archive.org]](https://web.archive.org/web/https://www.dropbox.com/transparency)</sup>

- Отчет о прозрачности разногласий <https://discord.com/blog/discord-transparency-report-q1-2022> <sup>[[Archive.org]](https://web.archive.org/web/20220812051950/https://discord.com/blog/discord-transparency-report-q1-2022)</sup>

- Отчет о прозрачности GitHub <https://github.blog/2021-02-25-2020-transparency-report/> <sup>[[Archive.org]](https://web.archive.org/web/https://github.blog/2021-02-25-2020-transparency-report/)</sup>

- Отчет о прозрачности Snapchat <https://www.snap.com/en-US/privacy/transparency/> <sup>[[Archive.org]](https://web.archive.org/web/20220806141853/https://www.snap.com/en-US/privacy/transparency)</sup>

- Отчет о прозрачности TikTok <https://www.tiktok.com/transparency/en/information-requests-2021-2/> <sup>[[Archive.org]](https://web.archive.org/web/20220812054600/https://www.tiktok.com/transparency/en/information-requests-2021-2/)</sup>

- Отчет о прозрачности Reddit <https://www.redditinc.com/policies/transparency-report-2021> <sup>[[Archive.org]](https://web.archive.org/web/20220812054736/https://www.redditinc.com/policies/transparency-report-2021)</sup>

- Отчет о прозрачности Твиттера <https://transparency.twitter.com/> <sup>[[Archive.org]](https://web.archive.org/web/20220812054839/https://transparency.twitter.com/)</sup>

# Общие приготовления { #general-preparations }

Personally, in the context of this guide, it is also interesting to have a look at your security model. And in this context,we only have one to recommend:

Безопасность с нулевым доверием[^391] («Никогда не доверяй, всегда проверяй»).

Here are some various resources about what Zero-Trust Security is:

- DEFCON, Zero Trust a Vision for Securing Cloud, <https://www.youtube.com/watch?v=euSsqXO53GY> <sup>[[Invidious]](https://yewtu.be/watch?v=euSsqXO53GY)</sup>

- От самого АНБ, «Принятие модели безопасности с нулевым доверием», <https://media.defense.gov/2021/Feb/25/2002588479/-1/-1/0/CSI_EMBRACING_ZT_SECURITY_MODEL_UOO115131-21.PDF> <sup>[[Archive.org]](https://web.archive.org/web/https://media.defense.gov/2021/Feb/25/2002588479/-1/-1/0/CSI_EMBRACING_ZT_SECURITY_MODEL_UOO115131-21.PDF)</sup>

## Picking your route { #picking-route }

First, here is a small basic UML diagram showing your available options according to your skills/budget/time/resources.

![image18](../media/image18.png)

### Timing limitations { #timing-limitations }

- You have no time at all:

    - **Go for the Tor Browser route.**

- You have extremely limited time to learn and need a fast-working solution:

    - **Your best option is to go for [the Tails route](#tails-route) (excluding the persistent plausible deniability section).**

- You have time and more importantly motivation to learn:

    - **Go with any route.**

### Budget & Material limitations { #budget-limitations }

- You have no budget and even accessing a laptop is complicated or you only have your smartphone:

    - **Go for the Tor Browser route.**

- You only have one laptop available and cannot afford anything else. You use this laptop for either work, family, or your personal stuff (or both):

    - **Your best option is to go for [the Tails route](#tails-route).**

- You can afford a spare dedicated unsupervised/unmonitored laptop for your sensitive activities:

    - But it is old, slow, and has bad specs (less than 6GB of RAM, less than 250GB disk space, old/slow CPU):

        + **You should go for [the Tails route](#tails-route).**

    - It is not that old, and it has decent specs (at least 8GB of RAM, 250GB of disk space or more, decent CPU):

        + **You could go for Tails, Whonix routes.**

    - It is new and it has great specs (more than 16GB or ideally 32GB of RAM, >250GB of disk space, recent fast CPU):

        + **You could go for any route, but we would recommend Qubes OS if your threat model allows it. Please see the requirements.[^363]**

    - If it is an ARM-based M1/M2 Mac:

        + **Not possible currently for these reasons:**

            * Virtualization of Intel x86 images on ARM (M1/M2) hosts is still limited to commercial software (e.g., Parallels, Fusion) which are mostly not supported by Whonix, yet. They are very buggy and for advanced people only. Please seek this information yourself.

            * [Virtualbox is now available natively for ARM64 architecture](https://osxdaily.com/2022/10/22/you-can-now-run-virtualbox-on-apple-silicon-m1-m2/) in a package as of October 2022. Download the ["Developer preview for macOS/Arm64 (M1/M2) hosts"](https://www.virtualbox.org/wiki/Downloads).

            * Whonix does not support macOS easily. "You need to build Whonix using the build script to get it running on Apple Silicon." [See the forum thread](https://www.whonix.org/wiki/MacOS#M1).

            * Tails is not supported on ARM64 architecture yet. [See this thread](https://gitlab.tails.boum.org/tails/blueprints/-/wikis/ARM_platforms/) for more information (keep in mind this page hasn't been updated recently).

            * Qubes OS is not supported on ARM64 architecture yet, but there is work being done to make it available on aarch64, which may be delayed for the unforseeable future..

**The general advice in this guide regarding virtualization software is that it's costly. That said, you should probably get a dedicated laptop, capable of running virtualization software, preferably a 64-bit architecture, to be used for more sensitive activities and testing.**

### Skills { #skills }

- Do you have no IT skills at all the content of this guide look like an alien language to you? Consider:

    - **The Tor Browser route (simplest of all)**

    - **[The Tails route](#tails-route) (excluding the persistent plausible deniability section).**

- You have some IT skills and mostly understand this guide so far, consider:

    - **The Tails route (with the optional persistent plausible deniability section).**

    - **The Whonix route.**

- You have moderate to high IT skills, and you are already familiar with some of the content of this guide, consider:

    - **Any route (Qubes OS is preferred if you can afford it).**

- You are an l33T hacker, "there is no spoon", "the cake is a lie", you have been using "doas" for years, and "all your base is belong to us", and you have strong opinions on systemd.

    - **This guide is not meant for you and will not help you with your HardenedBSD on your hardened Libreboot laptop ;-)**

### Adversarial considerations { #adversarial-considerations }

Now that you know what is possible, you should also consider threats and adversaries before picking the right route.

#### Threats { #threats }

- If your main concern is a forensic examination of your devices, you should consider the Tor Browser route or [the Tails route](#tails-route).

- If your main concerns are remote adversaries that might uncover your online identity on various platforms, you should consider the Tails, Whonix, or Qubes OS routes (listed in order of difficulty).

- If you want system-wide plausible deniability[^311]'[^294] despite the risks[^295]'[^314], consider the Tails route, including the persistent plausible deniability section (see [Persistent Plausible Deniability using Whonix & Tails](#whonix-tails-deniability)).**

- If you are in a hostile environment where Tor/VPN usage alone is impossible/dangerous/suspicious, consider the Tails route (without actually using Tor), or more advanced routes like Whonix or Qubes OS.

#### Adversaries { #adversaries }

- Low skills:

    - Low resources:

        + Any motivation: Any Route

    - Medium resources:

        + Low to Medium motivation: Any Route

        + High motivation: TAILS, Whonix, Qubes OS Routes

    - High resources:

        + Low motivation: Any route

        + Medium to High motivation: TAILS, Whonix, Qubes OS Routes

- Intermediate skills:

    - Low resources:

        + Low motivation: Any Route

        + Medium to High motivation: TAILS, Whonix, Qubes OS Routes

    - Medium resources:

        + Low motivation: Any Route

        + Medium to High motivation: TAILS, Whonix, Qubes OS Routes

    - High resources:

        + Low to High motivation: TAILS, Whonix, Qubes OS Routes

- Highly skilled:

    - Low resources:

        + Low motivation: Any Route

        + Medium to High motivation: TAILS, Whonix, Qubes OS Routes

    - Medium resources:

        + Low to High motivation: TAILS, Whonix, Qubes OS Routes

    - High resources:

        + Low to High motivations: TAILS, Whonix, Qubes OS Routes **(but likely out of scope from this guide as this is probably a global adversary)**

In all cases, you should read these two pages from the Whonix documentation that will give you in-depth insight into your choices:

- [Warning](https://www.whonix.org/wiki/Warning) <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Warning)</sup>
- [Dev/Threat Model](https://www.whonix.org/wiki/Dev/Threat_Model) <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Dev/Threat_Model)</sup>
- [Comparison with Others](https://www.whonix.org/wiki/Comparison_with_Others) <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Comparison_with_Others)</sup>

You might be asking yourself: "How do I know if I'm in a hostile online environment where activities are actively monitored and blocked?"

- First read more about it at the EFF here: <https://ssd.eff.org/en/module/understanding-and-circumventing-network-censorship> <sup>[[Archive.org]](https://web.archive.org/web/https://ssd.eff.org/en/module/understanding-and-circumventing-network-censorship)</sup>

- Check some data yourself here on the Tor Project OONI[^296] (Open Observatory of Network Interference) website: <https://explorer.ooni.org/>

- Have a look at <https://censoredplanet.org/> and see if they have data about your country.

- Specific to China, look at <https://gfwatch.org/> and <https://www.usenix.org/system/files/sec21-hoang.pdf> <sup>[[Archive.org]](https://web.archive.org/web/https://www.usenix.org/system/files/sec21-hoang.pdf)</sup>

- Test for yourself using OONI (this can be risky in a hostile environment).

## Steps for all routes { #steps-all-routes }

### Getting used to using better passwords { #better-passwords }

See [Guidelines for passwords and passphrases](#password-guidelines).

### Getting an anonymous Phone number { #anonymous-phone }

**Skip this step if you have no intention of creating anonymous accounts on most mainstream platforms but just want anonymous browsing or if the platforms you will use allow registration without a phone number.**

#### Physical Burner Phone and prepaid SIM card { #burner-phone }

##### Get a burner phone { #get-burner-phone }

This is rather easy. Leave your smartphone on and at home. Have some cash and go to some random flea market or small shop (ideally one without CCTV inside or outside and while avoiding being photographed/filmed) and just buy the cheapest phone you can find with cash and without providing any personal information. It only needs to be in working order.

_A note regarding your current phone:_ The point of leaving your smartphone on is to create avoid leaking the fact that you're not using the device. If a smartphone is turned off, this creates a metadata trail that can be used to correlate the time your smartphone was turned off with the activation of your burner. If possible, leave your phone doing something (for example, watching YouTube on auto-play) to obscure the metadata trail further. This will not make it impossible to correlate your inactivity, but may make it more difficult if your phone's usage patterns can look convincing while you buy your burner.

We would recommend getting an old "dumbphone" with a removable battery (old Nokia if your mobile networks still allow those to connect as some countries phased out 1G-2G completely). This is to avoid the automatic sending/gathering of any telemetry/diagnostic data on the phone itself. You should never connect that phone to any Wi-Fi.

**Site Note: Be careful of some sellers as shown here <https://therecord.media/malware-found-preinstalled-in-classic-push-button-phones-sold-in-russia>** <sup>[[Archive.org]](https://therecord.media/malware-found-preinstalled-in-classic-push-button-phones-sold-in-russia)</sup>

It will also be crucial not to power on that burner phone ever (not even without the SIM card) in any geographical location that could lead to you (at your home/work for instance) and never at the same location as your other known smartphone (because that one has an IMEI/IMSI that will easily lead to you). This might seem like a big burden, but it is not as these phones are only being used during the setup/sign-up process and for verification from time to time.

See [Warning about smartphones and smart devices](#smartphones-warning)

You should test that the phone is in working order before going to the next step. But we will repeat ourselves and state that it is important to leave your smartphone at home when going (or turn it off before leaving if you must keep it) and that you test the phone at a random location that cannot be tracked back to you (and again, do not do that in front of a CCTV, avoid cameras, be aware of your surroundings). No need for Wi-Fi at this place either.

When you are certain the phone is in working order, disable Bluetooth then power it off (remove the battery if you can) and go back home and resume your normal activities. Go to the next step.

##### Getting an anonymous pre-paid SIM card { #prepaid-sim }

This is the hardest part of the whole guide. It is a SPOF (Single Point of Failure). The places where you can still buy prepaid SIM cards without ID registration are getting increasingly limited due to various KYC type regulations[^297].

So here is a list of places where you can still get them now: <https://prepaid-data-sim-card.fandom.com/wiki/Registration_Policies_Per_Country> <sup>[[Archive.org]](https://web.archive.org/web/https://prepaid-data-sim-card.fandom.com/wiki/Registration_Policies_Per_Country)</sup>

You should be able to find a place that is "not too far" and just go there physically to buy some pre-paid cards and top-up vouchers with cash. Do verify that no law was passed before going that would make registration mandatory (in case the above wiki was not updated). Try to avoid CCTV and cameras and do not forget to buy a Top-Up voucher with the SIM card (if it is not a package) as most pre-paid cards will require a top-up before use.

See [Warning about smartphones and smart devices](#smartphones-warning)

Double-check that the mobile operators selling the pre-paid SIM cards will accept the SIM activation and top-up without any ID registration of any kind before going there. Ideally, they should accept SIM activation and top-up from the country you live in.

We would recommend GiffGaff in the UK as they are "affordable", do not require identification for activation and top-up, and will even allow you to change your number up to two times from their website. One GiffGaff prepaid SIM card will therefore grant you three numbers to use for your needs.

Выключайте телефон после активации/пополнения счета и перед тем, как идти домой. Никогда не включайте его снова, если вы не находитесь в месте, которое можно использовать для раскрытия вашей личности, и в идеале оставьте свой настоящий телефон включенным, но дома, прежде чем отправиться в безопасное место только с одноразовым телефоном.

#### Online Phone Number { #online-phone-number }

**DISCLAIMER: Do not attempt this until you are done setting up a secure environment according to one of the selected routes. This step will require online access and should only be done from an anonymous network. Do not do this from any known/unsecured environment. Skip this until you have finished one of the routes.**

There are many commercial services offering numbers to receive SMS messages online but most of those have no anonymity/privacy and can be of no help as most Social Media platforms place a limit on how many times a phone number can be used for registration.

There are some forums and subreddits (like r/phoneverification/) where users will offer the service of receiving such SMS messages for you for a small fee (using PayPal or some crypto payment). Unfortunately, these are full of scammers and very risky in terms of anonymity. **You should not use those under any circumstance.**

To this date, we do not know any reputable service that would offer this service and accept cash payments (by post for instance) like some VPN providers. But a few services are providing online phone numbers and do accept Monero which could be reasonably anonymous (yet less recommended than that physical way in the earlier chapter) that you could consider:

- **Recommended**: Do not require any identification (even e-mail):

    - (Iceland based, accepts Monero) <https://crypton.sh> <sup>[[Tor Mirror]](http://cryptonx6nsmspsnpicuihgmbbz3qvro4na35od3eht4vojdo7glm6yd.onion)</sup> <sup>[[Archive.org]](https://web.archive.org/web/https://crypton.sh/)</sup>

    - (Ukraine based, accepts Monero) <https://virtualsim.net/> <sup>[[Archive.org]](https://web.archive.org/web/https://virtualsim.net/)</sup>

- Do require identification (valid e-mail):

    - (US California based, accepts Monero) <https://mobilesms.io> <sup>[[Archive.org]](https://web.archive.org/web/https://mobilesms.io/)</sup>

    - (Germany based, accepts Monero) <https://www.sms77.io/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.sms77.io/)</sup>

    - (Russia based, accepts Monero) <https://onlinesim.ru/> <sup>[[Archive.org]](https://web.archive.org/web/https://onlinesim.ru/)</sup>

There are some other possibilities listed here <https://cryptwerk.com/companies/sms/xmr/> <sup>[[Archive.org]](https://web.archive.org/web/https://cryptwerk.com/companies/sms/xmr/)</sup>. **Use at your own risk.**

Now, what if you have no money? Well, in that case, you will have to try your luck with free services and hope for the best. Here are some examples, **use at your own risk**:

- <https://oksms.org>

- <https://smspva.com>

- <https://sms24.me>

**Disclaimer: We cannot vouch for any of these providers. We recommend doing it yourself physically. In this case, you will have to rely on the anonymity of Monero and you should not use any service that requires any kind of identification using your real identity. Please do read [Monero Disclaimer](#monero-disclaimer).**

It is more convenient, cheaper, and less risky to just get a pre-paid SIM card from one of the physical places that still sell them for cash without ID.

### Get a USB key { #usb-key }

**Skip this step if you have no intention of creating anonymous accounts on most mainstream platforms, but you will want anonymous browsing; or if the platforms which you will use allow registration without a phone number.**

Get at least one or two decent size generic USB keys (at least 16GB but we would recommend 32GB).

Please do not buy or use gimmicky self-encrypting devices such as these: <https://syscall.eu/blog/2018/03/12/aigo_part1/> <sup>[[Archive.org]](https://web.archive.org/web/https://syscall.eu/blog/2018/03/12/aigo_part1/)</sup>

Some might be very efficient[^298] but many are gimmicky gadgets that offer no real protection[^299].

### Find some safe places with decent public Wi-Fi { #safe-wifi }

You need to find safe places where you will be able to do your sensitive activities using some publicly accessible Wi-Fi (without any account/ID registration, avoid CCTVs).

This can be anywhere that will not be tied to you directly (your home/work) and where you can use the Wi-Fi for a while without being bothered. But also, a place where you can do this without being "noticed" by anyone.

If you think Starbucks is a clever idea, you may reconsider:

- They probably have CCTVs in all their shops and keep those recordings for an unknown amount of time.

- You will need to buy a coffee to get the Wi-Fi access code in most. If you pay for this coffee with an electronic method, they will be able to tie your Wi-Fi access with your identity.

Situational awareness is key, and you should be constantly aware of your surroundings and avoid touristy places like it was plagued by Ebola. You want to avoid appearing on any picture/video of anyone while someone is taking a selfie, making a TikTok video, or posting some travel pictures on their Instagram. If you do, remember chances are high that those pictures will end up online (publicly or privately) with full metadata attached to them (time/date/geolocation) and your face. Remember these can and will be indexed by Facebook/Google/Yandex/Apple and probably all three letters' agencies.

While this will not be available yet to your local police officers, it could be in the near future.

You will ideally need a set of 3-5 separate places such as this to avoid using the same place twice. Several trips will be needed over the weeks for the various steps in this guide.

You could also consider connecting to these places from a safe distance for added security. See [Using long-range Antenna to connect to Public Wi-Fis from a safe distance.](#long-range-wifi)

## The Tor Browser route { #tor-browser-route }

This part of the guide will help you in setting up the simplest and easiest way to browse the web anonymously. It is not necessarily the best method and there are more advanced methods below with (much) better security and (much) better mitigations against various adversaries. Yet, this is a straightforward way of accessing resources anonymously and quickly with no budget, no time, no skills, and limited usage.

So, what is Tor Browser? Tor Browser (<https://www.torproject.org/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.torproject.org/)</sup>) is a web browser like Safari/Firefox/Chrome/Edge/Brave designed with privacy and anonymity in mind.

This browser is different from other browsers as it will connect to the internet through the Tor Network using Onion Routing. We first recommend that you watch this very nice introduction video by the Tor Project themselves: <https://www.youtube.com/watch?v=JWII85UlzKw> <sup>[[Invidious]](https://yewtu.be/watch?v=JWII85UlzKw)</sup>. After that, you should probably head over to their page to read their quick overview here: <https://2019.www.torproject.org/about/overview.html.en> <sup>[[Archive.org]](https://web.archive.org/web/https://2019.www.torproject.org/about/overview.html.en)</sup>. Without going into too many technical details, Tor Browser is an easy and simple "fire and forget" solution to browse the web anonymously from pretty much any device. It is probably sufficient for most people and can be used from any computer or smartphone.

Here are several ways to set it up for all main OSes.

**Warning:** You should avoid installing extensions in Tor Browser, as they can be used to fingerprint and identify you.

### Windows, Linux, and macOS { #tor-windows-linux-macos }

Please see [Installing and using desktop Tor Browser](#desktop-tor-browser).

### Android { #tor-android }

**Note on Tor Browser for Android: The development of Tor Browser for Android is behind desktop Tor Browser Bundle (TBB). Some features are not available yet. E.g., the desktop version of Tor now enables automatic bridges using Moat:**

"**Connection Assist** works by looking up and downloading an up-to-date list of country-specific options to try using your location (with your consent). It manages to do so without needing to connect to the Tor Network first by utilizing [moat](https://support.torproject.org/glossary/moat/) – the same domain-fronting tool that Tor Browser uses to request a bridge from torproject.org."

- Head over to:

    - Play Store: <https://play.google.com/store/apps/details?id=org.torproject.torbrowser>

    - F-Droid Store: It's not yet there but you can add it manually following the instructions at <https://support.torproject.org/tormobile/tormobile-7/> <sup>[[Archive.org]](https://web.archive.org/web/https://support.torproject.org/tormobile/tormobile-7/)</sup>

- Install

- Launch Tor Browser

- After launching, click the upper right **Settings** icon

- Select **Settings** > **Privacy and security** > **Tor network**

- Select **Config Bridge**.

- Read [Using Tor bridges in hostile environments](#tor-bridges).

- **If needed (after reading the appendix above)**, activate the option and select the type of bridge you want:

    - Obfs4

    - Meek-Azure

    - Snowflake

- **If your internet isn't censored**, consider running one of the bridge types to help the network!

    - Easy: Obsf4 - You can run your own Obsf4 easily with these instructions. <https://community.torproject.org/relay/setup/bridge/>

    - Medium: Snowflake - More about Snowflakes here. <https://snowflake.torproject.org/>

    - Hard: Meek - This is the documentation. It's not as simple. <https://gitlab.torproject.org/legacy/trac/-/wikis/doc/meek/#how-to-run-a-meek-server-bridge>

Personally, if you need to use a Bridge (this is not necessary for a non-hostile environment), you should pick a Meek-Azure. Those will probably work even if you are in China and want to bypass the Great Firewall. It is probably the best option to obfuscate your Tor activities if needed and Microsoft servers are usually not blocked.

_Only available for Desktop Tor users: Recently, the Tor Project has made it incredibly simple to access Bridges with **Connection Assist**, and it is now automatically done in hostile or censored regions. Simply open the Tor Browser and the connection will be configured based on your needs on any hostile network. Previously, we had a list of options below this paragraph which were necessary to enable and configure bridges, but now that this is done automatically using [moat](https://support.torproject.org/glossary/moat/)._ <sup>[[Archive.org]](https://web.archive.org/web/20220801151048/https://support.torproject.org/glossary/moat/)</sup>

- You are almost done

As with the desktop version, you need to know there are safety levels in Tor Browser. On Android, you can access these by following these steps:

- Click the menu (bottom right)

- Click **Settings**.

- Head over to the **Privacy and security** section.

- Click **Security Settings**.

You will find details about each level here: <https://tb-manual.torproject.org/security-settings/> <sup>[[Archive.org]](https://web.archive.org/web/https://tb-manual.torproject.org/security-settings/)</sup> but here is a summary:

- Standard (the default):

    - All features are enabled (including JavaScript)

- Safer:

    - JavaScript is disabled on non-HTTPS websites

    - Some fonts and symbols are disabled

    - Any media playback is "click to play" (disabled by default)

- Safest:

    - Javascript is disabled everywhere

    - Some fonts and symbols are disabled

    - Any media playback is "click to play" (disabled by default)

We would recommend the "Safer" level for most cases. The Safest level should be enabled if you think you are accessing suspicious or dangerous websites and/or if you are extra paranoid.

If you are extra paranoid, use the "Safest" level by default and consider downgrading to Safer is the website is unusable because of Javascript blocking.

However, the Safer level should be used with some extra precautions while using some websites: see [Additional browser precautions with JavaScript enabled](#browser-precautions-js).

Now, you are really done, and you can now surf the web anonymously from your Android device.

**Please see** [Warning for using Orbot on Android](#orbot-android-warning).

### iOS { #tor-ios }

**Disclaimer: Onion Browser, following a 2018 release on iOS, has had IP leaks via WebRTC. It is still the only officially endorsed browser for the Tor network for iOS. Users should exercise caution when using the browser and check for any DNS leaks.**

While the official Tor Browser is not yet available for iOS, there is an alternative called Onion Browser endorsed by the Tor Project[^300].

- Head over to <https://apps.apple.com/us/app/onion-browser/id519296448>

- Install

- Disable Wi-Fi and Mobile Data

- Launch Onion Browser

- After Launching, click the upper right Settings icon (Disabling Wi-Fi and Mobile Data previously were to prevent Onion Browser from connecting automatically and to allow access to these options).

- Select "Bridge Configuration" and read [Using Tor bridges in hostile environments](#tor-bridges)

- **If needed (after reading the appendix above)**, activate the option and select the type of bridge you want:

    - Obfs4

    - Snowflake

    - (Meek-Azure is unfortunately not available on Onion Browser for iOS (See [commit 21bc18428](https://github.com/OnionBrowser/OnionBrowser/commit/21bc18428368224507b27ee58464ad352f4ec810) for more information.)

- **If your internet isn't censored**, consider running one of the bridge types to help the network!

    - Easy: Obsf4 - You can run your own Obsf4 easily with these instructions. <https://community.torproject.org/relay/setup/bridge/>

    - Medium: Snowflake - More about Snowflakes here. <https://snowflake.torproject.org/>

    - Hard: Meek - This is the documentation. It's not as simple. <https://gitlab.torproject.org/legacy/trac/-/wikis/doc/meek/#how-to-run-a-meek-server-bridge>

Personally, if you need to use a Bridge (this is not necessary for a non-hostile environment), you should pick a Snowflake one (since Meek-Azure bridges are not available). Those will probably work even if you are in China and want to bypass the Great Firewall. It is probably the best option you have on iOS.

- You are almost done

As with the desktop version, you need to know there are safety levels in Onion Browser. On iOS, you can access these by following these steps:

- Click the shield icon (upper left)

- You will have three levels to pick from

| Security Level | JavaScript | WS/XHR/Geo | A/V | Apps | WebRTC | HTTP↔HTTPS | Ads/Pop-ups |
  |-------|------------|-------------|------|------|---------|------------|-------------|
  | **Gold** | Disabled | Disabled | No | Blocked | Blocked | Blocked | Blocked |
  | Silver | Partially allowed | Disabled | No | Blocked | Blocked | Blocked | Blocked |
  | Bronze | Allowed | Enabled | Allowed | Blocked | Not blocked | Not blocked | Blocked |

We would recommend the "Silver" level for most cases. The Gold level should only be enabled if you think you are accessing suspicious or dangerous websites or if you are extra paranoid. The Gold mode will also most likely break many websites that rely actively on JavaScript.

As JavaScript is enabled in the Silver mode, please see [Additional browser precautions with JavaScript enabled](#browser-precautions-js).

Now, you are really done, and you can now surf the web anonymously from your iOS device.

### Important Warning { #important-warning }

**This route is the easiest but is not designed to resist highly skilled adversaries. It is however usable on any device regardless of the configuration. This route is also vulnerable to correlation attacks (See [Your Anonymized Tor/VPN traffic](#traffic-anonymization)) and is blind to anything that might be on your device (this could be any malware, exploit, virus, remote administration software, parental controls...). Yet, if your threat model is quite low, it is probably sufficient for most people.**

If you have time and want to learn, we recommend going for other routes instead as they offer far better security and mitigate far more risks while lowering your attack surface considerably.

## The Tails route { #tails-route }

This part of the guide will help you in setting up Tails if one of the following is true:

- You cannot afford a dedicated laptop

- Your dedicated laptop is just too old and too slow

- You have very low IT skills

- You decide to go with Tails anyway

Tails[^301] stands for **The Amnesic Incognito Live System**. It is a bootable Live Operating System running from a USB key that is designed for leaving no traces and forcing all connections through the Tor network.

You insert the Tails USB key into your laptop, boot from it and you have a full operating system running with privacy and anonymity in mind. As soon as you shut down the computer, everything will be gone unless you saved it somewhere.

Tails is an amazingly straightforward way to get going in no time with what you have and without much learning. It has extensive documentation and tutorials.

**WARNING: Tails is not always up to date with their bundled software. And not always up to date with the Tor Browser updates either. You should always make sure you are using the latest version of Tails and you should use extreme caution when using bundled apps within Tails that might be vulnerable to exploits and reveal your location**[^302]**.**

It does however have some drawbacks:

- Tails uses Tor and therefore you will be using Tor to access any resource on the internet. This alone will make you suspicious to most platforms where you want to create anonymous accounts (this will be explained in more detail later).

- Your ISP (whether it is yours or some public Wi-Fi) will also see that you are using Tor, and this could make you suspicious in itself.

- Tails does not include (natively) some of the software you might want to use later which will complicate things quite a bit if you want to run some specific things (Android Emulators for instance).

- Tails uses Tor Browser which while it is very secure will be detected as well by most platforms and will hinder you in creating anonymous identities on many platforms.

- Tails will not protect you more from the 5$ wrench[^11].

- Tor in itself might not be enough to protect you from an adversary with enough resources as explained earlier.

**Important Note: If your laptop is monitored/supervised and some local restrictions are in place, please read** [How to bypass (some) local restrictions on supervised computers](#bypass-local-restrictions)**.**

You should also read Tails Documentation, Warnings, and limitations, before going further <https://tails.boum.org/doc/about/warnings/index.en.html> <sup>[[Archive.org]](https://web.archive.org/web/https://tails.boum.org/doc/about/warnings/index.en.html)</sup>

Принимая все это во внимание, а также тот факт, что их документация великолепна, мы просто перенаправим вас к их хорошо сделанному и хорошо поддерживаемому руководству:

<https://tails.boum.org/install/index.en.html> <sup>[[Archive.org]](https://web.archive.org/web/https://tails.boum.org/install/index.en.html)</sup>, pick your flavor and proceed.

If you're having an issue accessing Tor due to censorship or other issues, you can try using Tor Bridges by following this Tails tutorial: <https://tails.boum.org/doc/anonymous_internet/tor/index.en.html> <sup>[[Archive.org]](https://web.archive.org/web/https://tails.boum.org/doc/anonymous_internet/tor/index.en.html)</sup> and find more information about these on Tor Documentation <https://2019.www.torproject.org/docs/bridges> <sup>[[Archive.org]](https://web.archive.org/web/https://2019.www.torproject.org/docs/bridges)</sup>

**If you think using Tor alone is dangerous/suspicious, see [What about when Tor and VPNs aren't possible?](#tor-vpn-not-possible)**

### Tor Browser settings on Tails { #tails-tor-settings }

When using Tor Browser, you should click the little shield Icon (upper right, next to the Address bar) and select your Security level (see <https://tb-manual.torproject.org/security-settings/> <sup>[[Archive.org]](https://web.archive.org/web/https://tb-manual.torproject.org/security-settings/)</sup> for details). Basically, there are three.

- Standard (the default):

    - All features are enabled (including JavaScript)

- Safer:

    - JavaScript is disabled on non-HTTPS websites

    - Some fonts and symbols are disabled

    - Any media playback is "click to play" (disabled by default)

- Safest:

    - Javascript is disabled everywhere

    - Some fonts and symbols are disabled

    - Any media playback is "click to play" (disabled by default)

We would recommend the "Safer" level for most cases. The Safest level should be enabled if you think you are accessing suspicious or dangerous websites or if you are extra paranoid. The Safest mode will also most likely break many websites that rely actively on JavaScript.

If you are extra paranoid, use the "Safest" level by default and consider downgrading to Safer is the website is unusable because of Javascript blocking.

Lastly, while using Tor Browser on Tails on the "Safer" level, please consider [Additional browser precautions with JavaScript enabled](#browser-precautions-js).

Когда вы закончите и у вас на ноутбуке будет работающий Tails, перейдите к шагу [Создание анонимных онлайн-удостоверений] (#creating-identities) гораздо дальше в этом руководстве или, если вам нужна настойчивость и правдоподобное отрицание, перейдите к следующему разделу.

### Persistent Plausible Deniability using Whonix & Tails { #whonix-tails-deniability }

Рассмотрите возможность проверки проекта <https://github.com/aforensics/HiddenVM> <sup>[[Archive.org]](https://web.archive.org/web/https://github.com/aforensics/HiddenVM)</sup> для Tails.

This project is a clever idea of a one-click self-contained VM solution that you could store on an encrypted disk using plausible deniability[^311] (see [The Whonix route](#whonix-route) first chapters and also for some explanations about Plausible deniability, as well as the [How to securely delete specific files/folders/data on your HDD/SSD and Thumb drives:] section at the end of this guide for more understanding).

This would allow the creation of a hybrid system mixing Tails with the Virtualization options of the Whonix route in this guide.

![image19](../media/image19.png)

**Note: See** [Pick your connectivity method](#whonix-connectivity) **in the Whonix Route for more explanations about Stream Isolation**

In short:

- You could run non-persistent Tails from one USB key (following their recommendations)

- You could store persistent VMs within a secondary container that could be encrypted normally or using the Veracrypt plausible deniability feature (these could be Whonix VMs for instance or any other).

- You do benefit from the added Tor Stream Isolation feature (see [Tor over VPN] for more info about stream isolation).

In that case, as the project outlines it, there should be no traces of any of your activities on your computer and the sensitive work could be done from VMs stored into a Hidden container that should not be easily discoverable by a soft adversary.

**This option is particularly interesting for "traveling light" and to mitigate forensics attacks while keeping persistence on your work.** You only need 2 USB keys (one with Tails and one with a Veracrypt container containing persistent Whonix). The first USB key will appear to contain just Tails and the second USB will appear to contain just random garbage but will have a decoy volume which you can show for plausible deniability.

You might also wonder if this will result in a "Tor over Tor" setup, but it will not. The Whonix VMs will be accessing the network directly through clearnet and not through Tails Onion Routing.

In the future, this could also be supported by the Whonix project themselves as explained here: [Whonix-Host](https://www.whonix.org/wiki/Whonix-Host) <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Whonix-Host)</sup> but it is not yet recommended for end-users.

Помните, что шифрование с правдоподобным отрицанием или без него не является панацеей и от него будет мало пользы в случае пыток. На самом деле, в зависимости от того, кем будет ваш противник (ваша модель угрозы), возможно, было бы разумно вообще не использовать Veracrypt (ранее TrueCrypt), как показано в этой демонстрации: <https://defuse.ca/truecrypt-plausible-deniability-useless-by-game-theory.htm> <sup>[[Archive.org]](https://web.archive.org/web/https://defuse.ca/truecrypt-plausible-deniability-useless-by-game-theory.htm)</sup>

**Правдоподобное отрицание эффективно только против мягких законных противников, которые не прибегают к физическим средствам.**

**См. <https://en.wikipedia.org/wiki/Rubber-hose_cryptanalysis>** <sup>[[Wikiless]](https://wikiless.tiekoetter.com/wiki/Rubber-hose_cryptanalysis)</sup> <sup>[[Archive.org]](https://web.archive.org/web/https://en.wikipedia.org/wiki/Rubber-hose_cryptanalysis)</sup>

ВНИМАНИЕ. Если вы планируете хранить такие скрытые виртуальные машины на внешнем SSD-накопителе, ознакомьтесь с разделами [**Рекомендации по использованию внешних SSD-накопителей**](#on-external-ssd) и [**Понимание различий между HDD и SSD**](#hdd-vs-ssd):

- **Не используйте скрытые тома на SSD-накопителях, поскольку Veracrypt не поддерживает и не рекомендует их**[^303]**.**

- **Вместо этого используйте файловые контейнеры вместо зашифрованных томов.**

- **Убедитесь, что вы знаете, как правильно очистить данные с внешнего SSD-накопителя.**

Here is my guide on how to achieve this:

**Первый запуск**

- Загрузите последнюю версию HiddenVM с сайта <https://github.com/aforensics/HiddenVM/releases> <sup>[[Archive.org]](https://web.archive.org/web/https://github.com/aforensics/HiddenVM/releases)</sup>.

– Загрузите последнюю версию Whonix XFCE с [GitHub Releases](https://github.com/Whonix/whonix-gw-ga/releases/latest) <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Download/VirtualBox/XFCE)</sup>.

**Note:** As of guide v1.2.5, Whonix has been upgraded from version 17 to 18 (Whonix 18.1.4.x). See [[Upgrading to Whonix 18]](#qubes-whonix18) for the upgrade path if you currently use Whonix 17.x.

- Prepare a USB Key/Drive with Veracrypt

- Создайте скрытый том на USB-накопителе/ключе (мы рекомендуем не менее 16 ГБ для скрытого тома)

- Во внешнем томе поместите несколько файлов-приманок.

- В скрытом томе поместите файл образа приложения HiddenVM.

    - In the Hidden Volume, place the Whonix XFCE ova file

- Загрузитесь в Tails

- Настройте раскладку клавиатуры по своему усмотрению.

- Select Additional Settings and set an administrator (root) password (needed for installing HiddenVM)

- Запустить Тейлз

- Подключитесь к безопасному Wi-Fi (это обязательный шаг для работы остальных)

- Go into Utilities and Unlock your Veracrypt (hidden) Volume (do not forget to check the hidden volume checkbox)

- Запустите образ приложения HiddenVM.

- При появлении запроса на выбор папки выберите корень скрытого тома (где находятся файлы изображений приложений Whonix OVA и HiddenVM).

- Позвольте ему сделать свое дело (Virtualbox будет установлен в Tails одним щелчком мыши).

- Когда это будет сделано, Virtualbox Manager должен автоматически запуститься.

- Import the Whonix OVA files (see [Whonix Virtual Machines](#whonix-vms))

Note, if during the import you are having issues such as "NS_ERROR_INVALID_ARG (0x80070057)", this is probably because there is not enough disk space on your Hidden volume for Whonix. Whonix themselves recommend 32GB of free space but that's probably not necessary and 10GB should be enough for a start. You can try working around this error by renaming the Whonix \*.OVA file to \*.TAR and decompressing it within Tails. When you are done with decompression, delete the OVA file and import the other files with the Import wizard. This time it might work.

**Subsequent Runs**

- Boot into Tails

- Connect to Wi-Fi

- Unlock your Hidden Volume

- Launch the HiddenVM App

- This should automatically open VirtualBox manager and show your earlier VMs from the first run

