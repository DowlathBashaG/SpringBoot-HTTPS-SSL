# SpringBoot-HTTPS-SSL

## Generate KeyStore Certificate

- Command : C:\Users\aDMIN>keytool -genkey -alias https-example -storetype JKS -keyalg RSA -keysize 2048 -validity 365 -keystore https-example.jks

![gener_cert](https://user-images.githubusercontent.com/9671419/87206100-a3a69b80-c326-11ea-872b-6dd4adfd1428.PNG)

## application.property [ Override server port with 8443 ]

server.port=8443

server.ssl.key-alias=https-example

server.ssl.key-store-type=JKS

server.ssl.key-password=password

server.ssl.key-store=classpath:https-example.jks

## Copy keystore JKS file under the resource

![CopyTheJKS_under resources](https://user-images.githubusercontent.com/9671419/87206107-a6a18c00-c326-11ea-94c7-c48c39519b5d.PNG)

## Access the URL's 

without https:

http://localhost:8443/hello

![cer_1](https://user-images.githubusercontent.com/9671419/87206102-a4d7c880-c326-11ea-8dc9-2cb35153a141.PNG)

with https

https://localhost:8443/hello

![cer_2](https://user-images.githubusercontent.com/9671419/87206103-a5705f00-c326-11ea-8fd5-4bf3a4e535aa.PNG)

![cer_3](https://user-images.githubusercontent.com/9671419/87206104-a5705f00-c326-11ea-87f1-e0f974668ce8.PNG)

![cer_4](https://user-images.githubusercontent.com/9671419/87206106-a608f580-c326-11ea-9663-58bc33c642bc.PNG)
