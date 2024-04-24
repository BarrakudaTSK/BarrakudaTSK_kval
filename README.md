# BarrakudaTSK_kval

https://www.youtube.com/watch?v=603pRVXm654

https://youtu.be/jxWhf9cxrTI

Этапы:
1. Везде установить visual
2. Sql na net1 - open
3. ЦУС сервер на net1 - admin
4. ЦУС клиент на net1 - open
5. Установить на net1 - openCA (5-ть программ)

Как запускать программы: 
Заходим в Powershell от имени администратора, далее пишем start (путь к программе, а также добавляем \WINNCCSL.MSI)

ip (Admin, open, openCA - 1.2.3.0-3) / default gateway 1.2.3.5 / maska 255.255.255.240

ip (Client - 2.3.4.0-3) / defaul gateway 2.3.4.5 / maska 255.255.255.224

Действия: 
1. Отключить везде Брандмауэр, затем изменить tcp (internet), откатить дату на прошлый год (2023)
2. Зайти в Панель управления\Все элементы панели управления\Центр управления сетями и общим доступом\Дополнительные параметры общего доступа и всё перевести в включено
3. Проверить адаптеры


Выполнить в Net1 - Open

Заходим в A7 - SOFT - ____000 - SERVER - PACKEDJ - VISUAL C / Ребут окна

Заходим в A7 - SOFT - ____000 - SERVER - PACKEDJ - SQL второй файл и лучше выложить на рабочий стол
  - Named (WINNCCSQL)
  - поставить Автоматический тип
  - пароль на администратор (xxXX1234)
  - filestream поставить галочки на вкл

Заходим на Sql сервер, включаем tcp, а также производим Restart

Заходим в A7 - SOFT - ____000 - CLIENT - PACKEDJ - RU-RU последний файл через POWERSHELL

Не забываем, что при запуске ЦУС, мы вводим ip от Net1 - Admin
  - Administrator / Administrator
  - Ключи находяться в директории f-7 - vipnet license (папка сеть 2)

Выполнить в  Net1 - Admin 

Заходим в A7 - SOFT - ____000 - SERVER - PACKEDJ - VISUAL C / Ребут окна

Заходим в A7 - SOFT - ____000 - SERVER - PACKEDJ - RU-RU последний файл через POWERSHELL  (После установления sql на Open)
  - пишем ip от Net1 - Open
  - sa / xxXX1234

Заходим в A7 - SOFT - _______ - SETUP

Заходим в C5 - SOFT - CLIENT

Запускаем УКЦ - новую базу данных - записываем ip net1 - admin > sa / xxXX1234 > ставим свой пароль

Выполнить в Net1 - OpenCA

Заходим в A7 - SOFT - ____000 - SERVER - PACKEDJ - VISUAL C / Ребут окна

Далее производим установку программ:
  - vipnetC
  - vipnetr629 - ______ - SOFT - SETUP
  - vipnetp6 - ______ - SOFT - SETUP
  - vipnetc5 - SOFT - CLIENT_R

Выполнить в Net2 - Client

Заходим в A7 - SOFT - ____000 - SERVER - PACKEDJ - VISUAL C / Ребут окна

Заходим в C5 - SOFT - CLIENT_R
