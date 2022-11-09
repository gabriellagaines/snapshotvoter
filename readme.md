# snapshotvoter
Скрипт на node.js для off-chain голосования на snapshot.org
## Возможности
- Создание списка проползалов
- Поддержка множества приватных адресов
- На текущий момент поддержка только ```single-choice``` типа голосования
- Поддержка задержки между аккаунтами
- Поддержка рандомного выбора ответа
- Автоматическая подписка на проект
- Поддержка парсинга списка проползалов
## Необходимое ПО
- nodejs
- npm / yarn
## Установка
```
git clone https://github.com/sm1ck/snapshotvoter.git
npm i
```
## Настройка
В файле main.js ```rand_mode``` можно изменить на 1 для рандомного выбора ответа, оставить 0 для своего значения. Установите ```random_min``` и ```random_max``` если планируете использовать рандомное голосование. Для использования списка проползалов измените ```isPropList``` на true.

В файле keys.json создайте список приватников:
```
"приватный_ключ_1",
"приватный_ключ_2"
```
В файле props.json создайте список проползалов, если хотите кастомный список с ```isPropList``` в true:
```
"0xfeb1832a75e2ef47dea4b08509a16e4e9176e9d2a962c9466c5d345b37428384",
"0x2a7436c5bebeaee1a369e484a212a183da549dfce0393d6dc1f84837e8c5c79d"
```
## Запуск
```
node main.js <название_проекта> <айди_проползала> <номер_варианта>
```
Название проекта - скопировать из строки, например https://snapshot.org/#/arbitrum-odyssey.eth

arbitrum-odyssey.eth - это то, что нам нужно

Айди проползала - скопируйте из браузера, например https://snapshot.org/#/arbitrum-odyssey.eth/proposal/0x44aba87414d2d7ce88218b676d9938338d7866a245f48a7829e805a99bcda6a2

хеш 0x44aba87414d2d7ce88218b676d9938338d7866a245f48a7829e805a99bcda6a2 - айди
```
node main.js <название_проекта> getprops
```
Сохранить список активных проползалов в файл props.json. Для использования списка не забудьте изменить значение переменной ```isPropList``` в true.
## Автор
Автор Jancrypto (telegram)

Donate: 0x9D278054C3e73294215b63ceF34c385Abe52768B