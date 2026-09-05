---
title: "Проверка"
description: "Проверьте подлинность и целостность выпусков Anonymous Planet."
hide:
  - navigation
schema:
  "@context": https://schema.org
  "@type": Organization
  "@id": https://anonymousplanet.net/
  name: Anonymous Planet
  url: https://anonymousplanet.net/verify/
  logo: ../../media/profile.png
---

<div class="hero-block">
  <div class="hero-eyebrow">Никогда не доверяйте скачанному вслепую.</div>
  <h1 class="hero-title">Проверка выпусков<span class="hero-subtitle">Подписи. Хеши. Ничему не доверяйте вслепую.</span></h1>
  <p class="hero-tagline">
    Каждый выпуск подписан GPG и снабжён хешем. Проверьте его перед чтением.
  </p>
  <div class="hero-cta-row">
    <a href="#quick-verification" class="hero-cta hero-cta--primary">Быстрая проверка</a>
    <a href="../pgp/" class="hero-cta hero-cta--secondary">Импортировать наши ключи</a>
  </div>
</div>

---

## Что мы публикуем { #artifacts }

<div class="index-grid">

  <div class="index-card">
    <h3 class="index-card__title">Руководство в PDF</h3>
    <p class="index-card__body"><code>thgtoa.pdf</code> и <code>thgtoa-dark.pdf</code> — полное руководство в светлой и тёмной теме. Единственный канонический экспорт в одном файле.</p>
    <a href="https://github.com/Anon-Planet/thgtoa/releases" class="index-card__link">Последний выпуск</a>
  </div>

  <div class="index-card">
    <h3 class="index-card__title">Отсоединённые подписи</h3>
    <p class="index-card__body">Файлы <code>.asc</code> для каждого PDF и файла хешей, подписанные ключом подписи выпусков (RSK). Проверяйте с помощью <code>gpg --verify</code>.</p>
    <a href="../pgp/" class="index-card__link">Наши ключи</a>
  </div>

  <div class="index-card">
    <h3 class="index-card__title">Файлы хешей</h3>
    <p class="index-card__body"><code>sha256sums.txt</code> и <code>b2sums.txt</code> для проверки целостности. Оба также подписаны. Проверяйте с помощью <code>sha256sum -c</code> или <code>b2sum -c</code>.</p>
    <a href="#manual-verification" class="index-card__link">Ручная проверка</a>
  </div>

</div>

---

## Быстрая проверка { #quick-verification }

### С помощью скрипта Python (рекомендуется)

```sh
# Проверить всё: хеши, подписи и при необходимости VirusTotal
python scripts/verify_pdf.py --all

# Только хеши
python scripts/verify_pdf.py --hashes

# Только подписи GPG
python scripts/verify_pdf.py --signatures

# Статус проверки VirusTotal (требует переменную окружения VT_API_KEY)
python scripts/verify_pdf.py --vt
```

---

## Ручная проверка { #manual-verification }

### 1. Импортируйте ключ

```sh
gpg --import pgp/anonymousplanet.asc
```

Прежде чем доверять ключу, сверьте отпечаток с нашей [страницей PGP](../pgp/index.md) и [выпусками GitHub](https://github.com/Anon-Planet/thgtoa/releases).

### 2. Проверьте PDF

```sh
gpg --verify export/thgtoa.pdf.asc      export/thgtoa.pdf
gpg --verify export/thgtoa-dark.pdf.asc export/thgtoa-dark.pdf
```

Ожидаемый вывод:

```text
gpg: Signature made Sun 31 May 2026 03:23:26 AM EDT
gpg:                using EDDSA key C3023DBEA3FB38C438BA1EEDCEC60AEDE8B992A2
gpg: Good signature from "Anonymous Planet Release Signing Key" [ultimate]
Primary key fingerprint: C302 3DBE A3FB 38C4 38BA  1EED CEC6 0AED E8B9 92A2
```

!!! note "О предупреждении WARNING"
    Сообщение `WARNING: This key is not certified with a trusted signature` ожидаемо. Оно означает, что другой ключ в вашей сети доверия не заверил этот ключ, а не то, что подпись недействительна.

### 3. Проверьте хеши

=== "Linux / macOS"

    ```sh
    sha256sum -c sha256sums.txt
    b2sum     -c b2sums.txt
    ```

=== "Windows (PowerShell)"

    ```powershell
    Get-FileHash -Algorithm SHA256 export\thgtoa.pdf | Select-Object Hash
    # Сравните со значением в thgtoa.pdf.sha256
    ```

### 4. VirusTotal (необязательно)

```sh
export VT_API_KEY=your_vt_api_key
python scripts/verify_pdf.py --vt
```

Или откройте напрямую URL отчётов VirusTotal, указанные в примечаниях к выпуску.

---

## Устранение неполадок { #troubleshooting }

**«Good signature», но неверный владелец?**
Убедитесь, что импортировали правильный ключ из [`pgp/`](../pgp/index.md). Проверьте, что отпечаток совпадает с RSK: `C302 3DBE A3FB 38C4 38BA  1EED CEC6 0AED E8B9 92A2`.

**Хеш не совпадает?**
Скачайте файл заново. Убедитесь, что используете правильный файл хешей для версии (светлой или тёмной). Проверьте диск на ошибки.

**GPG не установлен?**

| Платформа | Команда |
|---|---|
| Debian / Ubuntu | `sudo apt install gnupg` |
| RHEL / Fedora | `sudo dnf install gnupg2` |
| macOS | `brew install gnupg` |
| Windows | [Gpg4win](https://gpg4win.org) |
