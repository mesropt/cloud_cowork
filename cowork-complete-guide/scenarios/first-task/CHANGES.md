# Организация файлов — Basecamp Coffee Roasters
**Дата:** 31 марта 2026
**Выполнено:** Claude (Cowork)

---

## Структура папок

```
first-task/
├── finances/
│   ├── invoices/       ← счета от поставщиков
│   └── receipts/       ← кассовые чеки
├── legal/              ← договоры и соглашения
├── operations/
│   ├── data/           ← таблицы и аналитика
│   └── notes/          ← заметки, задачи, протоколы
└── marketing/          ← соцсети и промо
```

---

## Что и куда переместили

| Исходное имя | Новое расположение | Почему |
|---|---|---|
| `Document1.txt` | `finances/invoices/invoice-mountain-view-2026-01-08.txt` | Счёт от Mountain View Supplies на $594 |
| `IMG_4521.txt` | `finances/receipts/receipt-basecamp-2026-01-10.txt` | Чек за покупку в кофейне |
| `IMG_4523.txt` | `finances/receipts/receipt-office-depot-2026-01-07.txt` | Чек из Office Depot |
| `contract_final_v2.txt` | `legal/supplier-agreement-green-valley-2026.txt` | Договор с поставщиком выпечки |
| `data.csv` | `operations/data/sales-data-jan-2026.csv` | Данные о продажах за январь 2026 |
| `download(1).txt` | `operations/notes/health-inspection-dec-2025.txt` | Акт санитарной проверки (96/100) |
| `download.txt` | `operations/notes/meeting-notes-2026-01-05.txt` | Протокол командного совещания |
| `notes.txt` | `operations/notes/spring-menu-ideas.txt` | Идеи для весеннего меню |
| `todo.txt` | `operations/notes/weekly-todo.txt` | Список задач на неделю |
| `Screenshot 2026-01-03.txt` | `marketing/instagram-post-2026-01-03.txt` | Пост в Instagram от 3 января |

---

## Решения, которые я принял самостоятельно

- Переименовал все файлы с информативными именами (дата, содержание, источник)
- Разделил финансы на счета и чеки — разные цели и хранение
- Санитарную проверку отнёс к operations, а не legal — это рабочий документ, не договор
- README.md оставил на месте — это служебный файл сценария
