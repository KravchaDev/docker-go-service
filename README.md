#  docker-go-service
![lic](https://img.shields.io/github/license/Kravchadev/session_practice) ![lic](https://img.shields.io/github/downloads/Kravchadev/session_practice/total)

Простой веб-сервис обернутый в Docker-контейнер

### Освоенные навыки
- docker
- golang
- http
- vim

### Как начать работу
Входим в директорию проекта
```
$ cd docker-go-service
```
Устанавливаем Golang на машину (не обязательно, для теста кода, если смените какие-то строки):
```
$ sudo apt-get install go-golang
```
Устанавливаем Docker:
```
$ sudo apt-get install docker.io 
```
Инициируем контейнер под версией 0.1:
```
$ docker build . -t go:v0.1
```
Проверяем созданный образ:
```
$ docker images
```

Запускаем наш первый веб-сервис:
```
$ docker run go:v0.1
$ docker run -d -p 8080:8080 go:v0.1
```
Отслеживать майнинг можно по адресу ```localhost:8080/{сюда вписать любое слово} ``` 

```http://localhost:8080/Docker```
![](https://habrastorage.org/webt/xg/7f/fz/xg7ffz4pwxg9q8uw36osshgyb5c.png)

```http://localhost:8080/Docker```
![](https://habrastorage.org/webt/_t/ko/d0/_tkod0julagrs82h7fuzsza7dqa.png)

## Примечание
Данный образ Docker будет весить в 70 раз меньше, чем стандартный, так как компиляция кода Go происходит в AlpineLinux.

![](https://habrastorage.org/webt/yc/fw/vi/ycfwviarlzk6wovcwlebd4mnxxw.png)

```v0.1``` - стандартный Docker образ с полной установкой Golang. (время сборки 3-4 мин.)

```v0.2``` и ```v0.3``` - Docker образ с созданием бинарника и запуском кода, использую легковесный Alpine 
