# Домашнее задание к занятию «Средство визуализации Grafana» - Монжелесов Роман

### Задание 1

![image](https://github.com/monzhelesov/HWORKS/blob/main/11.png)

### Задание 2

![image](https://github.com/monzhelesov/HWORKS/blob/main/12.png)\

> 1. CPU utilization\
100 - (
  avg by (instance) (
    rate(node_cpu_seconds_total{mode="idle"}[5m])
  ) * 100
)

> 2. CPU Load Average 1/5/15\
node_load1
node_load5
node_load15

> 3. Memory RAM\
node_memory_MemAvailable_bytes

> 4. Storage\
node_filesystem_avail_bytes{mountpoint="/",fstype!="tmpfs"}

### Задание 3

![image](https://github.com/monzhelesov/HWORKS/blob/main/13.png)
![image](https://github.com/monzhelesov/HWORKS/blob/main/133.png)

### Задание 4

Файл лежит вместе с домашкой под названием dashboard.json