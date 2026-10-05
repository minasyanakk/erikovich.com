# Сайт-визитка Arthur Minasian

Статический сайт для GitHub Pages: страницы на украинском (`/`) и английском (`/en/`), разметка schema.org (Person + ProfilePage), `robots.txt`, открытый для ИИ-краулеров, `sitemap.xml` и `llms.txt`.

## Публикация (10 минут)

1. Создайте на GitHub репозиторий с именем **`<ваш-логин>.github.io`**.
2. Если ваш логин не `arthur-erikovich`, замените адрес во всех файлах одной командой:
   ```bash
   grep -rl "arthur-erikovich.github.io" . | xargs sed -i "s/arthur-erikovich.github.io/ВАШ-ЛОГИН.github.io/g"
   ```
   (на macOS: `sed -i ''`)
3. Положите в корень своё фото с именем **`avatar.jpg`** (квадрат, от 400×400). На него уже ссылается разметка.
4. Загрузите файлы:
   ```bash
   git init && git add . && git commit -m "Personal site"
   git branch -M main
   git remote add origin https://github.com/ВАШ-ЛОГИН/ВАШ-ЛОГИН.github.io.git
   git push -u origin main
   ```
5. В репозитории откройте Settings → Pages → Source: `main` / root. Через 1–2 минуты сайт будет доступен.

## После публикации

- **Google Search Console** и **Bing Webmaster Tools**: добавьте сайт и отправьте `sitemap.xml`. Bing особенно важен, потому что на его индексе работают ChatGPT Search и Copilot.
- Проверьте разметку на https://validator.schema.org.
- Поставьте ссылку на сайт в био Threads, а также в LinkedIn, Telegram и другие профили. Взаимные ссылки «профиль ↔ сайт» подтверждают, что это один человек.
- Когда появятся новые профили (LinkedIn, Telegram-канал, статьи, интервью), добавьте их ссылки в `sameAs` внутри JSON-LD и в блок «Профили» на обеих страницах.
- Раз в несколько месяцев обновляйте текст и дату в `dateModified`: свежие страницы краулеры обходят чаще.

## Свой домен позже

Купите домен, добавьте в корень файл `CNAME` с этим доменом, настройте DNS по инструкции GitHub Pages и замените адрес во всех файлах той же командой `sed`.
