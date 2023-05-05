# Определение стоимости автомобилей

Сервис по продаже автомобилей с пробегом «Не бит, не крашен» разрабатывает приложение для привлечения новых клиентов. В нём можно быстро узнать рыночную стоимость своего автомобиля. В вашем распоряжении исторические данные: технические характеристики, комплектации и цены автомобилей.

## Цель исследования:

Нужно построить модель для определения стоимости.

Заказчику важны:

- качество предсказания;
- скорость предсказания;
- время обучения.

## Итог исследования:


- Рассмотрен датасет с объявлениями о продаже автомобилей в начале 2016 года. Обнаружено значительное количество пропусков в столбцах Repaired, VehicleType, FuelType, Gearbox, Model. Данные проверены на корреляцию Пирсона и нелинейную корреляцию при помощи библиотеки phik. Корреляция признаков между собой незначительна.
- Данные предобработаны. В датасете выявлены и удалены явные дубликаты.Определены неинформативные признаки.В данных обнаружены аномальные значения в столбцах RegistrationYear, Power, Price.Для заполнения пропусков в категориальных переменных было принято решение использовать отдельное значение "unknown".
- Рассмотрены модели дерево решений, случайного леса, LightGBM и Catboost.
- Для модели Catboost рассмотрены варианты использования встроеннго кодировщика и OrdinalEncoder. Результаты по полученным метрикам схожие, однако время обучения с использованием втроенного кодировщика оказалось значительно больше, чем использование OrdinalEncoder. Поэтому вариант с OrdinalEncoder оказался более предпочтительным.
- Наилучшие результаты по RMSE показала модель CatBoost, далее RandomForest и LightGBM. RandomForest показал значительно большее время на обучении и предсказаниях, чем остальные модели. Время предсказаний у моделей CatBoost и LightGBM приблизительно одинаковое, однако время обучения CatBoost значительно больше. Метрика RSME несколько хуже, чем у CatBoost, но меньше 2500, что удовлетворяет требованиям технического задания. 
- По итогам исследования была выбрана модель LightGBM. Получена метрика RMSE = 1916.625 на тестовой выборке.


## Стек технологий:

Pandas, matplotlib, numpy, scikit-learn, seaborn, CatBoost, XGBoost, LightGBM

## Статус проекта:

Завершен.