# Проект для «Викишоп»

Интернет-магазин «Викишоп» запускает новый сервис. Теперь пользователи могут редактировать и дополнять описания товаров, как в вики-сообществах. То есть клиенты предлагают свои правки и комментируют изменения других. Магазину нужен инструмент, который будет искать токсичные комментарии и отправлять их на модерацию. 

## Цель исследования:

Обучите модель классифицировать комментарии на позитивные и негативные. В вашем распоряжении набор данных с разметкой о токсичности правок.

Постройте модель со значением метрики качества *F1* не меньше 0.75. 

## Итог исследования:

- Рассмотрен датасет комментариев в интернет-магазине с разметкой о токсичности правок.Проведена очистка текста от ненужных символов, пунктуации, чисел и лемманизация слов в тексте.Создана матрица TF-IDF признаков.
- Обучены модели для классификации комментариев на позитивные и негативные.
- Рассмотрена библиотека FastText, использующая word embeddings.
- FastText показала наилуший результат, удовлетворяющий условиям ТЗ по метрике F1.

## Стек технологий:

Pandas, matplotlib, numpy, scikit-learn, seaborn, NLTK, re, CatBoost, XGBoost, LightGBM

## Статус проекта:

Завершен частично, будет добавлена модель BERT.