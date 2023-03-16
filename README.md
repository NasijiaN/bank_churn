# Описание проекта "Отток клиентов"

Заказчиком данного исследования является банк "Бета-банк".

**Цель исследования** - спрогнозировать вероятность оттока клиентов банка в ближайшее время с помощью обученной модели.

В данной работе для достижения поставленной цели были применены следующие модели: 

* Дерево решений 
* Случайный лес 
* Логистическая регрессия 

## Ход исследования

Перед исследованием и применением моделей были почищены данные: избавились от пропущенных значений и проверили данные на наличие дубликатов, а также преобразовали категориальные переменные в числовые функцией pd.get_dummies и масштабировали данные методом StandardScaler.

При применении моделей в данных наблюдался дисбаланс, большинство ответов были негативными и из-за чего модели не проходили проверку адекватности. Устранили данную проблему методом upsample, увеличив долю позитивных ответов в 4 раза.

## Вывод 

Благодаря устранению дисбаланса в дальнейшем модели выдавали результаты лучше. Наиболее высокие результаты показала модель "Случайный лес", поэтому мы ее использовали в дальнейшем нашем исследовании.

Для того, чтобы увеличить качество модели "Случайный лес" мы перебрали значения нескольких гиперпараметров. Таким образом, получили следующие результаты по метрикам:

* Полнота ~ 0.70
* Точность ~ 0.51
* F1 ~ 0.59
* Auc_roc ~ 0.84
