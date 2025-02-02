# Прогнозирование количества посетителей ресторанов

Этот проект направлен на создание модели для прогнозирования количества посетителей ресторанов на основе различных факторов, таких как данные о бронированиях, информация о ресторанах, а также информация о днях недели и праздниках. Модель использует алгоритм градиентного бустинга для предсказания целевой переменной.

## Описание данных

В проекте используются следующие наборы данных:

1. **air_reserve.csv** — данные о бронированиях для ресторанов сети Air.
2. **hpg_reserve.csv** — данные о бронированиях для ресторанов сети HPG.
3. **air_store_info.csv** — информация о ресторанах сети Air.
4. **hpg_store_info.csv** — информация о ресторанах сети HPG.
5. **air_visit_data.csv** — данные о посещениях ресторанов сети Air.
6. **date_info.csv** — информация о датах, включая праздники и специальные события.
7. **store_id_relation.csv** — связь между ресторанами сети Air и HPG.

## Структура проекта

1. **Обработка данных**:
   - Конвертация дат в формат `datetime`.
   - Создание признаков, таких как разница между датой бронирования и датой посещения, день недели, час.
   - Агрегация данных о бронированиях и объединение с основными данными о посещениях и информации о ресторанах.

2. **Подготовка данных для обучения**:
   - Кодирование категориальных признаков (жанр ресторана, район, день недели).
   - Создание матрицы признаков и целевой переменной (количество посетителей).

3. **Моделирование**:
   - Разделение данных на тренировочную и тестовую выборки.
   - Обучение модели градиентного бустинга (`GradientBoostingRegressor`).
   - Оценка качества модели с использованием метрик MAE и RMSE.

