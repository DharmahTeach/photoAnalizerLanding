# Инструкция по деплою на GitHub Pages

## 1. Создайте репозиторий на GitHub

1. Перейдите на https://github.com/new
2. Название репозитория: `body-metrics-landing` (или любое другое)
3. Выберите **Public**
4. **НЕ** создавайте README, .gitignore или лицензию (они уже есть)
5. Нажмите "Create repository"

## 2. Подключите удаленный репозиторий

```bash
cd C:\p\BOTS\PhotoAnalizer\landing2\dist
git remote add origin https://github.com/[ВАШ-USERNAME]/[НАЗВАНИЕ-РЕПОЗИТОРИЯ].git
git push -u origin main
```

Замените `[ВАШ-USERNAME]` и `[НАЗВАНИЕ-РЕПОЗИТОРИЯ]` на ваши данные.

## 3. Включите GitHub Pages

1. Перейдите в Settings репозитория
2. В левом меню выберите **Pages**
3. В разделе **Source** выберите:
   - Branch: `main`
   - Folder: `/ (root)`
4. Нажмите **Save**

## 4. Ваш сайт будет доступен по адресу:

`https://[ВАШ-USERNAME].github.io/[НАЗВАНИЕ-РЕПОЗИТОРИЯ]/`

## Обновление сайта

После изменений в исходниках:

```bash
cd C:\p\BOTS\PhotoAnalizer\landing2
npm run build
cd dist
git add .
git commit -m "Update landing page"
git push
```

Сайт обновится автоматически через несколько минут.

