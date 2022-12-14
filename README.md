# Budget-Calculator-Python
Budget Calculator Python version 0.0.1

 Калькулятор бюджета
Калькулятор бюджета — это простое приложение Python, которое позволит вам рассчитать
свой бюджет.
Функции
    Храните свои расходы в виде файла любого типа (предпочтительно .csv). Это
    долгосрочное хранилище для ваших данных
    Получить расходы по категории (в целом, по месяцам)
    См. круговую диаграмму расходов в месяц по категориям
    Язык приложения русский, белорусский или английский (на ваш выбор)
Дизайн
Калькулятор бюджета будет использовать файл любого типа для хранения всех данных в
следующих столбцах:
    Категория
    Дата
    Количество
Категория
Столбец «Категория» определяет источник расходов (бар, кафе, продуктовый магазин,
аптеки, интернет-магазины). Определение этих категорий на вас. Вы можете определить
любое количество категорий и выбрать способ их хранения.
Свидание
Столбец «Дата» определяет конкретную дату, когда были произведены ваши расходы. Формат: ГГГГ-ММ-ДД
Подсказки: используйте библиотеку pyhon datetime
Дата поможет вам сгруппировать данные по отдельным месяцам. Библиотека datetime
позволит вам получить год и месяц расходов.
Количество
Столбец «Сумма» определяет денежную стоимость, которая была потрачена на определенную
категорию. Пример: Я потратил 20 BYN на продукты на рынке. Сумма = 20
Логику валюты можно определить самостоятельно. В противном случае можно просто
считать, что все траты осуществляются в валюте BYN и расширять логику в дальнейшем,
если хотите.
Пример
Сценарий:
1. Я потратил 20 BYN на продукты 20 мая.
2. Потратил 35 BYN на пиво в Лидбире 21 мая.
Результат
Выходной файл выглядит следующим образом:
   Категория, Дата, Сумма
Продукты,2022-05-20,20
Бар,2022-05-21,35

 Группа по
Как пользователь, я хочу иметь возможность получать расходы «по категориям» и «в
месяц». Вы можете использовать любую функциональность для реализации этой логики.
Итак, имея следующий файл:
 Категория, Дата, Сумма
Продукты,2022-05-20,20
Бар,2022-05-21,35
Алиэкспресс, 2022-06-21,60
Бар,2022-06-25,20
Бакалея,2022-06-02,120
Сценарии
GROUPBY КАТЕГОРИЯ
Я хочу иметь возможность получать свои расходы, например, по категории «Продукты».
  Категория, Дата, Сумма
Продукты,2022-05-20,20
Продукты,2022-06-02,120
GROUPBY МЕСЯЦ
Я хочу иметь возможность получать свои расходы по месяцам: 2022-05
 Категория, Дата, Сумма
Продукты,2022-05-20,20
Бар,2022-05-21,35
GROUPBY «МЕСЯЦ» И «КАТЕГОРИЯ»
Я хочу иметь возможность получать информацию о своих расходах по месяцам и категориям
продуктов: продукты, 2022–2005 гг.
 Категория, Дата, Сумма
Продукты,2022-05-20,20
Representation of output
Как пользователь, я хочу видеть результаты не в виде текста на консоли, а в виде
диаграммы:

   В этом вам поможет библиоткека matplotlib и следующий код:
 import matplotlib.pyplot as plt
labels = 'Groceries', 'Bar', 'Pharmacies', 'Pet', 'Transport'
sizes = [350, 70, 5, 60, 30]
fig1, ax1 = plt.subplots()
ax1.pie(sizes, labels=labels, autopct='%1.1f%%',
        shadow=True, startangle=90)
ax1.axis('equal')
plt.show()


 Budget calculator
Budget calculator is a simple Python application that will allow u to calculate your
budget
Features
    Store your spendings as file of any type (.csv preferred). It is a long-term
    storage for your data
    Get spendings for category (overall, by month)
    See pie chart for spendings per month by category
    Language of App is Russian, Belarusian or English (by your choise)
Design
Budget calculator will use file of any type to store all there data in the following
columns:
    Category
    Date
    Amount
Category
Category column defines source of spendings (Bar, cafe, groceries store, pharmacies, online-shopping). Definition of these categories is on you. You can define any number of categories and choose the way you will store them
Date
Date column defines particular date when your spendings were performed at. Format:
YYYY-MM-DD
Hints: use pyhon datetime library
Date will help you to group data by partivular month. datetime library will allow you to get year and month of spendings.
Amount
Amount column defines money value that was spent for particular category. Example: I spent 20 BYN for groceries in the market. Amount = 20
Currency' logic can be defined by yourself. Otherwise, you can just assume that all
spendings are performed in BYN currency and expand logic in the future if you want.
Example
Scenario:
1. I spent 20 BYN for groceries in the market on the 20th of May
2. I spent 35 BYN for beer in Leedbeer on the 21th of May
Result
Output file is the following:
      Category,Date,Amount
Groceries,2022-05-20,20
Bar,2022-05-21,35

 GroupBy
As a user, I want to be able to get spendings per category and per month . You can use any functionality to implement this logic. So, having the following file:
   Category,Date,Amount
Groceries,2022-05-20,20
Bar,2022-05-21,35
Aliexpress,2022-06-21,60
Bar,2022-06-25,20
Groceries,2022-06-02,120
Scenarios
GROUPBY CATEGORY
I want to be able to get my spendings by, for example, Groceries category.
   Category,Date,Amount
Groceries,2022-05-20,20
Groceries,2022-06-02,120
GROUPBY MONTH
I want to be able to get my spendings by Month: 2022-05
 Category,Date,Amount
Groceries,2022-05-20,20
Bar,2022-05-21,35
 GROUPBY MONTH AND CATEGORY
I want to be able to get my spendings by Month and Groceries category : Groceries,
2022-05
 Category,Date,Amount
Groceries,2022-05-20,20
Representation of output
As a user I want to be able to see results not as a text on console, but as a chart:

  This code should help you
 import matplotlib.pyplot as plt
# Pie chart, where the slices will be ordered and plotted counter-clockwise:
labels = 'Groceries', 'Bar', 'Pharmacies', 'Pet', 'Transport'
sizes = [350, 70, 5, 60, 30]
fig1, ax1 = plt.subplots()
ax1.pie(sizes, labels=labels, autopct='%1.1f%%',
shadow=True, startangle=90)
ax1.axis('equal') # Equal aspect ratio ensures that pie is drawn as a circle.
plt.show()
