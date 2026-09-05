### О платных услугах { #paid-services }

Если вы намерены пользоваться платными услугами, отдавайте предпочтение тем, которые принимают наличные или Monero: так вы сможете платить напрямую, безопасно и анонимно.

Если нужная вам услуга не принимает такие платежи, но принимает Bitcoin (BTC), обратитесь к следующему приложению: [Анонимная оплата в интернете BTC (или другой криптовалютой)](#anonymous-crypto-payments).

В этом разделе приведён обзор действующих требований некоторых платформ:

- **Для лучшей защиты приватности рассмотрите рекомендованные инструменты на <https://privacyguides.org>** <sup>[[Archive.org]](https://web.archive.org/web/https://privacyguides.org)</sup> **вместо привычных массовых сервисов.**

- **Также рассмотрите рекомендованные инструменты из <https://www.whonix.org/wiki/Documentation>** <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Documentation)</sup> **вместо распространённых решений, например почтовых провайдеров: <https://www.whonix.org/wiki/E-Mail#Anonymity_Friendly_Email_Provider_List>** <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/E-Mail#Anonymity_Friendly_Email_Provider_List)</sup>

**Приведённый ниже обзор касается не практик конфиденциальности этих платформ, а только требований при регистрации учётной записи. Если вам нужны инструменты и платформы, учитывающие приватность, посетите <https://privacyguides.org>** <sup>[[Archive.org]](https://web.archive.org/web/https://privacyguides.org/)</sup>**.**

Условные обозначения:

- «Неясно»: недостаточно сведений либо они противоречивы.

- «Возможно»: это происходило в меньшинстве тестов.

- «Вероятно»: это происходило в большинстве тестов.

- «Да» или «Нет»: это либо происходило, либо систематически не происходило ни в одном из тестов.

- «Легко»: в целом всё прошло просто, с минимальными препятствиями или без них.

- «Средне»: есть некоторые препятствия, но задача выполнима без чрезмерных затруднений.

- «Сложно»: процесс сопряжён с множеством серьёзных препятствий.

- «Н/Д»: неприменимо, поскольку это невозможно было проверить в рамках данного руководства.

- «Косвенно»: требование предъявляется не напрямую, а через стороннюю систему (например, финансовый KYC).

- **Важная информация приведена в разделе [Система настоящих имён](#real-name-system). Подробности — ниже.**

**Ниже перечислены «проблемные сервисы». Если сервиса в списке нет, это означает, что с ним не выявлено никаких проблем (как, например, с Briar).**

**Amazon**

- Это нарушает их условия использования? Нет, но фактически да <https://www.amazon.com/gp/help/customer/display.html?nodeId=202140280> <sup>[[Archive.org]](https://web.archive.org/web/https://www.amazon.com/gp/help/customer/display.html?nodeId=202140280)</sup>

"1. Amazon Services, Amazon Software

A. Use of Amazon Services on a Product. To use certain Amazon Services on a Product, you must have your own Amazon.com account, be logged in to your account on the Product, **and have a valid payment method associated with your account.** "

Хотя формально настоящее имя не требуется, необходим действительный способ оплаты. К сожалению, «наличные» или «Monero» в качестве способа оплаты не принимаются. Поэтому сервис опирается на финансовый KYC, где политика настоящего имени практически повсеместно обязательна.

- Потребуют ли номер телефона? Да, но см. ниже.

- Можно ли создать учётную запись через Tor? Да, но см. ниже.

Из-за требования действительного способа оплаты мы не могли это протестировать. Хотя это, по-видимому, не нарушает условий Amazon, в рамках данного руководства это невозможно, если только вам не удастся анонимно получить платёжный инструмент с KYC, что, насколько мне известно, практически невозможно или чрезвычайно сложно.

Таким образом, насколько мне известно, создать анонимную учётную запись Amazon невозможно.

**Apple**

- Is this against their ToS? Yes <https://www.apple.com/legal/internet-services/icloud/en/terms.html> <sup>[[Archive.org]](https://web.archive.org/web/https://www.apple.com/legal/internet-services/icloud/en/terms.html)</sup>

"IV. Your Use of the Service

A. Your Account

In order to use the Service, you must enter your Apple ID and password to authenticate your Account**. You agree to provide accurate and complete information when you register with, and as you use, the Service ("Service Registration Data"), and you agree to update your Service Registration Data to keep it accurate and complete".**

- Will they require a phone number? Yes

- Can you create accounts through Tor? Yes

Note that this account will not allow you to set up an Apple mail account. For that, you will need an Apple device.

**Binance**

- Is this against their ToS? Yes <https://www.binance.com/en/terms> <sup>[[Archive.org]](https://web.archive.org/web/https://www.binance.com/en/terms)</sup>

- Will they require a phone number? No, they do require an e-mail

- Can you create accounts through Tor? No

**Discord**

- Is this against their ToS? No <https://discord.com/terms> <sup>[[Archive.org]](https://web.archive.org/web/https://discord.com/terms)</sup>

- Will they require a phone number? No, but they do require an e-mail

- Can you create accounts through Tor? We had no issues with that so far using the Desktop Client

You might encounter more issues using the Web Client (Captchas). Especially with Tor Browser.

I suggest using the Discord Client app on a VM through Tor or ideally through VPN/Proxy over Tor to mitigate such issues.

**Element**

- Is this against their ToS? No <https://element.io/terms-of-service> <sup>[[Archive.org]](https://web.archive.org/web/https://element.io/terms-of-service)</sup>

- Will they require a phone number? No, they do not even require an e-mail

- Can you create accounts through Tor? Yes

Expect some Captchas during account creation on some homeservers.

**Facebook**

- Is this against their ToS? Yes <https://www.facebook.com/terms.php> <sup>[[Archive.org]](https://web.archive.org/web/https://www.facebook.com/terms.php)</sup>

"1. Who can use Facebook

When people stand behind their opinions and actions, our community is safer and more accountable. For this reason, you must:

- Use the same name that you use in everyday life.

- Provide accurate information about yourself.

- Will they require a phone number? Yes, and probably more later

- Can you create accounts through Tor? Yes, but it is very difficult and their onion address[^398] will not help. In most cases, you'll just have a random error at sign-up and your account suspended after sign-in."

But this clause of their ToS is illegal in Germany (see [Requirements](#requirements-limitations)).

Facebook is one of the most aggressive platforms with identity verification and is pushing hard their "real name policy". It is why this guide is only advised to German residents.

Over our tests tho we were able to pinpoint a few tips:

- It will be easier if you have an Instagram account first.

- Signing up through Tor is almost impossible (even using their .onion address which is a joke) and will only succeed if you are " very lucky" (I assume if you are using an exit node that is not yet known by Facebook verification systems). In most cases, it will not allow registration at all and will just fail with "An error has occurred during registration".

- Signing up through VPNs is more likely to succeed but might still result in the same error. So, you must be ready for a lot of trial and error here.

- Signing up through a Self-Hosted VPN/Proxy is your best bet but make sure your profile/identity matches the IP geolocation.

- My earlier entry in the guide about the Orwellian quote from Animal Farm is in full effect on Facebook. You will experience huge variation in acceptance depending on age/sex/ethnicity/nationality/... This is where you will have far fewer issues if you are making an account of a Young European Caucasian Female. You will almost certainly fail if you try making a Middle-Aged Male where my other accounts are still unsuspended/unbanned to this day.

- Logging-in (after you sign-up) however works fine with VPN and Tor but might still trigger an account suspension for violating Community Guidelines or Terms of Services (despite you not using the account at all for anything else than signing-up/logging-in). Ideally, you should log-in back with the same IP from a self-hosted VPN/Proxy.

I also suspect strongly based on my test that the following points have an impact on your likelihood of being suspended over time:

- Not having friends

- Not having interests and an "organic activity"

- Not being in the contacts of any other user

- Not being on other platforms (such as Instagram/WhatsApp)

- Restricting your profile privacy settings too soon after signing-up

If your account gets suspended, you will need to appeal the decision through a quite simple form that will require you to submit a "proof of ID". However, that proof of ID verification system is more lenient than LinkedIn and will allow you to send various documents which require far less Photoshop skills.

It is also possible that they ask you to take a selfie video or picture-making certain gestures to prove your identity. If that is the case, we are afraid it is a dead-end for now unless you use a deepfake face swapping technique.

If you do file an appeal, you will have to wait for Facebook to review it (I do not know whether this is automatic or human) and you will have to wait and hope for them to unsuspend your account.

**GitHub**

- Is this against their ToS? No <https://docs.github.com/en/free-pro-team@latest/github/site-policy/github-terms-of-service> <sup>[[Archive.org]](https://web.archive.org/web/https://docs.github.com/en/free-pro-team@latest/github/site-policy/github-terms-of-service)</sup>

- Will they require a phone number? Nope, all good

- Can you create accounts through Tor? Yes, but expect some captchas

GitHub is straightforward and requires no phone number.

Be sure to go into Settings > E-Mail and make your e-mail private as well as block any push that would reveal your e-mail.

**GitLab**

- Is this against their ToS? No <https://about.gitlab.com/handbook/legal/subscription-agreement/> <sup>[[Archive.org]](https://web.archive.org/web/https://about.gitlab.com/handbook/legal/subscription-agreement/)</sup>

- Will they require a phone number? Nope, all good

- Can you create accounts through Tor? Yes, but expect captchas

GitLab is straightforward and requires no phone number.

**Google**

- Is this against their ToS? No <https://policies.google.com/terms> <sup>[[Archive.org]](https://web.archive.org/web/https://policies.google.com/terms)</sup>

- Will they require a phone number? Yes, they will. There is no escape here.

- Can you create accounts through Tor? Yes, but expect some captchas and your phone number will be required

Proton is good ... but to appear less suspicious, it is simply better to also have a mainstream Google Mail account.

As Proton, Google will also most likely require a phone number during sign-up as part of their verification process. However contrary to Proton, Google will store that phone number during the sign-up process and will also limit the number of accounts that can be created during the sign-up[^399]'[^400].

From my experience during my research, this count is limited to three accounts/phone numbers. If you are unlucky with your number (if it was previously used by another mobile user), it might be less.

You should therefore use again your online phone number OR your burner phone and pre-paid SIM card to create the account. Do not forget to use the identity details you made up earlier (birthdate). When the account is created, please do take some time to do the following:

- **(Trick)** Log into Google Mail on desktop and go into the Gmail Quick Settings > See all Setting > Forwarding and POP/IMAP > Add a forwarding address > Verify (using Proton) > Go back to Gmail and set the forwarding to forward and delete Google copy > Save. This step will allow you to check your Google Mail using Proton instead and will allow you to avoid triggering Google Security checks by Logging in from various VPN/Tor exit IP addresses in the future while storing your sensitive e-mail at Proton instead. This trick will allow you to receive all the e-mails from your Gmail addresses on your Proton (or other) address without needing to login into your Google accounts (reducing risks of it being suspended, especially if you use Tor).

- Enable 2FA within the Google account settings. First, you will have to enable 2FA using the phone number. Then you will see the option appear to enable 2FA using an Authenticator app. Use that option and set it up with a new KeePassXC TOTP entry. When it is done, remove the phone 2FA from the Google account. This will prevent someone from using that phone number in the future (when you do not have it anymore) to recover/gain access to that account.

- Add Proton as a recovery e-mail address for the account.

- Remove the phone number from the account details as a recovery option.

- Upload a Google profile picture you made earlier during the identity creation step.

- Review the Google Privacy settings to disable as much as you can:

    - Activity logging

    - YouTube

- Log out and do not touch it unless needed (as mentioned, you will use Proton to check your Gmail).

Keep in mind that there are different algorithms in place to check for weird activity. If you receive any mail (on Proton) prompting about a Google Security Warning. Click it and click the button to say, "Yes it was me". It helps.

Do not use that account for "sign-up with Google" anywhere unless necessary.

Be extremely careful if you decide to use the account for Google activities (such as Google Maps reviews or YouTube Comments) as those can easily trigger some checks (Negative reviews, Comments breaking Community Guidelines on YouTube).

If your account gets suspended [^401] (this can happen on sign-up, after signing-up or after using it in some Google services), you can still get it unsuspended by submitting[^402] an appeal/verification (which will again require your Phone number and possibly an e-mail contact with Google support with the reason). **Suspension of the account does not disable the e-mail forwarding, but the suspended account will be deleted after a while.**

After suspension, if your Google account is restored, you should be fine.

If your account gets banned, you will have no appeal and the forwarding will be disabled. Your phone number will be flagged, and you will not be able to use it to sign-up on a different account. Be careful when using those to avoid losing them. They are precious.

It is also possible that Google will require an ID check through indirect financial KYC or ID picture check if you try to access/publish mature content on their platform[^403].

**Instagram**

- Is this against their ToS? **Maybe?** We are not sure <https://help.instagram.com/581066165581870?ref=dp> <sup>[[Archive.org]](https://web.archive.org/web/https://help.instagram.com/581066165581870?ref=dp)</sup>

"**You can't impersonate others or provide inaccurate information. You do not have to disclose your identity on Instagram, but you must provide us with accurate and up-to-date information (including registration information)**. **Also, you may not impersonate someone you are not, and you can't create an account for someone else unless you have their express permission".**

This one is a bit of an Oxymoron don't you think? So, we are not sure whether it is allowed or not.

- Will they require a phone number? Maybe but less likely over VPN and very likely over Tor

- Can you create accounts through Tor? Yes, but expect some captchas and your phone number will be required

It is also possible that they ask you to take a selfie video or picture-making certain gestures to prove your identity (within the app or through an e-mail request). If that is the case, we are afraid it is a dead-end for now.

It is no secret that Instagram is part of Facebook however it is more lenient than Facebook when it comes to user verification. It is quite unlikely you will get suspended or banned after signing up. But it could help.

For instance, we noticed that you will face fewer issues creating a Facebook account if you already have a valid Instagram account. You should always create an Instagram account before trying Facebook.

Unfortunately, there are some limitations when using the web version of Instagram. For instance, you will not be able to enable Authenticator 2FA from the web for a reason we do not know.

After sign-up, do the following:

- Upload a picture of your generated identity if you want.

- Go into your Settings

- Make the account private (initially at least)

- Do not show activity status

- Do not allow sharing

**Jami**

- Is this against their ToS? No <https://jami.net/privacy-policy/> <sup>[[Archive.org]](https://web.archive.org/web/https://jami.net/privacy-policy/)</sup>

- Will they require a phone number? No, they do not even require an e-mail

- Can you create accounts through Tor? Nope it does not work for some technical reason

**Kraken**

- Is this against their ToS? Yes <https://www.kraken.com/legal> <sup>[[Archive.org]](https://web.archive.org/web/https://www.kraken.com/legal)</sup>

- Will they require a phone number? No, they do require an e-mail

- Can you create accounts through Tor? Yes

**LinkedIn**

- Is this against their ToS? Yes <https://www.linkedin.com/legal/user-agreement> <sup>[[Archive.org]](https://web.archive.org/web/https://www.linkedin.com/legal/user-agreement)</sup>

"To use the Services, you agree that: (1) you must be the "_Minimum Age_" (described below) or older; (2) **you will only have one LinkedIn account, which must be in your real name**; and (3) you are not already restricted by LinkedIn from using the Services. **Creating an account with false information is a violation of our terms**, including accounts registered on behalf of others or persons under the age of sixteen. "

But this clause of their ToS is illegal in Germany (see [Requirements](#requirements-limitations)).

- Will they require a phone number? Yes, they will.

- Can you create accounts through Tor? Yes, but expect some captchas and your phone number will be required

LinkedIn is far less aggressive than twitter but will nonetheless require a valid e-mail (preferably again your Gmail) and a phone number in most cases (tho not always).

LinkedIn however is relying a lot on reports and user/customer moderation. You should not create a profile with an occupation inside a private corporation or a small startup company. The company employees are monitoring LinkedIn activity and receive notifications when new people join. They can then report your profile as fake, and your profile will then be suspended or banned pending appeal.

LinkedIn will then require you to go through a verification process that will, unfortunately, require you to send an ID proof (identity card, passport, driver's license). This ID verification is processed by a company called Jumio[^404] that specializes in ID proofing. This is most likely a dead end as this would force you to develop some strong Photoshop skills.

Instead, you are far less likely to be reported if you just stay vague (say you are a student/intern/freelance) or pretend you work for a large public institution that is too large for anyone to care or check.

As with Twitter and Google, you should do the following after signing up:

- Disable ads

- Disable notifications

- Disable lookup by phone/e-mail

- Upload a picture of your identity

**MailFence**

- Is this against their ToS? No

- Will they require a phone number? No, but they require an e-mail

- Can you create accounts through Tor? Maybe. From my tests, the signing-up verification e-mails are not sent when using Tor to sign-up. No issues however when using a VPN over Tor or a Proxy over Tor.

**Medium**

- Is this against their ToS? No, unless it is about crypto <https://policy.medium.com/medium-terms-of-service-9db0094a1e0f> <sup>[[Archive.org]](https://web.archive.org/web/https://policy.medium.com/medium-terms-of-service-9db0094a1e0f)</sup>

- Will they require a phone number? No, but they require an e-mail

- Can you create accounts through Tor? No issues with that so far

Signing-in does require an e-mail every time.

**Microsoft**

- Is this against their ToS? Yes <https://www.microsoft.com/en/servicesagreement/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.microsoft.com/en/servicesagreement/)</sup>

"i. Creating an Account. You can create a Microsoft account by signing up online. **You agree not to use any false, inaccurate, or misleading information when signing up for your Microsoft account".**

But this clause of their ToS is illegal in Germany (see [Requirements](#requirements-limitations)).

- Will they require a phone number? Likely but not always. Depending on your luck with your Tor exit node, they may only require e-mail verification. If you use a VPN over Tor, they will likely only ask for an e-mail.

- Can you create accounts through Tor? Yes, you can but expect captchas, at least e-mail verification, **and likely phone verification.**

So yes, it is still possible to create an MS account without a phone number and using Tor or VPN, but you might have to cycle through a few exit nodes to achieve this.

After signing up you should set up 2FA authentication within the security options and using KeePassXC TOTP.

**OnlyFans**

- Is this against their ToS? No, it looks fine <https://onlyfans.com/terms> <sup>[[Archive.org]](https://web.archive.org/web/https://onlyfans.com/terms)</sup>

- Will they require a phone number? No, they do require an e-mail

- Can you create accounts through Tor? Yes, you can

Unfortunately, you will be extremely limited with that account and to do anything you will need dot complete their verification process which requires a KYC type financial transaction check. So, not very useful.

**Proton**

- Is this against their ToS? No <https://proton.me/legal/terms> <sup>[[Archive.org]](https://web.archive.org/web/https://proton.me/legal/terms)</sup>

- Will they require a phone number? Maybe. This depends on the IP you are coming from. If you come from Tor, it is likely. From a VPN, it is less likely.

- Can you create accounts through Tor? Yes, but highly likely that a phone number will be required when only an e-mail or a captcha will be required over a VPN. They even have a ".onion" address at <http://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion/>.

You obviously need an e-mail for your online identity and disposable e-mails are pretty much banned everywhere.

Proton is a free e-mail provider based in Switzerland that advocates security and privacy.

They are recommended by Privacyguides.org[^405]. Their only apparent issue is that they do require (in most cases) a phone number or another e-mail address for registration (when you try to register from a VPN or Tor at least).

They claim they do not store/link the phone/e-mail associated with the registration but only store a hash that is not linked to the account[^406]. If their claim is true and the hash is not linked to your account, and that you followed my guide about the phone number, you should be reasonably safe from tracking.

This e-mail account can be used for creating a Google/Gmail account.

**Reddit**

- Is this against their ToS? No <https://www.redditinc.com/policies> <sup>[[Archive.org]](https://web.archive.org/web/https://www.redditinc.com/policies)</sup>

- Will they require a phone number? No, they will not.

- Can you create accounts through Tor? Yes

Reddit is simple. All you need to register is a valid username and a password. Normally they do not even require an e-mail (you can skip the e-mail when registering, leaving it blank).

No issues whatsoever signing up over Tor or VPN besides the occasional Captchas.

Consider reading this reddit post: <https://old.reddit.com/r/ShadowBan/comments/8a2gpk/an_unofficial_guide_on_how_to_avoid_being/> <sup>[[Archive.org]](https://web.archive.org/web/https://old.reddit.com/r/ShadowBan/comments/8a2gpk/an_unofficial_guide_on_how_to_avoid_being/)</sup>

**Slashdot**

- Is this against their ToS? Yes <https://slashdotmedia.com/terms-of-use/> <sup>[[Archive.org]](https://web.archive.org/web/https://slashdotmedia.com/terms-of-use/)</sup>

"8. Registration; Use of Secure Areas and Passwords

Some areas of the Sites may require you to register with us. When and if you register, you agree to (a) provide accurate, current, and complete information about yourself as prompted by our registration form (including your e-mail address) and (b) to maintain and update your information (including your e-mail address) to keep it accurate, current, and complete. You acknowledge that should any information provided by you be found to be untrue, inaccurate, not current, or incomplete, we reserve the right to terminate this Agreement with you and your current or future use of the Sites (or any portion thereof)".

- Will they require a phone number? No

- Can you create accounts through Tor? Yes

**Telegram**

- Is this against their ToS? No <https://telegram.org/tos> <sup>[[Archive.org]](https://web.archive.org/web/https://telegram.org/tos)</sup>

- Will they require a phone number? Yes unfortunately

- Can you create accounts through Tor? Yes, but sometimes you randomly get banned without any reason

Telegram is quite straightforward, and you can download their portable Windows app to sign-up and log in.

It will require a phone number (that can only be used once) and nothing else.

In most cases, we had no issues whether it was over Tor or VPN, but we had a few cases where our telegram account was just banned for violating terms of services (not sure which one?). This again despite not using them for anything.

They provide an appeal process through e-mail, but we had no success with getting any answer.

Their appeal process is just sending an e-mail to <recover@telegram.org> <sup>[[Archive.org]](https://web.archive.org/web/mailto:recover@telegram.org)</sup> stating your phone number and issue and hope they answer.

After signing up you should do the following:

- Go into Edit profile

- Set a Username

- Go into Settings (Desktop App)

- Set the Phone Number visibility to Nobody

- Set Last Seen & Online to Nobody

- Set Forwarded Messages to Nobody

- Set Profile photos to Contacts

- Set Calls to Contacts

- Set Group & Channels to Contacts

**Tutanota**

- Is this against their ToS? No <https://tutanota.com/terms/> <sup>[[Archive.org]](https://web.archive.org/web/https://tutanota.com/terms/)</sup>

- Will they require a phone number? No, but they do require an e-mail.

- Can you create accounts through Tor? Not really, almost all Tor Exit nodes are banned AFAIK

**Twitter**

- Is this against their ToS? No <https://twitter.com/en/tos>

- Will they require a phone number? Extremely likely, possibly now a requirement in all cases.

- Can you create accounts through Tor? Yes, but expect some captchas and your phone number will be required after a while.

Twitter is extremely aggressive in preventing anonymity on its network. You should sign-up using e-mail and password (not phone) and not using "Sign-in with Google". Use your Gmail as the e-mail address.

More than likely, your account will be suspended immediately during the sign-up process and will require you to complete a series of automated tests to unlock. This will include a series of captchas, confirmation of your e-mail and Twitter handle, or other information. In some cases, it will also require your phone number.

In some cases, despite you selecting a text verification, the Twitter verification system will call the phone no matter what. In that case, you will have to pick up and hear the verification code. We suspect this is another method of preventing automated systems and malicious companies or entities from selling text receiving services over the internet.

Twitter will store all this information and link it to your account including your IP, e-mail, and phone number. You will not be able that phone number to create a different account.

Once the account is restored, you should take some time to do the following:

- Upload the identity profile picture.

- Enable 2FA from the security settings using a new KeePassXC TOTP entry, save the security codes in KeePassXC as well.

- Disable Photo tagging

- Disable E-mail lookup

- Disable Phone lookup

- Disable all personalized advertising settings

- Disable geolocation of tweets

- **Caution:** Remove the phone number from the account (at your own risk, this often leads to suspension of the account)

- Follow some people based

- Log out and leave it be.

After about a week, you should check Twitter again and the chances are quite high that it will be suspended again for "suspicious activity" or "violating community guidelines" despite you not using it at all (not even a single tweet/follow/like/retweet or DM) but this time by another system. We call this the "Double-tap".

This time you will need to submit an appeal using a form[^407], provide a good reason and wait for the appeal to be processed by Twitter. During that process, you may receive an e-mail (on Proton) asking you to reply to a customer service ticket to prove that you do have access to your e-mail and that it is you. This will be directed toward your Gmail address but will arrive on your Proton.

Do not reply from Proton as this will raise suspicions, you must sign in to Gmail (unfortunately) and compose a new mail from there copy-pasting the E-Mail, Subject, and Content from Proton. As well as a reply confirming you have access to that e-mail.

After a few days, your account should get unsuspended "for good". No issues after that but keep in mind they can still ban your account for any reason if you violate the community guidelines. The phone number and e-mail will then be flagged, and you will have no other option but to get a new identity with a new number to sign-up again. Do not use this account for trolling.

**Twitch**

- Is this against their ToS? No <https://www.twitch.tv/p/en/legal/terms-of-service/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.twitch.tv/p/en/legal/terms-of-service/)</sup>

- Will they require a phone number? No, but they do require an e-mail.

- Can you create accounts through Tor? Yes

Note that you will not be able to enable 2FA on Twitch using only e-mail. This feature requires a phone number to enable.

**WhatsApp**

- Is this against their ToS? **Yes** <https://www.whatsapp.com/legal/updates/terms-of-service-eea> <sup>[[Archive.org]](https://web.archive.org/web/https://www.whatsapp.com/legal/updates/terms-of-service-eea)</sup>

"**Registration**. You must register for our Services **using accurate information**, provide your current mobile phone number, and, if you change it, update your mobile phone number using our in-app change number feature. You agree to receive text messages and phone calls (from us or our third-party providers) with codes to register for our Services".

- Will they require a phone number? Yes, they do.

- Can you create accounts through Tor? No issues with that so far.

**4chan**

- Is this against their ToS? No

- Will they require a phone number? No, they will not.

- Can you post there with Tor or VPN? Not likely.

4chan is 4chan ... This guide will not explain 4chan to you. They block Tor exit nodes and known VPN IP ranges.

You are going to have to find a separate way to post there using at least seven proxies[^408] that are not known by 4chan blocking system (hint: Anonymous VPS using Monero is probably your best option).

![image40](../media/image40.png)

**Crypto Wallets**

Use any crypto wallet app within the Windows Virtual Machine. But be careful not to transfer anything toward an Exchange or a known Wallet. Crypto is in most cases NOT anonymous and can be traced back to you when you buy/sell any (remember the [Your Crypto Transactions](#crypto-transactions) section).

**If you really want to use Crypto, use Monero which is the only one with reasonable privacy/anonymity.**

Ideally, you should find a way to buy/sell crypto with cash from an unknown person.

**What about those mobile-only apps (WhatsApp/Signal)**

There are only three ways of securely using those anonymously (that we would recommend). Using a VPN on your phone is not one of those ways. All of those are, unfortunately, "tedious" to say the least.

- Use an Android Emulator within the Windows VM and run the App through your multi-layer of Tor/VPN. The drawback is that such emulators are usually quite resource-hungry and will slow down your VM and use more battery. Here is also an (outdated) guide on this matter: <https://www.bellingcat.com/resources/how-tos/2018/08/23/creating-android-open-source-research-device-pc/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.bellingcat.com/resources/how-tos/2018/08/23/creating-android-open-source-research-device-pc/)</sup>. As for myself, we will recommend the use of:

    - Android-x86 on Virtualbox (see <https://www.android-x86.org/documentation/virtualbox.html> <sup>[[Archive.org]](https://web.archive.org/web/https://www.android-x86.org/documentation/virtualbox.html)</sup>) that you can also set up easily.

    - AnBox (<https://anbox.io> <sup>[[Archive.org]](https://web.archive.org/web/https://anbox.io/)</sup>) that you can also set up rather easily including on the Whonix Workstation, see <https://www.whonix.org/wiki/Anbox> <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Anbox)</sup>

- **Not recommended:** Using a non-official app (such as Wassapp for WhatsApp) to connect from the Windows VM to the app. Use at your own risk as you could get banned for violating the terms of services by using a non-official App.

- **Not recommended and most complicated:** Have a burner Smartphone that you will connect to the VM layered network through Tethering/Sharing of the connection through Wi-Fi. We will not detail this here, but it is an option.

There is no way to reliably set a decent multi-layered connectivity approach easily on an Android phone (it is not even possible on IOS as far as we know). By reliable, we mean being sure that the smartphone will not leak anything such as geolocation or anything else from booting up to shutting down.

**Anything else**

You should use the same logic and security for any other platform.

It should work in most cases with most platforms. **The hardest platform to use with full anonymity is Facebook.**

This will obviously not work with banks and most financial platforms (such as PayPal or Crypto Exchanges) requiring actual real official and existing identification. This guide will not help you there as this would be illegal in most places.

### How to Chat & Share Files Anonymously { #anonymous-chat-files }

There are plenty of messaging apps everywhere. Some have excellent UI and UX and terrible Security/Privacy. Some have excellent Security/Privacy but terrible UI and UX. It is not easy to pick the ones that you should use for sensitive activities. So, this section will help you do that.

Before going further, there are also some key basic concepts you should understand:

#### E2E Encryption { #on-e2e-encryption }

End-to-end Encryption[^409] (aka e2ee) is a rather simple concept. It just means only you and your destination know each-others public encryption keys and no one in between that would be eavesdropping would be able to decrypt the communication.

However, the term is often used differently depending on the provider:

- Some providers will claim e2ee but forget to mention what is covered by their protocols. For instance, is metadata also protected within their e2ee protocol? Or is it just the content of the messages?

- Some providers do provide e2ee but only as an opt-in option (disabled by default).

- Some providers do offer e2ee with 1 to 1 messaging but not with group messaging.

- Some providers will claim the use of e2ee, but their proprietary apps are closed source where no one can verify the claim and the strength of the encryption used.

For these reasons, it is always important to check the claims of various apps. Open-Source apps should always be preferred to verify what kind of encryption they are using and if their claims are true. If not open source, such apps should have an openly available independent (made by a reputable third party) report confirming their claims.

#### Roll your own crypto { #roll-your-own-crypto }

See the [Bad Cryptography](#on-bad-cryptography) section at the start of this guide.

**Always be cautious of apps rolling their own crypto until it has been reviewed by many in the crypto community (or even better published and peer-reviewed academically)**. Again, this is harder to verify with closed-source proprietary apps.

It is not that rolling your own crypto is bad in essence, it is that good cryptography needs real peer-reviewing, auditing, testing... And since you are probably not a cryptanalyst (and we are not either), chances are high we are not competent to assess the cryptography of some apps.

#### Forward Secrecy { #forward-secrecy }

Forward Secrecy[^410] (FS aka PFS for Perfect Forward Secrecy) is a property of the key agreement protocol of some of those messaging apps and is a companion feature of e2ee. This happens before you establish communication with the destination. The "Forward" refers to the future in time and means that every time you establish a new e2ee communication, a new set of keys will be generated for that specific session. The goal of forward secrecy is to maintain the secrecy of past communications (sessions) even if the current one is compromised. If an adversary manages to get hold of your current e2ee keys, that adversary will then be limited to the content of the single session and will not be able to easily decrypt past ones.

This has some user experience drawbacks like for instance, a new device could not be able to conveniently access the remotely stored chat history without additional steps.

**So, in short, Forward Secrecy protects past sessions against future compromises of keys or passwords.**

More on this topic on this YouTube video: <https://www.youtube.com/watch?v=zSQtyW_ywZc> <sup>[[Invidious]](https://yewtu.be/watch?v=zSQtyW_ywZc)</sup>

Some providers and apps claiming to offer e2ee do not offer FS/PFS sometimes for usability reasons (group messaging for instance is more complex with PFS). It is therefore important to prefer open-source apps providing forward secrecy to those that do not.

#### Zero-Access Encryption at rest { #zero-access-encryption }

Zero-Access Encryption[^411] at rest is used when you store data at some provider (let us say your chat history or chat backups) but this history or backup is encrypted on your side and cannot be read or decrypted by the provider hosting it.

Zero-Access encryption is an added feature/companion to e2ee but is applied mainly to data at rest and not communications.

Examples of this issue would be iMessage and WhatsApp, see the [Your Cloud Backup & Sync Services](#cloud-backups) at the start of this guide.

So again, it is best to prefer Apps/Providers that do offer Zero-Access Encryption at rest and cannot read/access any of your data/metadata even at rest and not only limited to communications.

Such a feature would have prevented important hacks such as the Cambridge Analytica scandal[^412] if it were implemented.

#### Metadata Protection { #metadata-protection }

Remember the [Your Metadata](#metadata) section (including geo-location). End-to-end Encryption is one thing, but it does not necessarily protect your metadata.

For Instance, WhatsApp might not know what you are saying but they might know who you are talking to, how long and when you have been talking to someone, who else is in groups with you, and if you transferred data with them (such as large files).

End-to-end Encryption does not in itself protect an eavesdropper from harvesting your metadata.

This data can also be protected/obfuscated by some protocols to make metadata harvesting substantially harder for eavesdroppers. This is the case for instance with the Signal Protocol which does offer some added protection with features like:

- The Sealed Sender option[^413].

- The Private Contact Discovery[^414].

- The Private Group System[^415].

Other Apps like Briar or OnionShare will protect metadata by using the Tor Network as a shield and storing everything locally on-device. Nothing is stored remotely, and all communications are either direct using proximity wi-fi/Bluetooth or remotely through the Tor network.

Most apps however and especially closed-source proprietary commercial apps will collect and retain your metadata for various purposes. And such metadata alone is enough to figure out a lot of things about your communications.

Again, it is important to prefer open-source apps with privacy in mind and various methods in place to protect not only the content of communications but all the associated metadata.

#### Open-Source { #open-source }

Finally, Open-Source apps should always be preferred because they allow third parties to check actual capabilities and weaknesses vs claims of marketing departments. Open-Source does not mean the app should be free or non-commercial. It just means transparency.

<table>
<colgroup>
<col style="width: 9%" />
<col style="width: 6%" />
<col style="width: 7%" />
<col style="width: 7%" />
<col style="width: 7%" />
<col style="width: 8%" />
<col style="width: 7%" />
<col style="width: 7%" />
<col style="width: 9%" />
<col style="width: 10%" />
<col style="width: 7%" />
<col style="width: 8%" />
</colgroup>
<thead>
<tr class="header">
<th>App<sup>0</sup></th>
<th>e2ee<sup>1</sup></th>
<th>Roll Your Own Crypto</th>
<th><p>Perfect</p>
<p>Forward Secrecy</p></th>
<th>Zero-Access Encryption at-rest<sup>5</sup></th>
<th>Metadata Protection (obfuscation, encryption…)</th>
<th>Open-Source</th>
<th>Default Privacy Settings</th>
<th>Native Anonymous Sign-up (no e-mail or phone)</th>
<th>Possible through Tor</th>
<th>Privacy and Security Track Record ***</th>
<th>De-centralized</th>
<th>Additional notes</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td><p>Berty</p>
<p>(avoid)</p></td>
<td>Yes</td>
<td>No</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes <a href="#fn13" class="footnote-ref" id="fnref13" role="doc-noteref"><sup>13</sup></a></td>
<td>Good</td>
<td>Yes</td>
<td>Yes</td>
<td>Good</td>
<td>Yes (peer to peer)</td>
<td>Not sufficiently reviewed by this project, cannot recommend</td>
</tr>
<tr class="odd">
<td>Briar (preferred)</td>
<td>Yes</td>
<td>No <a href="#fn1" class="footnote-ref" id="fnref1" role="doc-noteref"><sup>1</sup></a></td>
<td>Yes</td>
<td>Yes</td>
<td>Yes (strong)</td>
<td>Yes</td>
<td>Good</td>
<td>Yes</td>
<td>Natively<sup>3</sup></td>
<td>Good</td>
<td>Yes (peer to peer)</td>
<td></td>
</tr>
<tr class="even">
<td><p>Cwtch</p>
<p>(preferred)</p></td>
<td>Yes</td>
<td>No</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes (strong)</td>
<td>Yes</td>
<td>Good</td>
<td>Yes</td>
<td>Natively</td>
<td>Good</td>
<td>Yes (peer to peer)</td>
<td></td>
</tr>
<tr class="odd">
<td><p>Discord</p>
<p>(avoid)</p></td>
<td>No</td>
<td>Closed-source<sup>7</sup></td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>Bad</td>
<td>E-Mail Required</td>
<td>Virtualization</td>
<td>Bad</td>
<td>No</td>
<td></td>
</tr>
<tr class="even">
<td>Element / Matrix.org (preferred)</td>
<td>Yes (opt-in)</td>
<td>No</td>
<td>Yes</td>
<td>Yes</td>
<td>Poor<a href="#fn2" class="footnote-ref" id="fnref2" role="doc-noteref"><sup>2</sup></a></td>
<td>Yes</td>
<td>Good</td>
<td>Yes</td>
<td>Via Proxy<sup>3</sup> or Virtualization</td>
<td>Good</td>
<td>Partial (federated servers)</td>
<td></td>
</tr>
<tr class="odd">
<td>Facebook Messenger (avoid)</td>
<td>Partial (Only 1to1 / opt-in)</td>
<td>Closed-source<sup>7</sup></td>
<td>Yes</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>Bad</td>
<td>E-Mail and Phone required</td>
<td>Virtualization</td>
<td>Bad</td>
<td>No</td>
<td></td>
</tr>
<tr class="even">
<td>OnionShare (preferred)</td>
<td>Yes</td>
<td>No</td>
<td>TBD<sup>8</sup></td>
<td>TBD<sup>8</sup></td>
<td>Yes (strong)</td>
<td>Yes</td>
<td>Good</td>
<td>Yes</td>
<td>Natively</td>
<td>Good</td>
<td>Yes (peer to peer)</td>
<td></td>
</tr>
<tr class="odd">
<td>Apple Messages (aka iMessage)</td>
<td>Yes</td>
<td>Closed-source<sup>7</sup></td>
<td>No</td>
<td>Partial</td>
<td>No</td>
<td>No</td>
<td>Good</td>
<td>Apple device Required</td>
<td>Maybe Virtualization using real Apple device ID</td>
<td>Bad</td>
<td>No</td>
<td></td>
</tr>
<tr class="even">
<td>IRC</td>
<td>Yes (OTR plugins)</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>Yes</td>
<td>Bad</td>
<td>Yes</td>
<td>Via Proxy<sup>3</sup> or Virtualization</td>
<td>Good</td>
<td>No</td>
<td></td>
</tr>
<tr class="odd">
<td><p>Jami</p>
<p>(preferred)</p></td>
<td>Yes</td>
<td>No<a href="#fn3" class="footnote-ref" id="fnref3" role="doc-noteref"><sup>3</sup></a></td>
<td>Yes</td>
<td>Yes</td>
<td>Partial</td>
<td>Yes</td>
<td>Good</td>
<td>Yes</td>
<td>Via Proxy<sup>3</sup> or Virtualization<sup>9</sup></td>
<td>Good</td>
<td>Partial</td>
<td>Tor breaks some features</td>
</tr>
<tr class="even">
<td>KakaoTalk (avoid)</td>
<td>Yes</td>
<td>Closed-source<sup>7</sup></td>
<td>No<a href="#fn4" class="footnote-ref" id="fnref4" role="doc-noteref"><sup>4</sup></a></td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>Bad</td>
<td>No (but possible)</td>
<td>Virtualization</td>
<td>Bad</td>
<td>No</td>
<td></td>
</tr>
<tr class="odd">
<td>Keybase</td>
<td>Yes</td>
<td>No</td>
<td>Partial (exploding message)</td>
<td>No</td>
<td>No</td>
<td>Yes</td>
<td>Good</td>
<td>E-Mail Required</td>
<td></td>
<td></td>
<td>No</td>
<td></td>
</tr>
<tr class="even">
<td>Kik (avoid)</td>
<td>No</td>
<td>Closed-source<sup>7</sup></td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>Bad</td>
<td>No (but possible)</td>
<td>Virtualization</td>
<td>Bad</td>
<td>No</td>
<td></td>
</tr>
<tr class="odd">
<td>Line (avoid)</td>
<td>Partial (opt-in)</td>
<td>Closed-source<sup>7</sup></td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>Bad</td>
<td>No (but possible)</td>
<td>Virtualization</td>
<td>Bad</td>
<td>No</td>
<td></td>
</tr>
<tr class="even">
<td>Pidgin with OTR (avoid)</td>
<td>Yes (OTR<a href="#fn5" class="footnote-ref" id="fnref5" role="doc-noteref"><sup>5</sup></a>)</td>
<td>No</td>
<td>Yes</td>
<td>No</td>
<td>No</td>
<td>Yes</td>
<td>Bad</td>
<td>Yes</td>
<td>Via Proxy<sup>3</sup> or Virtualization</td>
<td>Bad<a href="#fn6" class="footnote-ref" id="fnref6" role="doc-noteref"><sup>6</sup></a></td>
<td>No</td>
<td></td>
</tr>
<tr class="odd">
<td>Tox (avoid)</td>
<td>Yes</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>Yes</td>
<td>Good</td>
<td>Yes</td>
<td>Via Proxy<sup>3</sup> or Virtualization</td>
<td>Medium<a href="#fn7" class="footnote-ref" id="fnref7" role="doc-noteref"><sup>7</sup></a></td>
<td>Yes</td>
<td>Known cryptographic weaknesses<a href="#fn14" class="footnote-ref" id="fnref14" role="doc-noteref"><sup>14</sup></a></td>
</tr>
<tr class="even">
<td><p>Session</p>
<p>(Preferred only on iOS)</p></td>
<td>Yes</td>
<td>No</td>
<td>No</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Good</td>
<td>Yes</td>
<td>Via Proxy<sup>3</sup> or Virtualization<sup>10</sup></td>
<td>Good</td>
<td>Yes</td>
<td>Lacks PFS, deniability</td>
</tr>
<tr class="odd">
<td>Signal</td>
<td>Yes</td>
<td>No</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes (moderate)</td>
<td>Yes</td>
<td>Good</td>
<td>Phone Required</td>
<td>Virtualization</td>
<td>Good</td>
<td>No</td>
<td>Requires burner or anonymous VOIP number for anonymous usage</td>
</tr>
<tr class="even">
<td>Skype (avoid)</td>
<td>Partial (Only 1to1 / opt-in)</td>
<td>Closed-source<sup>7</sup></td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>Bad</td>
<td>No (but possible)</td>
<td>Virtualization</td>
<td>Bad</td>
<td>No</td>
<td></td>
</tr>
<tr class="odd">
<td>SnapChat (avoid)</td>
<td>No</td>
<td>Closed-source<sup>7</sup></td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>Bad</td>
<td>No (but possible)</td>
<td>Virtualization</td>
<td>Bad</td>
<td>No</td>
<td>Deleted/expired messages are easily recoverable<a href="#fn15" class="footnote-ref" id="fnref15" role="doc-noteref"><sup>15</sup></a>,<a href="#fn16" class="footnote-ref" id="fnref16" role="doc-noteref"><sup>16</sup></a></td>
</tr>
<tr class="even">
<td>Teams (avoid)</td>
<td>Yes</td>
<td>Closed-source<sup>7</sup></td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>Bad</td>
<td>No (but possible)</td>
<td>Virtualization</td>
<td>Bad</td>
<td>No</td>
<td></td>
</tr>
<tr class="odd">
<td>Telegram</td>
<td>Partial (Only 1to1 / opt-in)</td>
<td>Yes (MTProto<a href="#fn8" class="footnote-ref" id="fnref8" role="doc-noteref"><sup>8</sup></a>)</td>
<td>Partial (secret chats only)</td>
<td>Yes</td>
<td>No</td>
<td>Partial<sup>5</sup></td>
<td>Medium (e2ee off by default)</td>
<td>Phone Required</td>
<td>Via Proxy<sup>3</sup> or Virtualization</td>
<td>Medium<a href="#fn9" class="footnote-ref" id="fnref9" role="doc-noteref"><sup>9</sup></a></td>
<td>No</td>
<td></td>
</tr>
<tr class="even">
<td>Viber (avoid)</td>
<td>Partial (Only 1to1)</td>
<td>Closed-source<sup>7</sup></td>
<td>Yes</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>Bad</td>
<td>No (but possible)</td>
<td>Virtualization</td>
<td>Bad</td>
<td>No</td>
<td></td>
</tr>
<tr class="odd">
<td>WeChat (avoid)</td>
<td>No</td>
<td>Closed-source<sup>7</sup></td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>Bad</td>
<td>No</td>
<td>Virtualization</td>
<td>Bad</td>
<td>No</td>
<td></td>
</tr>
<tr class="even">
<td>WhatsApp (avoid)</td>
<td>Yes</td>
<td>Closed-source<sup>7</sup></td>
<td>Yes</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>Bad</td>
<td>Phone Required</td>
<td>Virtualization</td>
<td>Bad</td>
<td>No</td>
<td></td>
</tr>
<tr class="odd">
<td>Wickr Me</td>
<td>Partial (Only 1to1)</td>
<td>No</td>
<td>Yes</td>
<td>No</td>
<td>Yes (moderate)</td>
<td>No</td>
<td>Good</td>
<td>Yes</td>
<td>Virtualization</td>
<td>Good</td>
<td>No</td>
<td></td>
</tr>
<tr class="even">
<td>Gajim (XMPP) (preferred)</td>
<td>Yes</td>
<td>No</td>
<td>Yes</td>
<td>No</td>
<td>No</td>
<td>Yes</td>
<td>Good</td>
<td>Yes</td>
<td>Via Proxy<sup>3</sup> or Virtualization</td>
<td>Good</td>
<td>Partial</td>
<td></td>
</tr>
<tr class="odd">
<td>Zoom (avoid<a href="#fn10" class="footnote-ref" id="fnref10" role="doc-noteref"><sup>10</sup></a>)</td>
<td>Disputed<a href="#fn11" class="footnote-ref" id="fnref11" role="doc-noteref"><sup>11</sup></a></td>
<td>No</td>
<td>TBD<sup>8</sup></td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>Bad</td>
<td>E-Mail Required</td>
<td>Virtualization</td>
<td>Bad<a href="#fn12" class="footnote-ref" id="fnref12" role="doc-noteref"><sup>12</sup></a></td>
<td>No</td>
<td>Malware risk<a href="#fn17" class="footnote-ref" id="fnref17" role="doc-noteref"><sup>17</sup></a></td>
</tr>
<tr class="Even">
<td>Molly</td>
<td>Yes</td>
<td>No</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes (moderate)</td>
<td>Yes</td>
<td>Good</td>
<td>Phone Required</td>
<td>Virtualization</td>
<td>Good</td>
<td>No</td>
<td>Requires phone number. Security hardened fork of Signal client. Security may be delayed for up to a week</td>
</tr>
</tbody>
</table>
<section class="footnotes footnotes-end-of-document" role="doc-endnotes">
<hr />
<ol>
<li id="fn1" role="doc-endnote"><p>Briar Documentation, Bramble Transport Protocol version 4 <a href="https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md">https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md</a> <a href="https://web.archive.org/web/https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md"><sup>[Archive.org]</sup></a><a href="#fnref1" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
<li id="fn2" role="doc-endnote"><p>Serpentsec, Matrix <a href="https://web.archive.org/web/https://serpentsec.1337.cx/matrix">https://web.archive.org/web/https://serpentsec.1337.cx/matrix</a><a href="#fnref2" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
<li id="fn3" role="doc-endnote"><p>Wikipedia, GnuTLS, <a href="https://en.wikipedia.org/wiki/GnuTLS">https://en.wikipedia.org/wiki/GnuTLS</a> <a href="https://wikiless.tiekoetter.com/wiki/GnuTLS"><sup>[Wikiless]</sup></a> <a href="https://web.archive.org/web/https://en.wikipedia.org/wiki/GnuTLS"><sup>[Archive.org]</sup></a><a href="#fnref3" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
<li id="fn4" role="doc-endnote"><p>KTH ROYAL INSTITUTE OF TECHNOLOGYSCHOOL OF ELECTRICAL ENGINEERING, A Security and Privacy Audit of KakaoTalk’s End-to-End Encryption <a href="http://www.diva-portal.org/smash/get/diva2:1046438/FULLTEXT01.pdf">www.diva-portal.org/smash/get/diva2:1046438/FULLTEXT01.pdf</a> <a href="https://web.archive.org/web/http://www.diva-portal.org/smash/get/diva2:1046438/FULLTEXT01.pdf"><sup>[Archive.org]</sup></a><a href="#fnref4" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
<li id="fn5" role="doc-endnote"><p>Wikipedia, OTR <a href="https://en.wikipedia.org/wiki/Off-the-Record_Messaging">https://en.wikipedia.org/wiki/Off-the-Record_Messaging</a> <a href="https://wikiless.tiekoetter.com/wiki/Off-the-Record_Messaging"><sup>[Wikiless]</sup></a> <a href="https://web.archive.org/web/https://en.wikipedia.org/wiki/Off-the-Record_Messaging"><sup>[Archive.org]</sup></a><a href="#fnref5" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
<li id="fn6" role="doc-endnote"><p>Pidgin Security Advisories, <a href="https://www.pidgin.im/about/security/advisories/">https://www.pidgin.im/about/security/advisories/</a> <a href="https://web.archive.org/web/https://www.pidgin.im/about/security/advisories/"><sup>[Archive.org]</sup></a><a href="#fnref6" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
<li id="fn7" role="doc-endnote"><p>Whonix Forum, Tox Integration <a href="https://forums.whonix.org/t/tox-qtox-whonix-integration/1219">https://forums.whonix.org/t/tox-qtox-whonix-integration/1219</a> <a href="https://web.archive.org/web/https://forums.whonix.org/t/tox-qtox-whonix-integration/1219"><sup>[Archive.org]</sup></a><a href="#fnref7" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
<li id="fn8" role="doc-endnote"><p>Telegram Documentation, MTProto Mobile Protocol <a href="https://core.telegram.org/mtproto">https://core.telegram.org/mtproto</a> <a href="https://web.archive.org/web/https://core.telegram.org/mtproto"><sup>[Archive.org]</sup></a><a href="#fnref8" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
<li id="fn9" role="doc-endnote"><p>Wikipedia, Telegram Security Breaches, <a href="https://en.wikipedia.org/wiki/Telegram_(software)#Security_breaches">https://en.wikipedia.org/wiki/Telegram_(software)#Security_breaches</a> <a href="https://wikiless.tiekoetter.com/wiki/Telegram_(software)"><sup>[Wikiless]</sup></a> <a href="https://web.archive.org/web/https://en.wikipedia.org/wiki/Telegram_(software)#Security_breaches"><sup>[Archive.org]</sup></a><a href="#fnref9" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
<li id="fn10" role="doc-endnote"><p>TechCrunch, Maybe we shouldn’t use Zoom after all, <a href="https://techcrunch.com/2020/03/31/zoom-at-your-own-risk/">https://techcrunch.com/2020/03/31/zoom-at-your-own-risk/</a> <a href="https://web.archive.org/web/https://techcrunch.com/2020/03/31/zoom-at-your-own-risk/"><sup>[Archive.org]</sup></a><a href="#fnref10" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
<li id="fn11" role="doc-endnote"><p>The Incercept, Zoom Meetings Aren’t End-to-End Encrypted, Despite Misleading Marketing <a href="https://theintercept.com/2020/03/31/zoom-meeting-encryption/">https://theintercept.com/2020/03/31/zoom-meeting-encryption/</a> <a href="http://27m3p2uv7igmj6kvd4ql3cct5h3sdwrsajovkkndeufumzyfhlfev4qd.onion/2020/03/31/zoom-meeting-encryption/"><sup>[Tor Mirror]</sup></a> <a href="https://web.archive.org/web/https://theintercept.com/2020/03/31/zoom-meeting-encryption/"><sup>[Archive.org]</sup></a><a href="#fnref11" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
<li id="fn12" role="doc-endnote"><p>Serpentsec, Secure Messaging: Choosing a chat app <a href="https://web.archive.org/web/https://serpentsec.1337.cx/secure-messaging-choosing-a-chat-app">https://web.archive.org/web/https://serpentsec.1337.cx/secure-messaging-choosing-a-chat-app</a><a href="#fnref12" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
<li id="fn13" role="doc-endnote"><p>Berty, Development, <a href="https://berty.tech">https://berty.tech</a><a href="#fn13" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
<li id="fn14" role="doc-endnote"><p>Tox Handshake Vulnerable to KCI, <a href="https://github.com/TokTok/c-toxcore/issues/426">https://github.com/TokTok/c-toxcore/issues/426</a><a href="#fn13" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
<li id="fn15" role="doc-endnote"><p>The Guardian, Deleted Snapchat photos recovered 'within days' by forensics company, <a href="https://www.theguardian.com/technology/2013/may/09/snapchat-photos-not-deleted">https://www.theguardian.com/technology/2013/may/09/snapchat-photos-not-deleted</a><a href="#fn13" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
<li id="fn16" role="doc-endnote"><p>The Guardian, Snapchat's expired snaps are not deleted, just hidden, <a href="https://web.archive.org/web/20131115224243/https://www.theguardian.com/media-network/partner-zone-infosecurity/snapchat-photos-not-deleted-hidden">https://web.archive.org/web/20131115224243/https://www.theguardian.com/media-network/partner-zone-infosecurity/snapchat-photos-not-deleted-hidden</a><a href="#fn13" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
<li id="fn17" role="doc-endnote"><p>The Guardian, ‘Zoom is malware’: why experts worry about the video conferencing platform, <a href="https://www.theguardian.com/technology/2020/apr/02/zoom-technology-security-coronavirus-video-conferencing">https://www.theguardian.com/technology/2020/apr/02/zoom-technology-security-coronavirus-video-conferencing</a><a href="#fn13" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
</ol>
</section>

**Legend:**

1. The mention "preferred" or "avoid" refers to the use of those apps for sensitive communications. This is just my opinion, and you can make your own using the resources above and others. Remember "Trust but verify".

2. e2ee refers to "end-to-end encryption"

3. Additional steps might be needed for securing Tor Connectivity

4. Their ability and willingness to fight for privacy and not cooperate with various adversaries

5. Only the client apps are open-source, not the server-side apps

6. This means the data is fully encrypted at rest (and not only during transit) and unreadable by any third party without a key you only know (including backups)

7. Unverifiable because it is proprietary closed source.

8. To Be Determined, unknown at the time of this writing

9. Jami will require you to enable DHTProxy in their options to work and it will be limited to text only.

10. Session also uses their own Onion Routing solution called LokiNet

**Some apps like Threema and Wire were excluded from this comparison due to not being free and not accepting anonymous cash methods such as Cash/Monero.**

#### Заключение { #comms-conclusion }

**Помните: [Контрольный список перед передачей информации](#pre-sharing-checklist).**

Мы рекомендуем следующие варианты в этом порядке (их также рекомендует Privacyguides.org[^416]'[^417], за исключением Session и Cwtch):

- macOS:

    - Встроенная поддержка луковой маршрутизации Tor (**предпочтительно**):

        + OnionShare version >2.3 (<https://onionshare.org/> <sup>[[Tor Mirror]](http://lldan5gahapx5k7iafb3s4ikijc4ni7gx5iywdflkba5y2ezyg6sjgyd.onion/)</sup> <sup>[[Archive.org]](https://web.archive.org/web/https://onionshare.org/)</sup>)**

        + Cwtch (<https://cwtch.im> <sup>[[Archive.org]](https://web.archive.org/web/https://cwtch.im/)</sup> **внимание: проект находится на стадии alpha/beta**)**

    - Невстроенная поддержка Tor (для оптимальной анонимности нужны дополнительные шаги: направить трафик через Tor с помощью виртуализации или прокси):

        + Element/Matrix.org (<https://element.io/> <sup>[[Archive.org]](https://web.archive.org/web/https://element.io/)</sup>)

        + Jami (<https://jami.net/> <sup>[[Archive.org]](https://web.archive.org/web/https://jami.net/)</sup>)*

        + Gajim/XMPP (<https://gajim.org/> <sup>[[Archive.org]](https://web.archive.org/web/https://gajim.org/)</sup>)

- Windows:

    - Встроенная поддержка луковой маршрутизации Tor (**предпочтительно**):

        + OnionShare version >2.3 (<https://onionshare.org/> <sup>[[Tor Mirror]](http://lldan5gahapx5k7iafb3s4ikijc4ni7gx5iywdflkba5y2ezyg6sjgyd.onion/)</sup> <sup>[[Archive.org]](https://web.archive.org/web/https://onionshare.org/)</sup>)**

        + Cwtch (<https://cwtch.im> <sup>[[Archive.org]](https://web.archive.org/web/https://cwtch.im/)</sup> **внимание: проект находится на стадии alpha/beta**)**

    - Невстроенная поддержка Tor (для оптимальной анонимности нужны дополнительные шаги: направить трафик через Tor с помощью виртуализации или прокси):

        + Element/Matrix.org (<https://element.io/> <sup>[[Archive.org]](https://web.archive.org/web/https://element.io/)</sup>)

        + Jami (<https://jami.net/> <sup>[[Archive.org]](https://web.archive.org/web/https://jami.net/)</sup>)*

        + Gajim/XMPP (<https://gajim.org/> <sup>[[Archive.org]](https://web.archive.org/web/https://gajim.org/)</sup>)

- Linux:

    - Встроенная поддержка луковой маршрутизации Tor (**предпочтительно**):

        + Briar (<https://briarproject.org/> <sup>[[Archive.org]](https://web.archive.org/web/https://briarproject.org/)</sup>)*

        + OnionShare version >2.3 (<https://onionshare.org/> <sup>[[Tor Mirror]](http://lldan5gahapx5k7iafb3s4ikijc4ni7gx5iywdflkba5y2ezyg6sjgyd.onion/)</sup> <sup>[[Archive.org]](https://web.archive.org/web/https://onionshare.org/)</sup>)**

        + Cwtch (<https://cwtch.im> <sup>[[Archive.org]](https://web.archive.org/web/https://cwtch.im/)</sup> **внимание: проект находится на стадии alpha/beta**)**

    - Невстроенная поддержка Tor (для оптимальной анонимности нужны дополнительные шаги: направить трафик через Tor с помощью виртуализации или прокси):

        + Element/Matrix.org (<https://element.io/> <sup>[[Archive.org]](https://web.archive.org/web/https://element.io/)</sup>)

        + Jami (<https://jami.net/> <sup>[[Archive.org]](https://web.archive.org/web/https://jami.net/)</sup>)*

        + Gajim/XMPP (<https://gajim.org/> <sup>[[Archive.org]](https://web.archive.org/web/https://gajim.org/)</sup>)

- Учтите: чтобы Jami работал через Tor, в настройках Jami нужно включить локальную опцию DHTProxy. Это будет работать только для текстовых сообщений, но не для звонков и видео.)

** Учтите, что эти варианты (Briar, Cwtch и OnionShare) пока не поддерживают несколько устройств. Ваша информация хранится исключительно на устройстве/в ОС, где всё настроено. Не используйте их в непостоянной ОС, если только вам не нужен кратковременный доступ.

Есть ли безопасные варианты для мобильных устройств? **Да, но ни один из них не одобряется и не рекомендуется, кроме Briar на Android. Кроме того, помните: это руководство в целом не советует использовать смартфоны для чувствительной деятельности.**

- Android:

    - Briar (<https://briarproject.org/> <sup>[[Archive.org]](https://web.archive.org/web/https://briarproject.org/)</sup>)

    - Cwtch (<https://cwtch.im> <sup>[[Archive.org]](https://web.archive.org/web/https://cwtch.im/)</sup> **внимание: проект находится на стадии alpha/beta**)

- iOS:

    - Из-за отсутствия лучшего варианта и хотя обычно он **не рекомендуется**: Session Messenger: <https://getsession.org/> <sup>[[Archive.org]](https://web.archive.org/web/https://getsession.org/)</sup>. Почему сегодня сообщество приватности его не рекомендует? **См. [Предостережение о мессенджере Session](#session-messenger-caution), чтобы узнать, почему мы осторожно относимся к Session Messenger**.

**Учтите: в целях безопасности все варианты без встроенной поддержки Tor следует использовать поверх Tor (из Tails или гостевой ОС за шлюзом Whonix, например Whonix Workstation либо ВМ Android-x86).**

Хотя мы не рекомендуем большинство платформ обмена сообщениями по изложенным выше причинам (требования номера телефона и электронной почты), это не означает, что ими невозможно пользоваться анонимно, если вы понимаете, что делаете. Даже Facebook Messenger можно использовать анонимно, соблюдая необходимые меры из этого руководства (виртуализация за шлюзом Tor в непостоянной ОС).

Предпочтительные варианты рекомендуются благодаря их подходу к приватности, настройкам по умолчанию и криптографическим решениям, а также потому, что они позволяют удобно зарегистрироваться анонимно без многочисленных сложностей с проверкой номера телефона или электронной почты и имеют открытый исходный код. В большинстве случаев следует выбирать именно их.

Для дополнительных сравнений можно также обратиться к следующим внешним ресурсам (**мы не обязательно разделяем их мнения**):

- SecuChart, <https://bkil.gitlab.io/secuchart/> <sup>[[Archive.org]](https://web.archive.org/web/https://bkil.gitlab.io/secuchart/)</sup> <sup>[[Repository]](https://github.com/bkil/secuchart)</sup> (Maintained open-source project)
- Wikipedia, <https://en.wikipedia.org/wiki/Comparison_of_cross-platform_instant_messaging_clients> <sup>[[Wikiless]](https://wikiless.tiekoetter.com/wiki/Comparison_of_cross-platform_instant_messaging_clients)</sup> <sup>[[Archive.org]](https://web.archive.org/web/https://en.wikipedia.org/wiki/Comparison_of_cross-platform_instant_messaging_clients)</sup>
    - Wikipedia, <https://en.wikipedia.org/wiki/Comparison_of_instant_messaging_protocols> <sup>[[Wikiless]](https://wikiless.tiekoetter.com/wiki/Comparison_of_instant_messaging_protocols)</sup> <sup>[[Archive.org]](https://web.archive.org/web/https://en.wikipedia.org/wiki/Comparison_of_instant_messaging_protocols)</sup>
- Whonix Documentation, Instant Messenger Chat <https://www.whonix.org/wiki/Chat> <sup>[[Archive.org]](https://web.archive.org/web/https://www.whonix.org/wiki/Chat)</sup> (Outdated, Unmaintained but contains insightful information)

- **Устаревшие, не поддерживаемые или заброшенные ресурсы, которые планируется удалить из руководства в следующем выпуске:**

    - <del>Secure Messaging Apps <https://www.securemessagingapps.com/> <sup>[[Archive.org]](https://web.archive.org/web/https://www.securemessagingapps.com/)</sup></del>
    - <del>Proton Blog, <https://proton.me/blog/whatsapp-alternatives/> <sup>[[Archive.org]](https://web.archive.org/web/2022053117143/https://proton.me/blog/whatsapp-alternatives)</sup></del>
    - <del>SecureChart.org, <https://securechatguide.org/featuresmatrix.html> <sup>[[Archive.org]](https://web.archive.org/web/https://securechatguide.org/featuresmatrix.html)</sup></del>
    - <del>Messenger-Matrix.de at <https://www.messenger-matrix.de/messenger-matrix-en.html> <sup>[[Archive.org]](https://web.archive.org/web/https://www.messenger-matrix.de/messenger-matrix-en.html)</sup></del>

**Мы не одобряем и не рекомендуем для анонимности некоторые массовые платформы, включая широко расхваливаемый Signal, который до сих пор требует номер телефона для регистрации и связи с другими пользователями. В контексте данного руководства мы настоятельно советуем по возможности не использовать Signal. Та же рекомендация относится к популярным ответвлениям Signal, таким как Molly (<https://molly.im><sup>[[Archive.org]](https://web.archive.org/web/https://molly.im)</sup>)**

### Как публично делиться файлами { #share-files-publicly }

**Предупреждение: прежде чем публиковать что-либо, убедитесь, что из файлов удалена вся информация, которая может раскрыть вашу личность. См. [Контрольный список перед передачей информации](#pre-sharing-checklist).**

Рассмотрите следующие платформы:

- Cryptpad.fr (<https://cryptpad.fr/>): бесплатный тариф ограничен 1 ГБ в сумме; сервис рекомендован PrivacyGuides.org: <https://privacyguides.org/cloud/> <sup>[[Archive.org]](https://web.archive.org/web/https://privacyguides.org/cloud/)</sup>

- Proton Drive (<https://proton.me/drive/>): платный сервис. Требуется «Proton Unlimited» или «Mail Plus». Proton Drive использует E2EE и рекомендован PrivacyGuides.org.
    - Как и в Proton и Proton VPN, анонимно зарегистрироваться здесь непросто. При регистрации через Tor просят подтверждение либо номером телефона, либо пожертвованием.

- Filen (<https://filen.io/>): бесплатный тариф ограничен 10 ГБ в сумме.

Рассмотрите использование IPFS[^421]:

- Pinata (<https://www.pinata.cloud/>): бесплатный тариф ограничен 1 ГБ в сумме.

### Безопасное редактирование документов { #redacting-documents }

Возможно, вы захотите безопасно и анонимно самостоятельно опубликовать какую-либо информацию в виде текста, изображений, видео и т. д.

Для этого есть несколько рекомендаций:

- В идеале не следует пользоваться проприетарным ПО, таким как Adobe Photoshop или Microsoft Office.

- Вместо этого предпочтительно использовать ПО с открытым исходным кодом, например LibreOffice и Gimp.

Хотя коммерческие альтернативы богаты функциями, они также проприетарны, имеют закрытый исходный код и нередко создают следующие проблемы:

- Отправляют телеметрические данные компании.

- Добавляют в документы ненужные метаданные, а иногда и водяные знаки.

- Эти приложения платные, и утечку любых метаданных могут связать с вами, поскольку вы где-то их приобрели.

Коммерческое ПО можно использовать для создания чувствительных документов, но следует особенно тщательно проверять все параметры разных приложений — платных и бесплатных, — чтобы утечка данных не раскрыла информацию о вас.

Ниже приведена сравнительная таблица рекомендуемого и включённого ПО, составленная по разным источникам (PrivacyGuides.org, Whonix, Tails, Prism-Break.org и автор). Учтите, что рекомендации учитывают контекст этого руководства: выходить в интернет следует лишь изредка и по необходимости.

<table>
<colgroup>
<col style="width: 18%" />
<col style="width: 14%" />
<col style="width: 13%" />
<col style="width: 20%" />
<col style="width: 14%" />
<col style="width: 17%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Type</strong></th>
<th><strong>Whonix</strong></th>
<th><strong>Prism-Break.org</strong></th>
<th><strong>PrivacyGuides.org</strong></th>
<th><strong>Tails</strong></th>
<th><strong>This guide</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Offline Document Editing</td>
<td>LibreOffice</td>
<td>N/A</td>
<td>LibreOffice*</td>
<td>LibreOffice</td>
<td><p>LibreOffice,</p>
<p>Notepad++</p></td>
</tr>
<tr class="even">
<td>Online Document Editing (collaboration)</td>
<td>N/A</td>
<td>Cryptpad.fr</td>
<td><p>Cryptpad.fr,</p>
<p>Etherpad.org,</p>
<p>Privatebin.net</p></td>
<td>N/A</td>
<td><p>Cryptpad.fr,</p>
<p>Etherpad.org,</p>
<p>Privatebin.net</p></td>
</tr>
<tr class="odd">
<td>Pictures Editing</td>
<td>Flameshot (L)</td>
<td>N/A</td>
<td>N/A</td>
<td>GIMP</td>
<td>GIMP</td>
</tr>
<tr class="even">
<td>Audio Editing</td>
<td>Audacity</td>
<td>N/A</td>
<td>N/A</td>
<td>Audacity</td>
<td>Audacity</td>
</tr>
<tr class="odd">
<td>Video Editing</td>
<td>Flowblade (L)</td>
<td>N/A</td>
<td>N/A</td>
<td>N/A</td>
<td><p>Flowblade (L)</p>
<p>Olive (?)</p>
<p>OpenShot (?)</p>
<p>ShotCut (?)</p></td>
</tr>
<tr class="even">
<td>Screen Recorder</td>
<td>Vokoscreen</td>
<td>N/A</td>
<td>N/A</td>
<td>N/A</td>
<td>Vokoscreen</td>
</tr>
<tr class="odd">
<td>Media Player</td>
<td>VLC</td>
<td>N/A</td>
<td>N/A</td>
<td>VLC</td>
<td>VLC</td>
</tr>
<tr class="even">
<td>PDF Viewer</td>
<td>Ristretto (L)</td>
<td>N/A</td>
<td>N/A</td>
<td>N/A</td>
<td>Browser</td>
</tr>
<tr class="odd">
<td>PDF Redaction</td>
<td>PDF-Redact Tools (L)</td>
<td>N/A</td>
<td>N/A</td>
<td>PDF-Redact Tools (L)</td>
<td><p>LibreOffice,</p>
<p>PDF-Redact Tools (L)</p></td>
</tr>
</tbody>
</table>

**Условные обозначения:** * Не рекомендуется, но упомянуто. Н/Д = не включено либо для данного типа ПО нет рекомендации. (L) = только Linux, но, возможно, может использоваться в Windows/macOS иными способами (HomeBrew, виртуализация, Cygwin). (?) = не тестировалось, но имеет открытый исходный код и может быть рассмотрено.

**Во всех случаях мы настоятельно рекомендуем запускать такие приложения только внутри ВМ или Tails, чтобы максимально предотвратить утечки. В противном случае перед публикацией придётся тщательно очистить документы (см. [Проверка метаданных](#metadata-auditing)).**

### Передача чувствительной информации { #sensitive-communication }

Возможно, вам потребуется анонимно передать информацию какой-либо организации, например прессе.

Если это необходимо, примите ряд мер: нельзя доверять какой бы то ни было организации защиту вашей анонимности[^422]. См. [Контрольный список перед передачей информации](#pre-sharing-checklist).

Для этого мы настоятельно рекомендуем SecureDrop[^423] (<https://securedrop.org/> <sup>[[Archive.org]](https://web.archive.org/web/https://securedrop.org/)</sup>) — проект с открытым исходным кодом Фонда свободы прессы.

- Непременно ознакомьтесь с их «руководством для источников»: <https://docs.securedrop.org/en/stable/source.html> <sup>[[Archive.org]](https://web.archive.org/web/https://docs.securedrop.org/en/stable/source.html)</sup>

- В идеале следует пользоваться SecureDrop через Tor; отобранный список таких сервисов приведён здесь: <https://github.com/alecmuffett/real-world-onion-sites#securedrop> <sup>[[Archive.org]](https://web.archive.org/web/https://github.com/alecmuffett/real-world-onion-sites#securedrop)</sup>

Если SecureDrop недоступен, можно рассмотреть иные способы связи, но предпочтение следует отдавать сквозному шифрованию. **Никогда не делайте этого от своего настоящего имени: действуйте только из безопасной среды и под анонимной личностью.**

Без SecureDrop можно рассмотреть:

- Электронную почту с шифрованием GPG, если адресат где-либо опубликовал ключ GPG. Его можно поискать здесь:

    - В их подтверждённых учётных записях социальных сетей (Twitter), если ключ там указан.

    - On <https://keybase.io> (Tor address <http://keybase5wmilwokqirssclfnsqrjdsi7jdir5wy7y7iu3tanwmtp6oid.onion>)

    - В каталогах OpenPGP, например: **(будьте осторожны: это публичные каталоги, и любой может загрузить любой ключ для любого адреса электронной почты; чтобы убедиться, что ключ принадлежит адресату, сверяйте подпись с другими платформами).**

        + <https://pgp.mit.edu/>

        + <https://keyserver.ubuntu.com/>

        + <https://keys.openpgp.org>

- Любую другую платформу (даже личные сообщения Twitter), но и в этом случае шифруйте сообщение для получателя с помощью GPG.

Чего следует избегать:

- Не отправляйте физические материалы почтой: можно оставить ДНК, отпечатки пальцев или иную отслеживаемую информацию (см. [VPN за наличные (предпочтительно)](#anonymous-cash-vpn)).

- Не используйте способы, привязанные к номеру телефона, даже одноразовому, например Signal/WhatsApp/Telegram.

- Не используйте голосовую или видеосвязь.

- Не раскрывайте при обмене сообщениями никаких сведений о своей настоящей личности.

- Не встречайтесь с людьми лично, если только другого выхода совершенно нет (это крайняя мера).

Если вы намерены нарушить свою анонимность ради безопасности:

- Сначала очень тщательно оцените риски.

- Тщательно изучите законность и безопасность своего намерения, а также последствия для себя и других. Хорошо всё обдумайте.

- Возможно, прежде обратитесь к **доверенному** адвокату.

**Поддерживающие действия**

- Время от времени осторожно входите в свои учётные записи, чтобы они оставались активными.

- Регулярно проверяйте почту на уведомления о проверках безопасности и другие сообщения учётных записей.

- Регулярно проверяйте возможную компрометацию любой из своих личностей с помощью <https://haveibeenpwned.com/> <sup>[[Archive.org]](https://web.archive.org/web/https://haveibeenpwned.com/)</sup> (разумеется, из безопасной среды).

# Безопасное резервное копирование работы { #secure-backups }

**Никогда не загружайте зашифрованные файловые контейнеры с правдоподобным отрицанием (скрытыми контейнерами внутри) в большинство облачных сервисов (iCloud, Google Drive, OneDrive, Dropbox) без мер предосторожности. Большинство облачных сервисов хранят резервные копии и версии файлов; такие копии и версии зашифрованных контейнеров могут использоваться для дифференциального анализа, доказывающего существование скрытого контейнера.**

Вместо этого руководство рекомендует другие способы безопасного резервного копирования ваших данных.

