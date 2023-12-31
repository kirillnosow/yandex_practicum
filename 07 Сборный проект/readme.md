# Восстановление золота из руды

### Цели проекта 
Подготовьте прототип модели машинного обучения для «Цифры», которая поможет оптимизировать производство, чтобы не запускать предприятие с убыточными характеристиками.  
  
### Задачи проекта 
1. Открыть файлы и изучите их.
2. Проверить, что эффективность обогащения рассчитана правильно. Вычислить её на обучающей выборке для признака rougher.output.recovery. Найти MAE между вашими расчётами и значением признака.
3. Проанализировать признаки, недоступные в тестовой выборке.
4. Провести предобработку данных.
5. Посмотреть, как меняется концентрация металлов (Au, Ag, Pb) на различных этапах очистки.
6. Сравнить распределения размеров гранул сырья на обучающей и тестовой выборках. 
7. Исследовать суммарную концентрацию всех веществ на разных стадиях: в сырье, в черновом и финальном концентратах.
8. Написать функцию для вычисления итоговой sMAPE.
9. Обучить разные модели и оцените их качество кросс-валидацией. Выбрать лучшую модель и проверить её на тестовой выборке. 

### Данные
В распоряжении сырые данные: их просто выгрузили из хранилища.

### Выводы
- были обработаны пропуски;
- проверена формула вычисления эффективности обогащения на соответствие действительности;
- исследованы изменения концентрации элементов на каждом этапе очистки: после каждого этапа очистки концентрация золота значительно возрастает, концентрация серебра уменьшается, концентрация свинца значительно повысилась после флотации, при последующей очистке повышение не такое явное, суммарная концентрация металлов стабильно повышается после прохождения каждого этапа очистки;
- распределения размеров гранул сырья в выборках схожи, никаких корректировок вносить не требуется;
- обучены разные модели и оценено их качество кросс-валидацией и подсчётом метрики sMAPE (симметричное среднее абсолютное процентное отклонение);
- лучшей моделью оказалась RandomForestRegressor.
