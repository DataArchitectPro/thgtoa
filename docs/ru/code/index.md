---
title: "Вклад в содержание"
description: "Как внести вклад в Путеводитель автостопщика: сборка, подпись, выпуск и написание материалов."
hide:
  - toc
  - navigation
schema:
  "@context": https://schema.org
  "@type": Organization
  "@id": https://anonymousplanet.net/
  name: Anonymous Planet
  url: https://anonymousplanet.net/code/
  logo: ../../media/profile.png
  sameAs:
    - https://github.com/Anon-Planet
    - https://opencollective.com/anonymousplanetorg
---

<div class="hero-block">
  <div class="hero-eyebrow">Открытый исходный код. Каждый PR важен.</div>
  <h1 class="hero-title">Внести вклад<span class="hero-subtitle">Помогите нам улучшить Путеводитель автостопщика.</span></h1>
  <p class="hero-tagline">
    Вклад может быть любым: от исправления опечатки до написания целых новых разделов.
  </p>
  <div class="hero-cta-row">
    <a href="https://github.com/Anon-Planet/thgtoa/issues/new" class="hero-cta hero-cta--primary">Создать задачу</a>
    <a href="#pipeline" class="hero-cta hero-cta--secondary">Конвейер выпуска</a>
  </div>
</div>

---

## Настройка { #setup }

Сначала установите следующее.

=== "Linux / macOS"

    ```sh
    # Python 3.11+
    python3 --version

    # poppler (pdftoppm) и qpdf
    sudo apt install poppler-utils qpdf # Debian/Ubuntu
    brew install poppler qpdf           # macOS

    # GPG
    sudo apt install gnupg # Debian/Ubuntu
    brew install gnupg     # macOS

    # Зависимости Python
    pip install "mkdocs-material[imaging]" pillow numpy
    ```

=== "Windows"

    ```powershell
    # Python 3.11+ с https://python.org

    # poppler: https://github.com/oschwartz10612/poppler-windows/releases
    # Распакуйте и добавьте папку bin\ в PATH

    # qpdf: https://github.com/qpdf/qpdf/releases
    # Распакуйте и добавьте папку bin\ в PATH

    # GPG: https://gpg4win.org

    # Зависимости Python
    pip install "mkdocs-material[imaging]" pillow numpy
    ```

Для сборки светлой версии PDF также нужен установленный **Google Chrome** или **Microsoft Edge** (безголовый Chromium).

---

## Структура репозитория { #layout }

```txt
.github/
  workflows/
    01-build.yml      # builds PDFs, uploads artifact
    02-sign.yml       # hashes + GPG signs, uploads signatures artifact
    03-release.yml    # публикует GitHub Release со всеми ресурсами
    04-changelog.yml  # добавляет новую запись в начало docs/changelog/index.md
    publish.yml       # развёртывает сайт MkDocs на GitHub Pages
docs/
  guide/index.md      # руководство (один Markdown-файл)
  changelog/          # примечания к выпускам
  code/               # эта страница
export/               # выходные PDF (PDF игнорируются Git; .sha256, .b2sum, .asc отслеживаются)
pgp/                  # открытые ключи подписи
scripts/
  build_guide_pdf.py  # сборщик PDF на MkDocs + Chromium
  convert.py          # пиксельный конвертер PDF в тёмную тему
  install_fonts.py    # локальная установка шрифтов
  update_changelog.py # автогенерация записей журнала изменений из git log
  setup_workflow.py   # помощник настройки GitHub Secrets
  verify_pdf.py       # помощник проверки подписи
  archived/
    tag_release.py    # АРХИВ — помощник тегов GPG (не используется в текущем процессе)
```

---

## Локальная сборка { #build }

```sh
python scripts/build_guide_pdf.py --both
```

Собирает сайт MkDocs, рендерит его в `export/thgtoa.pdf` через безголовый Chromium, затем создаёт `export/thgtoa-dark.pdf`.

| Флаг | Эффект |
|------|--------|
| `--both` | Сначала светлый PDF, затем тёмный |
| _(нет)_ | Только светлый PDF |
| `--dark` | Только тёмный PDF (светлый PDF уже должен существовать) |

Собрать только тёмный PDF из существующего светлого:

