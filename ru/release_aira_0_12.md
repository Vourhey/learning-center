## Работа с релизом AIRA 0.12

### Создание нового маяка

> Только если нужен новый маяк. Можно подключиться к уже существующему

Переходим на страницу [robonomics.network/net](https://robonomics.network/net/) и нажимает "create your own". Необходимо будет подтвердить транзакцию и вы увидите адрес нового маяка в списке.

![Create a lighthouse](/img/aira012/Screenshot_1.png "Создаем новый маяк")

### Получение образа

Релиз размещен на [Github](https://github.com/airalab/aira/releases/tag/0.12). Качаем образ для виртуальной машины.

![Obtain vm](/img/aira012/Screenshot_2.png "Получаем образ")

### Запуск образа

Дальше действия описываются на примере VirtualBox:
* Импортируем скачанный образ `Ctrl+I`
* Выделяем 2Гб оперативной памяти 
* В настройках сети меняем NAT на Bridge

![Importing](/img/aira012/Screenshot_3.png "Импортируем в VirtualBox")

После запуска AIRA будет синхронизироваться с сетью Kovan. Необходимо дождаться окончания и предложения отправить ETH и XRT

![Syncing](/img/aira012/Screenshot_4.png "Конец синхронизации")

Для удобства можно воспользоваться сервисом [Robonomics faucet](https://robonomics.network/faucet/). В поле ввода вставляем адрес и ждем поступления средств на счет клиента AIRA. 

Следующий шаг - выбор маяка:
![Choose a lighthouse](/img/aira012/Screenshot_5.png "Выбор маяка")

после этого AIRA приступит к сборке дистрибутива и переходу к следующему поколению. Когда этот процесс звершится, можно перезагружаться. AIRA готова к работе!

### Полезные команды

Просмотр состояния parity:
```
journalctl -u parity -f
```

Подключенные пиры IPFS:
```
ipfs swarm peers
```

