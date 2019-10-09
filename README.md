# terraform-container-optimzed-image

Это тестовый ресурс для конфигурации Container Optimized Image.

#Конфигурация
* Подставьте свой публичный ssh ключ вместо "your public ssh key" в cloud_config.yaml
* Подставьте свой token вместо "your YC_TOKEN" в main.tf
* Подставьте свой folder_id вместо "your folder id" в main.tf
* Подставьте свою zone вместо "your zone" в main.tf
* Подставьте свою subnet_id вместо "your subnet id" в main.tf

#Запуск
* Запустите ```terraform plan```, потом ```terraform apply```
* В outputs будет выведено:
```
  Outputs:

  external_ip = <some_IPv4>
``` 
* Зайдите на публичный IPv4 адрес: ```ssh yc-user@<some_IPv4>```
* Сделайте ```curl <some_IPv4>```, в ответ должно быть:
```
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta http-equiv="refresh" content="3">
        <title>Yandex.Scale</title>
    </head>
    <body>
    <h1>Hello v1</h1>
    </body>
    </html>
```