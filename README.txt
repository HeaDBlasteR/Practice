# AvaloniaTests — Система тестирования

Кроссплатформенное десктопное приложение для создания, редактирования и прохождения тестов. Реализовано на Avalonia UI с использованием паттерна MVVM и современных подходов к DI и реактивному программированию.

## 🎯 Описание

**AvaloniaTests** позволяет:
- Создавать и редактировать тесты с вопросами и вариантами ответов
- Проходить тесты с пошаговой навигацией
- Просматривать историю и детали результатов
- Управлять базой тестов и результатами

## 🔧 Технологии

- **.NET**: 8.0
- **UI**: Avalonia UI 11.3.2 (Fluent Theme)
- **MVVM**: CommunityToolkit.Mvvm, ReactiveUI 20.4.1
- **DI**: Microsoft.Extensions.DependencyInjection 9.0.7
- **Сериализация**: System.Text.Json 9.0.7

## ⚙️ Системные требования

- .NET 8.0 Runtime или выше
- Windows, Linux, macOS

## 🗂️ Архитектура и компоненты

### Models
- `Test` — тест с коллекцией вопросов
- `Question` — вопрос с вариантами ответов
- `Answer` — вариант ответа
- `TestResult` — результат прохождения теста

### ViewModels
- `MainWindowViewModel` — главное окно, управление тестами и результатами
- `TestEditorViewModel` — создание/редактирование тестов
- `TestRunnerViewModel` — прохождение теста
- `ResultViewModel` — просмотр результата

### Services
- `ITestService` — работа с тестами (JsonTestService)
- `IResultService` — работа с результатами (JsonResultService)
- `IWindowService` — управление окнами приложения
- `IDialogService` — диалоговые окна (редактор вопросов, подтверждения)
- `IErrorDialogService` — обработка ошибок

## 📱 Основная функциональность

### Управление тестами
- Создание, редактирование, удаление тестов
- Добавление/удаление вопросов и вариантов ответов
- Указание правильных ответов

### Прохождение тестов
- Пошаговая навигация по вопросам
- Выбор ответов, автоматический подсчёт результата
- Итоговое окно с результатом

### Просмотр результатов
- История прохождений
- Детализация по каждому тесту: баллы, процент, дата

## 🎨 Особенности интерфейса

- Современный дизайн (Fluent Theme)
- Адаптивная верстка
- Диалоговые окна для подтверждений и ошибок
- Интуитивная навигация между окнами

## 💾 Хранение данных

- Все тесты и результаты сохраняются в JSON-файлах (`tests.json` и др.)
- Файлы автоматически копируются в выходную директорию

## 🧩 DI и расширяемость

- Все сервисы и ViewModel регистрируются через `ServiceProvider`
- Легко добавлять новые сервисы и ViewModel

## 📝 Пример использования

1. **Создание теста**:  
   Запустите приложение → "Создать тест" → заполните поля → добавьте вопросы и ответы → отметьте правильные → сохраните.
2. **Прохождение теста**:  
   Выберите тест → "Пройти тест" → отвечайте на вопросы → получите результат.
3. **Просмотр результатов**:  
   Перейдите на вкладку "Результаты" → выберите интересующий результат.

## 🤝 Вклад и стиль кода

- Используйте C# 12.0
- Следуйте принципам SOLID и MVVM
- Используйте async/await для асинхронных операций
- Оформляйте код с комментариями для сложной логики

## 📄 Лицензия

MIT

## 🔗 Полезные ссылки

- [Avalonia UI](https://docs.avaloniaui.net/)
- [ReactiveUI](https://www.reactiveui.net/)
- [.NET 8](https://learn.microsoft.com/ru-ru/dotnet/)