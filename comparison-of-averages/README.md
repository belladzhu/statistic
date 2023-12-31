## Мини-проект по A/B тесту
В проекте я работаю с данными приложения для курьеров крупной компании по доставке приложений пиццы. \
У компании есть несколько ресторанов в разных частях города и целый штат курьеров. Проблема — к вечеру скорость доставки падает из-за того, что курьеры уходят домой после рабочего дня, а количество заказов лишь растет. Это приводит к тому, что в момент пересмены доставка очень сильно проседает в эффективности. \
Был придуман новый алгоритм, который позволяет курьерам запланировать свои последние заказы перед окончанием рабочего дня так, чтобы их маршрут доставки совпадал с маршрутом до дома. То есть, чтобы курьеры доставляли последние свои заказы за день как бы "по пути" домой. \
Было решено раскатить A/B тест на две равные группы курьеров. Часть курьеров использует старый алгоритм без опции "по пути", другие видят в своем приложении эту опцию и могут ее выбрать.

### Цель проекта:
Проанализировать данные эксперимента и помочь бизнесу принять решение о раскатке новой фичи на всех курьеров.

Сравнение графиков распределения и экспериментальной группы:
![аб 2](https://github.com/belladzhu/statistic/assets/101130608/9742569c-6a43-4392-b56c-c2711821c24e)
![аб 1](https://github.com/belladzhu/statistic/assets/101130608/e1ae0b73-92c2-4a4d-9309-ee6fa3468b9a)

### Вывод
Для сравнения средних в данных экспериментальных группах я использовала Т-тест Стьюдента. Статистика в тесте равна -43, p-value <= 0.05.\
Следует раскатывать новую версию приложения, так как среднее время доставки статистически значимо изменилось. Среднее время доставки в тесте меньше, чем в контроле.
