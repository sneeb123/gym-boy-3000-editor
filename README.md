# Gym-Boy 3000 — web editor

`index.html` is a single-page editor for the files of the private Gym-Boy 3000
cloud (`programs/pending`, `programs/imported`, `results`): file list →
table editor (a block per exercise, a row per set) → written back to the
repository through the Contents API. No build step, no dependencies, no backend.

Documentation is maintained in three languages, in this order:
**English → 中文 → Русский**.

## English

- **Run locally**: just open `index.html` in a browser (double click) —
  api.github.com works from `file://` too.
- **GitHub Pages** (access from a phone): put `index.html` in the root of a
  public repository → Settings → Pages → Source: main. Only the editor page
  becomes public; the data stays in the private `gymboy-data` repository.
- **Sign-in**: a fine-grained PAT is pasted once
  (github.com/settings/personal-access-tokens/new): Repository access —
  `gymboy-data` only, Permissions → Contents — Read and write. The token is
  stored in the browser's localStorage and is only ever sent to api.github.com;
  the «sign out» link erases it.
- **Interface languages**: the button in the header cycles English → 中文 →
  Русский (English is the default); the choice is remembered in this browser.
- **Behavior**: the «total» column recomputes itself (plates + bar), set
  numbering too; a comma is accepted as the decimal separator. Required fields
  are checked before saving; on a conflict (the file changed in the cloud since
  it was opened) the editor offers to reload it. A public repository shows an
  amber warning (like the app since v0.10.1), but edits are not blocked.
- Commits are signed `Gym-Boy 3000: правка в веб-редакторе — <file>`; result
  files (`gymboy-result/1`) are edited with the same table; unknown JSON fields
  are preserved as-is.

## 中文

- **本地运行**：直接在浏览器中打开 `index.html`（双击）——`file://` 下也能访问
  api.github.com。
- **GitHub Pages**（从手机访问）：把 `index.html` 放进一个公开仓库的根目录 →
  Settings → Pages → Source: main。只有编辑器页面是公开的；数据仍保存在私有的
  `gymboy-data` 仓库中。
- **登录**：只需粘贴一次细粒度 PAT
  （github.com/settings/personal-access-tokens/new）：Repository access 只选
  `gymboy-data`，Permissions → Contents 选 Read and write。令牌保存在浏览器
  localStorage 中，只会发送到 api.github.com；「退出」链接会将其抹除。
- **界面语言**：点击顶栏按钮循环切换 English → 中文 → Русский（默认英文）；
  选择会保存在本浏览器中。
- **行为**：「总计」列自动重算（杠铃片 + 杠），组编号也是；逗号可作为小数点。
  保存前检查必填字段；若发生冲突（文件在打开后被云端修改），编辑器会建议重新
  读取。公开仓库会显示琥珀色警告（与 v0.10.1 起的应用一样），但不会阻止修改。
- 提交均带有 `Gym-Boy 3000: правка в веб-редакторе — <文件>` 前缀；结果文件
  （`gymboy-result/1`）用同一张表格编辑；未知的 JSON 字段原样保留。

## Русский

- **Локально**: просто открыть `index.html` в браузере (двойной клик) —
  обмен с api.github.com работает и с `file://`.
- **GitHub Pages** (доступ с телефона): положить `index.html` в корень
  публичного репозитория → Settings → Pages → Source: main. Публичной
  становится только страница редактора; данные остаются в приватном
  `gymboy-data`.
- **Вход**: один раз вставляется fine-grained PAT
  (github.com/settings/personal-access-tokens/new): Repository access — только
  `gymboy-data`, Permissions → Contents — Read and write. Токен хранится в
  localStorage браузера и уходит только на api.github.com; ссылка «выйти» его
  стирает.
- **Языки интерфейса**: кнопка в шапке листает English → 中文 → Русский
  (по умолчанию английский); выбор запоминается в этом браузере.
- **Поведение**: «итого» пересчитывается сам (блины + гриф), нумерация
  подходов — тоже; запятая принимается как десятичный разделитель. Перед
  записью — проверка обязательных полей; при конфликте (файл в облаке
  изменился с момента открытия) редактор предлагает перечитать файл.
  Публичный репозиторий — янтарное предупреждение (как в приложении с
  v0.10.1), но правки не блокируются.
- Коммиты подписаны `Gym-Boy 3000: правка в веб-редакторе — <файл>`; файлы
  результатов (`gymboy-result/1`) правятся той же таблицей; незнакомые поля
  JSON сохраняются как были.
