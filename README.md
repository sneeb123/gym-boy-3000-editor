# Gym-Boy 3000 — веб-редактор тренировок

Статическая страница: открывает файлы приватного репозитория-хранилища Gym-Boy 3000
(`programs/…`, `results/…`) таблицей подходов и сохраняет правки обратно через GitHub Contents API.

**Открыть редактор:** https://sneeb123.github.io/gym-boy-3000-editor/

## Как войти

1. GitHub → Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token
2. Repository access → Only select repositories → ваш репозиторий данных (`gymboy-data` или `gymboy-cloud`)
3. Permissions → Contents → Read and write
4. Вставить токен на странице редактора — он запомнится в этом браузере

## Приватность

- Страница полностью статическая, сервера нет: всё выполняется в вашем браузере.
- Токен хранится только в localStorage вашего браузера и отправляется только на api.github.com.
- Данные тренировок читаются и пишутся напрямую в ваш приватный репозиторий — сквозь эту страницу они никуда больше не идут.

Файлы те же, что видит приложение Gym-Boy 3000 на телефоне: правки подхватятся при следующем синке.
