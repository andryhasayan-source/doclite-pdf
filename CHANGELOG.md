# История версий · Changelog

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
