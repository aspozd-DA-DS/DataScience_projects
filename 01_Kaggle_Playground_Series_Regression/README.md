<a id="top"></a>

<p align="right">
  <a href="#ru">🇷🇺 RU</a> | <a href="#en">🇬🇧 EN</a>
</p>

---

<a id="ru"></a>

# ML‑модель для прогнозирования темпа (BPM) музыкальных треков

## 📌 Описание
Проект выполнен в рамках соревнования [Kaggle Playground Series — Season 5, Episode 9](https://www.kaggle.com/competitions/playground-series-s5e9).  
Цель — построить модель машинного обучения, способную предсказывать количество ударов в минуту (BeatsPerMinute, BPM) для музыкальных треков на основе их акустических и композиционных характеристик.

BPM — ключевой параметр в музыкальной индустрии:
- классификация жанров,
- создание плейлистов,
- DJ-инг,
- подбор музыки под ритм тренировок,
- рекомендательные системы.

Практическая ценность:
- Автоматическое определение темпа треков для музыкальных стриминговых сервисов (Spotify, Apple Music).  
- Использование в DJ‑приложениях и фитнес‑сервисах для подбора музыки под ритм тренировки.  
- Улучшение рекомендательных систем за счёт анализа ритмических характеристик.

---

## 🔧 Стек технологий
- Python  
- pandas, numpy
- matplotlib, seaborn 
- phik(корреляционный анализ), scipy.stats
- Feature Engineering: создание взаимодействий, полиномиальных признаков, категоризация
- scikit‑learn (Linear Regression, Ridge, Lasso, Decision Tree)  
- LightGBM, XGBoost, CatBoost
- Оптимизация: GridSearchCV для подбора гиперпараметров
- Kaggle API для автоматической загрузки данных
  
---

## 📊 Данные
- Датасет синтетически сгенерирован на основе [BPM Prediction Challenge](https://www.kaggle.com/datasets/gauravduttakiit/bpm-prediction-challenge).  
- Размер обучающей выборки: **524 000+ треков**.  
- Признаки: RhythmScore, AudioLoudness, VocalContent, AcousticQuality, InstrumentalScore, LivePerformanceLikelihood, MoodScore, TrackDurationMs, Energy.  
- Целевая переменная: BeatsPerMinute.

---

## Ключевые этапы проекта
1. **Загрузка и предобработка** - анализ структуры, проверка пропусков
2. **EDA** - распределения, корреляции, выявление артефактов данных
3. **Feature Engineering** - создание 15+ новых признаков
4. **Обучение моделей** - сравнение 8 алгоритмов, подбор гиперпараметров
5. **Анализ ошибок** - диагностика предсказаний, остатки
6. **Формирование submission** - подготовка файла для Kaggle

---

## 📈 Результаты
- Проведён полный цикл: загрузка данных → предобработка → EDA → feature engineering → обучение моделей → формирование submission.
- Датасет синтетический и не содержит статистически значимых зависимостей.
- Базовые линейные модели показали низкое качество (RMSE ≈ 26.5).  
- Лучший результат достигнут с LightGBM, но из‑за синтетической природы данных модели предсказывают среднее значение BPM.  
- Вывод: для повышения качества требуется работа с реальными музыкальными данными.

Реальная польза проекта — демонстрация навыков EDA, feature engineering и построения ML-моделей.

---
## 📁 Структура репозитория

`01_Kaggle_Playground_Series_Regression/`

```text
├── `Predicting the Beats-per-Minute of Songs.ipynb`  — основной ноутбук с полным анализом  
├── `Predicting_the_Beats-per-Minute_of_Songs.pdf`    — экспорт в PDF  
├── `requirements.txt`                                — зависимости проекта
└── `README.md`                                       — эта документация
```

---
## 🚀 Как запустить
1. Склонировать репозиторий:  
   ```bash
   git clone https://github.com/aspozd-DA-DS/DataScience_projects.git
   ```
2. Перейти в папку проекта:

   ```bash
   cd DataScience_projects/01_Kaggle_Playground_Series_Regression
   ```

3. Запустить ноутбук:

   ```bash
   jupyter notebook Predicting the Beats-per-Minute of Songs.ipynb
   ```
4. Убедитесь, что у вас настроен Kaggle API для автоматической загрузки данных

## 🏷 Topics
`Data Analysis` `EDA` `Visualization` `Kaggle` `Python` `Machine Learning` `Regression` `Music Data` `audio-analysis` `lightgbm` `xgboost` `catboost`

<p align="right"><a href="#top">⬆ наверх</a></p>

---

<a id="en"></a>

# ML model for predicting track tempo (BPM)

## 📌 Description
This project was completed as part of the [Kaggle Playground Series — Season 5, Episode 9](https://www.kaggle.com/competitions/playground-series-s5e9) competition.  
The goal is to build a machine learning model that predicts the number of beats per minute (BeatsPerMinute, BPM) of music tracks based on their acoustic and compositional characteristics.

BPM is a key parameter in the music industry:
- genre classification,
- playlist creation,
- DJing,
- choosing music to match workout rhythm,
- recommender systems.

Practical value:
- Automatic tempo detection for music streaming services (Spotify, Apple Music).  
- Use in DJ apps and fitness services to select music matching a workout's rhythm.  
- Improving recommender systems by analyzing rhythmic characteristics.

---

## 🔧 Tech stack
- Python  
- pandas, numpy
- matplotlib, seaborn 
- phik (correlation analysis), scipy.stats
- Feature Engineering: creating interactions, polynomial features, categorization
- scikit-learn (Linear Regression, Ridge, Lasso, Decision Tree)  
- LightGBM, XGBoost, CatBoost
- Optimization: GridSearchCV for hyperparameter tuning
- Kaggle API for automatic data download
  
---

## 📊 Data
- The dataset was synthetically generated based on the [BPM Prediction Challenge](https://www.kaggle.com/datasets/gauravduttakiit/bpm-prediction-challenge).  
- Training set size: **524,000+ tracks**.  
- Features: RhythmScore, AudioLoudness, VocalContent, AcousticQuality, InstrumentalScore, LivePerformanceLikelihood, MoodScore, TrackDurationMs, Energy.  
- Target variable: BeatsPerMinute.

---

## Key project stages
1. **Loading and preprocessing** - structure analysis, missing value checks
2. **EDA** - distributions, correlations, detection of data artifacts
3. **Feature Engineering** - creating 15+ new features
4. **Model training** - comparing 8 algorithms, hyperparameter tuning
5. **Error analysis** - prediction diagnostics, residuals
6. **Submission generation** - preparing the file for Kaggle

---

## 📈 Results
- Full cycle completed: data loading → preprocessing → EDA → feature engineering → model training → submission generation.
- The dataset is synthetic and contains no statistically significant dependencies.
- Baseline linear models showed low quality (RMSE ≈ 26.5).  
- The best result was achieved with LightGBM, but due to the synthetic nature of the data, the models essentially predict the mean BPM value.  
- Conclusion: improving quality requires working with real music data.

The real value of the project is demonstrating skills in EDA, feature engineering, and building ML models.

---
## 📁 Repository structure

`01_Kaggle_Playground_Series_Regression/`

```text
├── `Predicting the Beats-per-Minute of Songs.ipynb`  — main notebook with full analysis  
├── `Predicting_the_Beats-per-Minute_of_Songs.pdf`    — PDF export  
├── `requirements.txt`                                — project dependencies
└── `README.md`                                       — this documentation
```

---
## 🚀 How to run
1. Clone the repository:  
   ```bash
   git clone https://github.com/aspozd-DA-DS/DataScience_projects.git
   ```
2. Go to the project folder:

   ```bash
   cd DataScience_projects/01_Kaggle_Playground_Series_Regression
   ```

3. Run the notebook:

   ```bash
   jupyter notebook Predicting the Beats-per-Minute of Songs.ipynb
   ```
4. Make sure the Kaggle API is configured for automatic data download

## 🏷 Topics
`Data Analysis` `EDA` `Visualization` `Kaggle` `Python` `Machine Learning` `Regression` `Music Data` `audio-analysis` `lightgbm` `xgboost` `catboost`

<p align="right"><a href="#top">⬆ back to top</a></p>
