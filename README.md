# Оптимизация термической деполимеризации (TDU)
# Thermal Depolymerization Optimization (TDU)

---

### Описание проекта

Исследовательский инженерный проект, посвящённый моделированию и анализу процесса
термической деполимеризации отходов (Thermal Depolymerization Unit, TDU).

Проект является ранней открытой итерацией работы стартапа в области переработки
пластика и биомассы в промежуточные нефтепродукты. Представленная версия отражает
первый этап — построение модели процесса и анализ факторов, влияющих на его
эффективность, в условиях отсутствия реальных промышленных данных.

---

### Контекст и постановка задачи

На момент начала проекта:

- отсутствовали промышленные датасеты;
- не было публичных масштабных реализаций технологии;
- доступная информация ограничивалась научными публикациями, патентами
  и описаниями лабораторных прототипов;
- технологические эксперты (химики, инженеры) были недоступны на старте.

Задача заключалась в том, чтобы **с нуля реконструировать процесс TDU** в виде
данной модели, пригодной для анализа и последующей оптимизации.

---

### Цели моделирования

Проект фокусируется на двух ключевых метриках процесса:

- **Выход масла** — литры полученного масла на килограмм исходного сырья  
- **Чистота масла** — доля целевого продукта без примесей

Обе метрики рассматриваются как функция:

- состава сырья (пластик, биомасса, металлы, электронные отходы);
- параметров процесса (температура, давление, pH, скорость потока);
- динамики сенсорных показателей во времени.

---

### Подход и методология

Проект построен как **инженерно-ориентированное моделирование процесса**, а не
как классическая ML-задача на готовых данных.

**Основные этапы:**

1. **Симуляция батчей сырья**
   - Формирование партий отходов с реалистичными пропорциями компонентов
   - Диапазоны параметров основаны на научных и индустриальных источниках

2. **Симуляция сенсорных данных**
   - Температура, давление, pH, скорость потока моделируются как временные ряды
   - Логика генерации отражает вариативность промышленного процесса

3. **Расчёт выходных метрик**
   - Выход масла оценивается через интеграцию потока во времени
   - Чистота масла корректируется с учётом побочных реакций и загрязнений

4. **Аналитика и ML-моделирование**
   - EDA и фичеинжиниринг
   - Модели: XGBoost, LightGBM, простые нейросетевые архитектуры
   - Анализ важности признаков (в том числе SHAP)

ML используется **как инструмент анализа**, а не как финальное оптимизационное решение.

---

### Моя роль в проекте

- Анализ научных и открытых индустриальных источников по TDU и пиролизу
- Проектирование логики симуляции данных с нуля
- Разработка структуры данных и пайплайна моделирования
- Полный блок анализа и машинного обучения
- Участие в формировании общей архитектуры данных и процесса

После данной версии проект был существенно расширен.
Финальная версия не публикуется по коммерческим причинам.

---

### Состав репозитория

- `TDU Process v2.ipynb` — исследовательский ноутбук:
  - симуляция данных;
  - аналитика;
  - ML-моделирование;
  - визуализации и интерпретация результатов.

Исходные данные в открытый доступ не выкладываются.

---

### Ограничения

- Используются симулированные данные
- Модель не является цифровым двойником промышленной установки
- Проект не является production-ready решением

---

### Статус проекта

Исследовательский прототип / ранняя итерация.

Проект демонстрирует работу на стыке инженерии, доменного ресёрча
и data science в условиях высокой неопределённости.

---

## English version

### Project Overview

This is an engineering research project focused on modeling and analyzing the
Thermal Depolymerization Unit (TDU) process.

The project represents an early open iteration of a startup working on waste
processing technologies for converting plastic and biomass into intermediate
oil-based products. The published version reflects the initial stage — process
modeling and analysis of key efficiency drivers in the absence of real
industrial data.

---

### Context and Problem Statement

At the start of the project:

- no industrial datasets were available;
- no large-scale public implementations existed;
- available information was limited to academic papers, patents,
  and laboratory-scale prototypes;
- domain experts (chemists, process engineers) were not available initially.

The goal was to **reconstruct the TDU process from scratch** as a data-driven
model suitable for analysis and further optimization.

---

### Modeling Objectives

The project focuses on two core performance metrics:

- **Oil Yield** — liters of oil produced per kilogram of input material  
- **Oil Purity** — proportion of usable oil without contaminants

Both metrics are modeled as functions of:

- feedstock composition (plastics, biomass, metals, electronic waste);
- process parameters (temperature, pressure, pH, flow rate);
- temporal dynamics of sensor signals.

---

### Approach and Methodology

This project follows an **engineering-driven process modeling approach**
rather than a classical ML task based on pre-existing data.

**Key stages:**

1. **Feedstock batch simulation**
   - Generation of waste batches with realistic component ratios
   - Parameter ranges derived from scientific and industrial literature

2. **Sensor data simulation**
   - Temperature, pressure, pH, and flow rate modeled as time series
   - Variability reflects non-ideal industrial operating conditions

3. **Output metric estimation**
   - Oil yield estimated via flow integration over time
   - Oil purity adjusted based on side reactions and contamination effects

4. **Analytics and ML modeling**
   - Exploratory data analysis and feature engineering
   - Models: XGBoost, LightGBM, simple neural network architectures
   - Feature importance analysis (including SHAP)

ML is used **as an analytical tool**, not as a final optimization solution.

---

### My Role

- Research and analysis of academic and open industrial sources on TDU and pyrolysis
- Design of the data simulation logic from scratch
- Development of data structures and modeling pipeline
- Full analytics and machine learning workflow
- Contribution to overall data and process architecture

Subsequent internal versions include extended feature engineering and improved models.
The final commercial implementation is not publicly available.

---

### Repository Contents

- `TDU Process v2.ipynb` — research notebook containing:
  - data simulation;
  - analytics;
  - ML modeling;
  - visualizations and interpretation.

Source data is not published due to commercial constraints.

---

### Limitations

- Simulated data is used
- The model is not a digital twin of an industrial installation
- The project is not production-ready

---

### Project Status

Research prototype / early iteration.

The project demonstrates problem formulation, engineering modeling,
and analytical reasoning under conditions of high uncertainty.

