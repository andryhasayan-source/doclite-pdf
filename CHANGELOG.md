# История версий · Changelog

## 1.5.0 — рабочий центр документов

- Новое название: «DocLite PDF — рабочий центр документов» — число
  инструментов больше не пишем, их становится больше
  *New name: “DocLite PDF — Document Workspace”; we no longer put a tool
  count in the name, as the number keeps growing*
- Новый инструмент «Страницы»: миниатюры страниц — переставить, повернуть,
  удалить мышкой; большие документы открываются быстро
  *New tool, Pages: page thumbnails — reorder, rotate and delete with the
  mouse; large documents open quickly*
- Новый инструмент «Пароль»: поставить или снять пароль на PDF, шифрование
  AES-256 на вашем компьютере. Файл, который открывается без пароля, но
  с ограничениями на печать или изменение, освобождается от них без пароля
  *New tool, Password: add or remove a PDF password, AES-256 encryption on
  your computer. A file that opens without a password but has printing or
  editing restrictions can be freed of them without one*
- Подпись: печати и штамп «Копия верна» с должностью, фамилией и датой,
  несколько отметок на листе, «на все страницы»
  *Signature: stamps and a “True copy” certification with position, name and
  date, several marks per page, “apply to all pages”*
- Порядок документов при объединении и картинок в JPG → PDF: перетаскивание,
  стрелки, номера
  *Document order in Merge and image order in JPG → PDF: drag and drop,
  arrows, numbers*
- Точное распознавание текста для мелкого шрифта и плохих сканов (модели
  ~15 МБ на язык, примерно в 2,5 раза медленнее)
  *Precise text recognition for small print and poor scans (models ~15 MB
  per language, about 2.5 times slower)*
- Распознавание в PDF и в Word с расположением читает подготовленную копию
  страницы, а в документ кладёт цветной оригинал: на паспортах и бланках
  текста находится заметно больше, печати остаются цветными
  *Recognition to PDF and to Word with layout reads a prepared copy of the
  page but keeps the colour original in the document: noticeably more text on
  passports and forms, stamps stay in colour*
- Большие файлы (от 8 МБ или 40 страниц) сжимаются в фоне
  *Large files (8 MB or 40 pages and up) are compressed in the background*
- Водяной знак и нумерация сразу на несколько файлов — результат одним архивом
  *Watermark and page numbers for several files at once — one archive back*
- Защищённый PDF больше не даёт непонятную ошибку или битый файл: все
  инструменты говорят, что файл защищён, и подсказывают вкладку «Пароль»;
  операция не списывается
  *A protected PDF no longer produces an obscure error or a broken file: every
  tool says the file is protected and points to the Password tab; no
  operation is charged*
- Исправлено: пароли, начинающиеся с «-» или «@», не ставились
  *Fixed: passwords starting with “-” or “@” could not be set*
- Исправлено: при быстрой смене файла во вкладке «Страницы» порядок страниц
  мог примениться не к тому файлу
  *Fixed: switching files quickly on the Pages tab could apply the page order
  to the wrong file*
- Меньше расход памяти при сжатии и подписи больших документов
  *Lower memory use when compressing and signing large documents*

## 1.4.1 — укрепление

- Защита от уязвимости pdf.js (CVE-2024-4367): при открытии PDF запрещено
  исполнение кода из шрифтов
  *Protection against a pdf.js vulnerability (CVE-2024-4367): code execution
  from fonts is disabled when opening PDFs*
- Библиотека Excel обновлена до SheetJS 0.20.3 — закрыты две уязвимости при
  чтении специально собранных файлов (CVE-2023-30533, CVE-2024-22363)
  *Excel library updated to SheetJS 0.20.3, closing two vulnerabilities in
  reading crafted files (CVE-2023-30533, CVE-2024-22363)*
- Страница печати не может отправлять данные в интернет: скрипты страницы в
  HTML → PDF выполняются, картинки грузятся, но запросы наружу блокируются
  *The print page cannot send data to the internet: scripts in HTML → PDF still
  run and images still load, but outbound requests are blocked*
- Понятный отказ вместо падения окна для слишком больших файлов: до 300 МБ на
  файл и до 600 МБ суммарно для объединения
  *A clear message instead of a crashed window for oversized files: up to
  300 MB per file and 600 MB in total for merging*
- PDF распознаётся и по расширению — файлы без типа (бывает на Windows) больше
  не отсеиваются
  *PDFs are also recognized by extension — files without a type (happens on
  Windows) are no longer dropped*
- Лицензия PRO действует только на той установке, для которой выдана
  *A PRO license only works on the installation it was issued for*
- Понятное сообщение при переполнении хранилища браузера; окно открывается на
  вкладке последней фоновой задачи
  *A clear message when browser storage is full; the window opens on the tab of
  the latest background task*

## 1.4.0 — работа в фоне

- Распознавание текста и конвертация больших PDF в Word теперь идут в фоне:
  окно расширения можно закрыть, по готовности приходит уведомление
  с предложением сохранить результат
  *Text recognition and conversion of large PDFs to Word now run in the
  background: you can close the extension window and will get a notification
  offering to save the result when it is done*
- Очередь задач: можно поставить несколько файлов сразу, любую задачу видно,
  можно остановить, а последние результаты остаются в истории
  *A task queue: add several files at once, watch and stop any task, and keep
  recent results in the history*
- Если в PDF уже есть текст, он берётся из документа — распознавать нечего.
  В документах со смешанными страницами распознаются только страницы без текста
  *If a PDF already has text, that text is used as is. In mixed documents only
  the pages without text are recognized*
- Excel → PDF переписан: колонки, объединённые ячейки, рамки, шрифты и
  настройки печати берутся из файла, бланки печатаются как в Excel
  *Excel → PDF rewritten: column widths, merged cells, borders, fonts and print
  settings come from the file, so forms print the way they do in Excel*
- PDF → Word и PDF → Excel: восстановлены пробелы между словами, которые
  терялись в заголовках с плотным набором
  *PDF → Word and PDF → Excel: restored spaces between words that were lost in
  tightly spaced headings*
- Исправлено: у распознавания списывались две бесплатные операции вместо одной
  *Fixed: text recognition charged two free operations instead of one*

## 1.3.3 — распознавание текста (OCR)

- Новый инструмент: распознавание текста — скан или фото в PDF с текстовым
  слоем или сразу в Word
  *New tool: text recognition (OCR) — turn a scan or photo into a searchable
  PDF or a Word file*
- Русский и английский языки, автоматическое определение поворота страницы,
  фильтр мусора
  *Russian and English, automatic page-rotation detection, a junk filter*
- Языковые модели (~4 МБ на язык) скачиваются один раз по запросу и хранятся
  в браузере — дальше распознавание работает офлайн
  *Language models (~4 MB per language) download once, on request, and are
  kept in the browser — recognition then runs offline*
- Теперь одиннадцать инструментов вместо десяти
  *Now eleven tools instead of ten*

## 1.0.1 — 6 сентября 2026

Первая публичная версия в Chrome Web Store.
*First public release in the Chrome Web Store.*

- Десять инструментов для работы с PDF, вся обработка локальная
  *Ten PDF tools, all processing done locally*
- Интерфейс на русском и английском с переключателем
  *Russian and English interface with an in-app switch*
- Бесплатный режим: три операции в сутки, все инструменты доступны
  *Free tier: three operations a day, every tool unlocked*
- PRO: разовая покупка, лицензия без срока действия
  *PRO: one-time purchase, perpetual licence*
