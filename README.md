# Генерация ssl - Сертефиката
### !!! Предварительно должен быть сгененерирован корневой сертефикат

````shell
openssl genrsa -out rootCA.key 2048

openssl req -x509 -new -nodes -key rootCA.key -sha256 -days 1024 -out rootCA.pem
````
### Далее
````shell
./cert.sh my_domain_name
```` 