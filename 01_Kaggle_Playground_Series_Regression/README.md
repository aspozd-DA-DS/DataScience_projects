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
├── `Predicting the Beats-per-Minute of Songs.pdf`    — экспорт в PDF  
├── `requirements.txt`                                — зависимости проекта
└── `README.md`                                       — эта документация
```

---
## 🚀 Как запустить
1. Склонировать репозиторий:  
   ```bash
   git clone https://github.com/aspozd-DA-DS/DataScience_projects.git
2. Перейти в папку проекта:

   ```bash
   cd DataAnalytics_projects/01_Kaggle_Playground_Series_Regression

3. Запустить ноутбук:

   ```bash
   jupyter notebook Predicting the Beats-per-Minute of Songs.ipynb
4. Убедитесь, что у вас настроен Kaggle API для автоматической загрузки данных
   
## 🏷 Topics
`Data Analysis` `EDA` `Visualization` `Kaggle` `Python` `Machine Learning` `Regression` `Music Data` `audio-analysis` `lightgbm` `xgboost` `catboost`




