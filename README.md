# Генерация ssl - Сертефиката
### !!! Предварительно должен быть сгененерирован корневой сертефикат

````bash
openssl genrsa -out rootCA.key 2048

openssl req -x509 -new -nodes -key rootCA.key -sha256 -days 1024 -out rootCA.pem
````
### Далее
````bash
./cert.sh my_domain_name
```` 