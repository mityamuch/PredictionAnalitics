# ЛР2. Виртуальный датчик для контроля процесса обжига

## Что внутри
- `LR2_VirtualSensor.ipynb` — Jupyter Notebook с полным пайплайном: EDA → синхронизация с задержкой → признаки (lags/rolling/производные) → обучение минимум 3 моделей → метрики и анализ остатков → интерпретация.
- `requirements.txt` — зависимости для окружения Python.

## Данные
Должны лежать в той же папке:
- `data_train.csv`
- `target_train.csv`

> Тестовые файлы `data_test_small.csv/target_test_small.csv` в репозитории не предоставлены, поэтому в ноутбуке используется time-based holdout внутри `*_train.csv`.

## Как запустить
1. Установите зависимости:
   - `pip install -r requirements.txt`
2. Откройте ноутбук:
   - запустите `jupyter notebook`
   - откройте `LR2_VirtualSensor.ipynb`
3. Выполните все ячейки по порядку.

## Что смотреть в конце
- Таблица `res_df` с метриками (`MAE`, `RMSE`, `MAPE`, `WAPE`, `directional_acc`) и временем обучения/предсказания.
- Блок анализа остатков (нормальность, Ljung-Box, Breusch-Pagan).
- Визуализации остатков и “forecast vs real” на holdout-сегменте.
