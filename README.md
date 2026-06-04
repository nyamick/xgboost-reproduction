## О проекте

Данный проект выполнен в рамках учебной практики магистерской программы «Большие данные и интеллектуальные системы».

Цель работы - воспроизвести результаты статьи:

**Chen T., Guestrin C. (2016). XGBoost: A Scalable Tree Boosting System. KDD 2016.**

В работе выполнено:

* воспроизведение экспериментов статьи на датасете HIGGS;
* сравнение результатов с опубликованными в статье;
* исследование влияния гиперпараметров модели XGBoost;
* сравнение XGBoost и LightGBM на одной задаче классификации.



## Используемая статья

Chen T., Guestrin C.

**XGBoost: A Scalable Tree Boosting System**

Proceedings of the 22nd ACM SIGKDD International Conference on Knowledge Discovery and Data Mining (KDD 2016).

Ссылка:

https://arxiv.org/abs/1603.02754



## Датасет

Для экспериментов использовался датасет HIGGS.

Описание:

* задача бинарной классификации;
* 28 признаков;
* более 11 миллионов объектов;
* предсказание принадлежности физического события к классу Higgs Boson.

Источник:

https://archive.ics.uci.edu/ml/datasets/HIGGS



## Структура проекта

```text
project/
│
├── notebooks/
│   └── xgboost_reproduction.ipynb
│
├── figures/
│   ├── results.png
│
├── results/
│   └── results.csv
│
├── requirements.txt
├── LICENSE
└── README.md
```



## Установка

Создание виртуального окружения:

```bash
python -m venv venv
source venv/bin/activate
```

Установка зависимостей:

```bash
pip install -r requirements.txt
```



## Используемые библиотеки

* xgboost
* lightgbm
* scikit-learn
* pandas
* numpy
* matplotlib
* seaborn



## Запуск эксперимента

Запустить Jupyter Notebook:

```bash
jupyter notebook
```

Открыть файл:

```text
notebooks/xgboost_reproduction.ipynb
```

и выполнить все ячейки последовательно.



## Параметры воспроизведения

Для XGBoost использовались параметры из статьи:

* max_depth = 8
* learning_rate = 0.1
* n_estimators = 500
* colsample_bytree = 1.0
* subsample = 1.0

Метрика качества:

* ROC-AUC



## Дополнительные эксперименты

В рамках улучшения метода были проведены следующие исследования:

1. Влияние глубины дерева (max_depth).
2. Влияние learning rate.
3. Column subsampling (colsample_bytree = 0.5).
4. Сравнение XGBoost и LightGBM.



## Воспроизводимость

Для обеспечения воспроизводимости используется фиксированное значение:

```python
SEED = 42
```

Используемые версии библиотек указаны в файле requirements.txt.


## Автор

Денисенко А.С.

«Большие данные и интеллектуальные системы»

Иркутский государственный университет
