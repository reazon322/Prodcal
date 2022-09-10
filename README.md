# Prodcal

Можно использовать собрынные json файлы из **data**.

Парсинг производственных календарей с сайта **consultant.ru**.

**Формат:**

```json
{
  '2022-02-21': 'workday',
  '2022-02-22': 'preholiday',
  '2022-02-23': 'holiday weekend',
  '2022-02-24': 'workday',
}
```

**Статусы:**

- workday (рабочий)
- preholiday (предпраздничный, сокращенный)
- weekend (выходной)
- nowork (нерабочий)


**Пример использования**

```Python
from workingcal import get_working_calendar, save_working_calendar

data = get_working_calendar(input_year=2022)
save_working_calendar(data=data, path='data')
```

**В командной строке**

```bash
# Календарь текущего года
> python3 main.py
```

```bash
# Календарь 2010 и 2023 года
> python3 main.py --years 2010 2023
```

```bash
# Календари за период с 2010 по 2022 год
> python3 main.py --range 2010 2023
```

```bash
# Дополнительно: можно указать папку для скачивания.
# По умолчанию всегда создается папка "data"
> python3 main.py --range 2010 2023 --path your_folder
```


**Зависимости**
```bash
> pip3 install -r requirements.txt
```
