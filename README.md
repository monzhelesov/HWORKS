# Домашнее задание к занятию «Хранение в K8s» - Монжелесов Роман

## Задание 1

![url](https://github.com/monzhelesov/HWORKS/blob/main/1.png)
![url](https://github.com/monzhelesov/HWORKS/blob/main/2.png)

Манифест deployment: [containers-data-exchange.yaml](containers-data-exchange.yaml)


## Задание 2

![url](https://github.com/monzhelesov/HWORKS/blob/main/3.png)
![url](https://github.com/monzhelesov/HWORKS/blob/main/4.png)
![url](https://github.com/monzhelesov/HWORKS/blob/main/5.png)
![url](https://github.com/monzhelesov/HWORKS/blob/main/6.png)

После удаления deployment и pvc, pv перейдет в статус released (было bound) это означает, что pvc удален, но данные сохранились.

После удаления pv данные также сохранились так как pv - это только обьект k8s; также у нас стояла политика retain, что не дает трогать данные на диске, данные удаляются только вручную администратором.

Манифест deployment: [pv-pvc.yaml](pv-pvc.yaml)


## Задание 3

![url](https://github.com/monzhelesov/HWORKS/blob/main/7.png)

Манифест deployment: [sc.yaml](sc.yaml)