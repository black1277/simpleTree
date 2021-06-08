### Запускаем в режиме ожидания изменений компилятор TypeScript
```javascript
tsc -p ./src/server -w
```
### Запускаем nodemon в режиме ожидания изменений js файлов
```javascript
nodemon ./dist/server/server.js
```
### При помощи concurrently запускаем все одной командой
```javascript
concurrently -k "tsc -p ./src/server -w" "nodemon ./dist/server/server.js"
```
### Укладываем все в запуск скрипта в package.json
```javascript
"dev" : "concurrently -k \"tsc -p ./src/server -w\" \"nodemon ./dist/server/server.js\"",
```
### Запускаем скрипт
```javascript
 npm run dev 
```