```sh
python scripts/convert.py export/thgtoa.pdf export/thgtoa-dark.pdf
```

| Флаг | По умолчанию | Описание |
|------|---------|-------------|
| `--dpi` | `200` | DPI растеризации |
| `--batch-size` | `50` | Страниц на пакет — уменьшите при OOM |
| `--bg` | `1f1f31` | Цвет фона (hex) |
| `--text` | `e0e0e0` | Цвет основного текста (hex) |
| `--link` | `5e8bde` | Цвет ссылок (hex) |

Предпросмотр сайта:

```sh
mkdocs serve
# Открывается по адресу http://127.0.0.1:8000
```

---

## Вклад в содержание { #contributing }

<div class="index-grid">

  <div class="index-card">
    <h3 class="index-card__title">Используйте тематическую ветку</h3>
    <p class="index-card__body">Никогда не делайте коммит напрямую в <code>main</code>. Используйте отдельную тематическую ветку для каждого изменения, чтобы PR оставались проверяемыми и независимыми.</p>
  </div>

  <div class="index-card">
    <h3 class="index-card__title">Небольшие PR</h3>
    <p class="index-card__body">Разделяйте крупные изменения на несколько PR: один для нового содержания, другой для исправлений, третий для стиля. Большие PR блокируют слияния и создают долг проверки.</p>
  </div>

  <div class="index-card">
    <h3 class="index-card__title">Conventional Commits</h3>
    <p class="index-card__body">Все коммиты должны соответствовать формату <code>&lt;type&gt;(&lt;scope&gt;): &lt;description&gt;</code>. Его соблюдение обеспечивает pre-commit hook <code>commitizen</code>.</p>
  </div>

  <div class="index-card">
    <h3 class="index-card__title">Описывайте изменения</h3>
    <p class="index-card__body">Никогда не оставляйте описание PR пустым. Укажите, что изменилось, почему и какой контекст нужен проверяющему. Ссылайтесь на связанные задачи.</p>
  </div>

</div>

### Типы коммитов

| Тип | Раздел журнала изменений |
|------|-----------------|
| `feat`, `feature`, `add` | Добавлено |
| `fix`, `bugfix`, `revert`, `security` | Исправлено |
| `perf`, `refactor`, `change`, `chore`, `ci`, `docs`, `style`, `test`, `build` | Изменено |

Примеры:

```sh
feat: add dark-mode PDF export
fix(scripts): handle locked PDF on Windows
docs: update developer workflow guide
chore(ci): pin Chrome version to 120
```

### Правила

- **Следует** направлять PR в ветку `main`
- **Следует** писать «WIP» или открывать черновой PR для незавершённой работы
- **Следует** соблюдать [правило 50/72](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html) для сообщений коммитов
- **Не следует** выполнять массовые замены без проверки контекста каждого вхождения
- **Не следует** бросать PR во время проверки — оставайтесь на связи
- **Не следует** напрямую менять PR во время активной проверки — отправляйте изменения в ветку проверки

