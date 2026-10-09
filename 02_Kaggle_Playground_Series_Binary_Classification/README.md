<a id="top"></a>

<p align="right">
  <a href="#ru">🇷🇺 RU</a> | <a href="#en">🇬🇧 EN</a>
</p>

---

<a id="ru"></a>

# Прогнозная модель отклика клиента на банковское предложение

## 📌 Описание
Проект выполнен в рамках соревнования [Kaggle Playground Series — Season 5, Episode 8](https://www.kaggle.com/competitions/playground-series-s5e8).  
Цель — построить модель машинного обучения, которая предсказывает, подпишется ли клиент на банковский срочный депозит на основе его демографических характеристик и истории взаимодействия с банком.

Практическая ценность:
- Оптимизация маркетинговых кампаний за счёт точного таргетинга.  
- Снижение затрат на рекламу и повышение конверсии.  
- Анализ факторов, влияющих на решение клиента.  
- Персонализация предложений для клиентов.

---

## 🔧 Стек технологий
- Python  
- pandas, numpy
- matplotlib, seaborn  
- phik (корреляционный анализ), scipy.stats
- Feature Engineering: создание бизнес-признаков, взаимодействия, категоризация
- scikit‑learn (Logistic Regression, DummyClassifier, StratifiedKFold)  
- LightGBM, XGBoost, CatBoost
- Оптимизация: GridSearchCV, кросс-валидация
- Kaggle API для автоматической загрузки данных

---

## 📊 Данные
- Датасет синтетически сгенерирован на основе [Bank Marketing Dataset Full](https://www.kaggle.com/datasets/sushant097/bank-marketing-dataset-full).  
- Размер обучающей выборки: **750 000 клиентов**, тестовой — **250 000**.  
- Признаки: возраст, работа, семейное положение, образование, баланс, наличие кредита, параметры маркетинговой кампании (канал связи, месяц, длительность контакта, количество контактов, результат предыдущей кампании).  
- Целевая переменная: подписка на депозит (0 — нет, 1 — да).  
- Особенность: сильный дисбаланс классов (≈12% подписавшихся против 88% отказавшихся).

---
## Ключевые этапы проекта
1. **Загрузка и предобработка** - анализ структуры, обработка категориальных признаков
2. **EDA** - анализ распределений, выявление сезонности, целевых сегментов
3. **Feature Engineering** - создание бизнес-признаков, анализ корреляций
4. **Обучение моделей** - сравнение 4 алгоритмов, подбор гиперпараметров
5. **Анализ важности признаков** - интерпретация результатов
6. **Формирование прогнозов** - подготовка submission для Kaggle
7. **Валидация на оригинальных данных** - проверка устойчивости модели

---
## 📈 Результаты
- Проведён полный цикл: загрузка данных → предобработка → EDA → feature engineering → обучение моделей → формирование submission.  
- Лучший результат показала модель **LightGBM** с ROC‑AUC = **0.9636**.  
- Выявлены ключевые факторы отклика: длительность контакта, результат предыдущей кампании, месяц звонка, баланс клиента.  
- Построены профили клиентов, наиболее склонных к подписке на депозит.  
- Даны рекомендации по оптимизации маркетинговой стратегии.
- Проект подтверждает навыки: EDA, Feature Engineering, подбор гиперпараметров, работа с дисбалансом, интерпретация моделей

Модель может использоваться в реальном банке для оптимизации маркетинговых кампаний

---
## 📁 Структура репозитория

`02_Kaggle_Playground_Series_Binary_Classification/`

```text
├── `Binary_Classification_with_BankDataset.ipynb`      — основной ноутбук с полным анализом  
├── `Binary_Classification_with_a_BankDataset.pdf`        — экспорт в PDF 
├── `requirements.txt`                                     — зависимости проекта 
└── `README.md`                                            — эта документация
```

---

## 🚀 Как запустить
1. Склонировать репозиторий:  
   ```bash
   git clone https://github.com/aspozd-DA-DS/DataScience_projects.git
   ```
2. Перейти в папку проекта:

   ```bash
   cd DataScience_projects/02_Kaggle_Playground_Series_Binary_Classification
   ```

3. Запустить ноутбук:

   ```bash
   jupyter notebook "Binary_Classification_with_BankDataset.ipynb.ipynb"
   ```
4. Убедитесь, что у вас настроен Kaggle API для автоматической загрузки данных

## 🏷 Topics
`Data Analysis` `EDA` `Visualization` `Kaggle` `Python` `Machine Learning` `Classification` `Bank Marketing`  `lightgbm`  `xgboost`  `catboost` `feature-engineering` `roc-auc`

<p align="right"><a href="#top">⬆ наверх</a></p>

---

<a id="en"></a>

# Predictive model of customer response to a banking offer

## 📌 Description
This project was completed as part of the [Kaggle Playground Series — Season 5, Episode 8](https://www.kaggle.com/competitions/playground-series-s5e8) competition.  
The goal is to build a machine learning model that predicts whether a client will subscribe to a bank term deposit, based on their demographic characteristics and history of interaction with the bank.

Practical value:
- Optimizing marketing campaigns through precise targeting.  
- Reducing advertising costs and increasing conversion.  
- Analyzing the factors that influence a client's decision.  
- Personalizing offers for clients.

---

## 🔧 Tech stack
- Python  
- pandas, numpy
- matplotlib, seaborn  
- phik (correlation analysis), scipy.stats
- Feature Engineering: creating business features, interactions, categorization
- scikit-learn (Logistic Regression, DummyClassifier, StratifiedKFold)  
- LightGBM, XGBoost, CatBoost
- Optimization: GridSearchCV, cross-validation
- Kaggle API for automatic data download

---

## 📊 Data
- The dataset was synthetically generated based on the [Bank Marketing Dataset Full](https://www.kaggle.com/datasets/sushant097/bank-marketing-dataset-full).  
- Training set size: **750,000 clients**; test set: **250,000**.  
- Features: age, job, marital status, education, balance, loan status, marketing campaign parameters (contact channel, month, contact duration, number of contacts, outcome of the previous campaign).  
- Target variable: deposit subscription (0 — no, 1 — yes).  
- Note: strong class imbalance (≈12% subscribers vs. 88% non-subscribers).

---
## Key project stages
1. **Loading and preprocessing** - structure analysis, handling categorical features
2. **EDA** - distribution analysis, identification of seasonality and target segments
3. **Feature Engineering** - creating business features, correlation analysis
4. **Model training** - comparing 4 algorithms, hyperparameter tuning
5. **Feature importance analysis** - interpreting the results
6. **Generating predictions** - preparing the submission for Kaggle
7. **Validation on original data** - checking model stability

---
## 📈 Results
- Full cycle completed: data loading → preprocessing → EDA → feature engineering → model training → submission generation.  
- The best result was achieved by the **LightGBM** model with ROC‑AUC = **0.9636**.  
- Key drivers of response were identified: contact duration, outcome of the previous campaign, month of the call, client balance.  
- Profiles of clients most likely to subscribe to a deposit were built.  
- Recommendations for optimizing the marketing strategy were provided.
- The project demonstrates skills in: EDA, feature engineering, hyperparameter tuning, handling class imbalance, and model interpretation.

The model can be used in a real bank to optimize marketing campaigns.

---
## 📁 Repository structure

`02_Kaggle_Playground_Series_Binary_Classification/`

```text
├── `Binary_Classification_with_BankDataset.ipynb`      — main notebook with full analysis  
├── `Binary_Classification_with_a_BankDataset.pdf`        — PDF export 
├── `requirements.txt`                                     — project dependencies 
└── `README.md`                                            — this documentation
```

---

## 🚀 How to run
1. Clone the repository:  
   ```bash
   git clone https://github.com/aspozd-DA-DS/DataScience_projects.git
   ```
2. Go to the project folder:

   ```bash
   cd DataScience_projects/02_Kaggle_Playground_Series_Binary_Classification
   ```

3. Run the notebook:

   ```bash
   jupyter notebook "Binary_Classification_with_BankDataset.ipynb.ipynb"
   ```
4. Make sure the Kaggle API is configured for automatic data download

## 🏷 Topics
`Data Analysis` `EDA` `Visualization` `Kaggle` `Python` `Machine Learning` `Classification` `Bank Marketing`  `lightgbm`  `xgboost`  `catboost` `feature-engineering` `roc-auc`

<p align="right"><a href="#top">⬆ back to top</a></p>
