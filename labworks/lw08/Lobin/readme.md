#Лабораторная работа №8 Лобина Михаила
##Задание 1
Две части, send_1.c и receive_1.c. Одна посылает, вторая принимает сообщение через очередь сообщений. Для удобства есть lab1.sh, к-я собирает их оба и запускает по очереди.
##Задание 2
Также две части, send_2.c и receive_2.c. Работает аналогично первой части, но с нетекстовыми данными. Также есть сборочный файл.
##Задание 3
Один файл, обменивается со своим потомком данными по первому и второму каналу сообщений, ничего интересного. Сборочного файла нет, растительности нет, населен зомби.
##Задание 4
Простой клиент-сервер аж из трех частей - server_4.c, client_4.c и kill_4.c. Сервер принимает запрос по первому каналу от клиента, отвечает по каналу равному pid клиента. Kill отправляет сигнал на завершение и выключение канала.
//я потратил довольно много времени, чтобы разобраться со stack smashing в этом и следующем задании
##Задание 5
Система семафоров (условная) из четырех частей - server_5.c, client_send_5.c, client_receive_5.c, kill_5.c. Клиент-приемник присылает серверу запрос на семафор на пять единиц, сервер запоминает это и его pid, клиент-отправитель отправляет запрос на плюс единицу в семафор, когда семафор равен нулю, сервер отвечает по каналу, равному pid, приемнику. Kill также убивает сервер с закрытием очереди.