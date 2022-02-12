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
Инициируем контейнер под версией 2.0:
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