Пример того, чего _не_ следует делать, см. в [PR #51](https://github.com/Anon-Planet/thgtoa/pull/51).

!!! warning "Перед отправкой"
    - Убедитесь, что рабочее дерево чистое (`git status`)
    - Если вы меняли `docs/`, локально запустите `mkdocs build`, чтобы найти неработающие ссылки
    - Если вы добавили сноски, убедитесь, что у каждой есть определение `[^N]:` и хотя бы одна встроенная ссылка `[^N]`

---

## Конвейер выпуска { #pipeline }

После первоначальной сборки конвейер полностью ручной: ни один шаг не запускает следующий автоматически. Это предотвращает расхождения версий между собранным, подписанным и выпущенным содержимым.

```txt
push в main  (или ручной запуск)
      │
      ▼
  01-build.yml
  Собирает thgtoa.pdf + thgtoa-dark.pdf.
  Загружает артефакт: pdfs — запишите ID запуска.
      │
      │  вручную запустите 02-sign.yml с ID запуска сборки
      ▼
  02-sign.yml
  Вычисляет хеши (SHA-256 + BLAKE2b) и подписывает GPG все файлы.
  Коммитит export/ обратно в main.
  Загружает: signatures, pdfs-signed — запишите ID запуска.
      │
      │  вручную запустите 03-release.yml с ID запуска подписи
      ▼
  03-release.yml
  Запускает VirusTotal. Создаёт GitHub Release с тегом release-YYYYMMDD-<short-sha>.
      │
      │  вручную запустите 04-changelog.yml со строкой версии
      ▼
  04-changelog.yml
  Добавляет в начало docs/changelog/index.md новую запись ## [vX.Y.Z] и коммитит.
```

### Теги выпусков

Теги используют формат `release-YYYYMMDD-<short-sha>`, например `release-20260527-abc1234`. При выпуске не нужно выбирать версию: тег всегда уникален и однозначно связан с конкретным коммитом.

Строка версии (например, `v1.2.4`) — отдельная метка, назначаемая человеком и существующая только в журнале изменений.

### Запуск каждого шага

**Сборка:** Отправьте изменения в `main` или откройте **Actions → Build PDFs → Run workflow**. Запишите ID запуска.

**Подпись:** Откройте **Actions → Sign PDFs → Run workflow**, введите ID запуска сборки. Запишите ID запуска.

**Выпуск:** Откройте **Actions → Release → Run workflow**, введите ID запуска подписи.

**Журнал изменений:** Откройте **Actions → Update Changelog → Run workflow**, введите строку версии. Для предварительного просмотра используйте `dry_run: true`.

---

## Проверка выпуска { #verify }

```sh
# Импортировать ключ подписи выпусков
gpg --import pgp/anonymousplanet.asc

# Проверить PDF
gpg --verify thgtoa.pdf.asc      thgtoa.pdf
gpg --verify thgtoa-dark.pdf.asc thgtoa-dark.pdf

# Проверить файлы хешей
gpg --verify sha256sums.txt.asc sha256sums.txt
gpg --verify b2sums.txt.asc     b2sums.txt

# Проверить совпадение хешей PDF
sha256sum -c sha256sums.txt
b2sum     -c b2sums.txt
```

Ожидаемый вывод:

```txt
gpg: Signature made Sun 31 May 2026 03:23:26 AM EDT
gpg:                using EDDSA key C3023DBEA3FB38C438BA1EEDCEC60AEDE8B992A2
gpg: Good signature from "Anonymous Planet Release Signing Key" [ultimate]
Primary key fingerprint: C302 3DBE A3FB 38C4 38BA  1EED CEC6 0AED E8B9 92A2
```

Предупреждения GitHub/Codeberg наподобие «The email in this signature doesn't match the committer email» можно безопасно игнорировать.

---

## Устранение неполадок { #troubleshooting }

**Во время сборки MkDocs отсутствует `cairosvg`**
`pip install "mkdocs-material[imaging]"` — требуется плагину `social`.

**`KeyError: 'JPEG'` в convert.py**
`sudo apt install libjpeg-dev && pip install --force-reinstall pillow`

**`qpdf: can't find PDF header`**
qpdf принимает только PDF на вход — убедитесь, что используете актуальную версию `convert.py`.

**Подпись GPG не выполняется: `No secret key`**
Экспортируйте заново: `gpg --armor --export-secret-keys <fingerprint>`, затем вновь вставьте полный блок вместе с заголовками в секрет `GPG_PRIVATE_KEY`.

**Подпись GPG не выполняется: `Bad passphrase`**
В секрете `GPG_PASSPHRASE` есть пробел или перевод строки в конце. Вставьте значение заново, без окружающих пробельных символов.

**`03-release.yml` завершается с ошибкой на VirusTotal**
`VT_API_KEY` отсутствует, недействителен или превышен бесплатный лимит в 500 запросов в день. Повторите запуск через несколько минут.

**`02-sign.yml` не может скачать артефакт PDF**
Неверный `build_run_id` либо срок хранения артефакта истёк (90 дней). Запустите новую сборку.

**Журнал изменений уже содержит версию X**
`update_changelog.py` завершается с ошибкой, если версия уже есть. Выберите следующую строку версии.

**Предупреждения о сносках: `link '#fnref:N' has no anchor`**
Определение `[^N]:` существует без соответствующей встроенной ссылки. Добавьте ссылку или удалите осиротевшее определение.
