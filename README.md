# Sprint_6 — Автотесты Яндекс.Самокат

Проект содержит UI-автотесты для учебного сервиса [Яндекс.Самокат](https://qa-scooter.praktikum-services.ru/).

## Требования

- Python 3.8+
- Mozilla Firefox (для запуска тестов)
- Chrome (опционально)

## Установка

```bash
pip install -r requirements.txt
```

## Запуск тестов

### Все тесты (Firefox по умолчанию)
```bash
pytest
```

### Конкретный тест-класс
```bash
pytest tests/test_faq.py -v
pytest tests/test_order.py -v
pytest tests/test_navigation.py -v
```

### Headless режим
```bash
pytest --headless
```

## Структура проекта

```
Sprint_6/
├── pages/          # Page Object Model
│   ├── main_page.py
│   └── order_page.py
├── locators/       # Локаторы элементов
│   ├── main_page_locators.py
│   └── order_page_locators.py
├── data/           # Тестовые данные
│   ├── order_data.py
│   └── faq_data.py
├── tests/          # Тесты
│   ├── test_faq.py       # FAQ аккордеон
│   ├── test_order.py     # Заказ самоката
│   └── test_navigation.py # Навигация по логотипам
├── conftest.py     # Фикстуры pytest
└── requirements.txt
```

## Покрытые сценарии

1. **FAQ** — проверка выпадающего списка «Вопросы о важном» (8 тестов)
2. **Заказ самоката** — позитивный сценарий с 2 наборами данных и 2 точками входа
3. **Навигация** — клик по логотипу Самоката и Яндекса
