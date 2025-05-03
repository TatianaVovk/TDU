# Оптимизация термической деполимеризации (TDU) 🛢️

Этот проект является частью стартапа, получившего грант на разработку решений в области переработки бытовых отходов и получения из них нефтепродуктов. Представленная здесь версия — это ранняя итерация исследования, направленного на анализ и повышение эффективности установки TDU (Thermal Depolymerization Unit), преобразующей пластик и биомассу в промежуточные виды топлива.

## 📌 Контекст

Проект моделирует работу TDU и нацелен на улучшение двух ключевых метрик:
- **Выход масла** — литры масла на кг сырья
- **Чистота масла** — процентное содержание целевого продукта без примесей

Работа велась в составе команды специалистов из различных областей таких как химия, инженерия и data science. 

## 🧠 Моя роль

Я участвовала:
- в поиске и анализе открытых и научных источников по технологии TDU
- в разработке симулированных датасетов (на основе индустриальных данных)
- полностью в блоке анализа и моделирования с помощью ML (EDA, фичи, модели)
- участвовала в разработке архитектуры данных и логики процессов

После этой версии был проведён расширенный фичеринжиниринг, переобучение моделей, улучшение нейросетевых решений. Полную версию по коммерческим причинам выкладывать не буду.

## 📁 Состав проекта

- `tdu_modeling.ipynb` — код анализа, визуализаций и моделей
- Данные не выкладываются в открытый доступ (по комерчиским причинам)

## 🔧 Методы и подходы

- Очистка и агрегация сенсорных данных (температура, давление, pH, flow rate)
- Симуляция полного процесса TDU с учетом химических реакций элементов
- Моделирование (XGBoost, LightGBM, нейросеть)
- Анализ важности признаков (SHAP и др.)

## ⚠️ Ограничения

- Использованы симулированные данные
- Финальная версия проекта содержит существенные улучшения и не является открытой


---

# Thermal Depolymerization Optimization (TDU) 🛢️

This project is part of a startup that received an initial grant for developing waste processing technology to convert household waste into valuable oil-based products. The version presented here is an early iteration aimed at modeling and improving the efficiency of a TDU (Thermal Depolymerization Unit), which transforms plastic and organic biomass into intermediate fuels.

## 📌 Context

The project focuses on improving two key performance metrics:
- **Oil Yield** — liters of oil per kg of input waste
- **Oil Purity** — percentage of clean, usable oil without contaminants

This work was carried out by a cross-functional team including chemists, engineers, and data scientists.

## 🧠 My Role

I contributed to:
- Researching and analyzing academic and open industrial sources on TDU
- Co-creating simulated datasets based on realistic processing parameters
- Leading the full ML block (EDA, feature engineering, modeling)
- Involved in develpoment of the data architecture and process logic

After this version, extensive improvements were made including deeper feature engineering, reworked models, and improved neural networks. The final version is not public due to commercial confidentiality.

## 📁 Project Content

- `tdu_modeling.ipynb` — main analysis, visualization and ML code
- Data is not published for confidentiality reasons

## 🔧 Methods & Approach

- Sensor data aggregation and cleaning (temperature, pH, pressure)
- Simulation of the entirety of the TDU process accounting for the chemical reactions of the involved elements
- ML modeling with XGBoost, LightGBM, and neural networks
- Feature importance analysis (SHAP and others)

## ⚠️ Limitations

- Simulated data was used
- Final commercial version includes improvements and remains private
