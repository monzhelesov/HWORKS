# Домашнее задание к занятию «Хранение в K8s» - Монжелесов Роман

## Задание 1

![url](https://github.com/monzhelesov/HWORKS/blob/main/1.png)

Манифест deployment: [deployment.yaml](deployment.yaml)

Манифест configmap: [configmap-web.yaml](configmap-web.yaml)


## Задание 2

![url](https://github.com/monzhelesov/HWORKS/blob/main/2.png)

Манифест secret: [secret-tls.yaml](secret-tls.yaml)

Манифест ingress: [ingress-tls.yaml](ingress-tls.yaml)


## Задание 3

![url](https://github.com/monzhelesov/HWORKS/blob/main/3.png)

```
1. Приватный ключ
openssl genrsa -out developer.key 2048

2. CSR (Certificate Signing Request)
openssl req -new -key developer.key -out developer.csr \
  -subj "/CN=developer"

3.openssl x509 -req -in developer.csr \
  -CA /var/snap/microk8s/current/certs/ca.crt \
  -CAkey /var/snap/microk8s/current/certs/ca.key \
  -CAcreateserial -out developer.crt -days 365
```

Манифест role-pod-reader: [role-pod-reader.yaml](role-pod-reader.yaml)

Манифест rolebinding-developer: [rolebinding-developer.yaml](rolebinding-developer.yaml)
