# Домашнее задание к занятию 14 «Средство визуализации Grafana»

## Задание повышенной сложности

**При решении задания 1** не используйте директорию [help](./help) для сборки проекта. Самостоятельно разверните grafana, где в роли источника данных будет выступать prometheus, а сборщиком данных будет node-exporter:

- grafana;
- prometheus-server;
- prometheus node-exporter.

За дополнительными материалами можете обратиться в официальную документацию grafana и prometheus.

В решении к домашнему заданию также приведите все конфигурации, скрипты, манифесты, которые вы 
использовали в процессе решения задания.

**При решении задания 3** вы должны самостоятельно завести удобный для вас канал нотификации, например, Telegram или email, и отправить туда тестовые события.

В решении приведите скриншоты тестовых событий из каналов нотификаций.

## Обязательные задания

### Задание 1

1. Используя директорию [help](./help) внутри этого домашнего задания, запустите связку prometheus-grafana.
<p align="center">
    <img width="1200 height="600" src="/scr/grafana_docker_up.png">
</p>

2. Зайдите в веб-интерфейс grafana, используя авторизационные данные, указанные в манифесте docker-compose.
<p align="center">
    <img width="1200 height="600" src="/scr/grafana_login.png">
</p>

3. Подключите поднятый вами prometheus, как источник данных.
<p align="center">
    <img width="1200 height="600" src="/scr/grafana_datasource1.png">
</p>

4. Решение домашнего задания — скриншот веб-интерфейса grafana со списком подключенных Datasource.
<p align="center">
    <img width="1200 height="600" src="/scr/grafana_datasource2.png">
</p>


## Задание 2

Изучите самостоятельно ресурсы:

1. [PromQL tutorial for beginners and humans](https://valyala.medium.com/promql-tutorial-for-beginners-9ab455142085).
2. [Understanding Machine CPU usage](https://www.robustperception.io/understanding-machine-cpu-usage).
3. [Introduction to PromQL, the Prometheus query language](https://grafana.com/blog/2020/02/04/introduction-to-promql-the-prometheus-query-language/).

Создайте Dashboard и в ней создайте Panels:

- утилизация CPU для nodeexporter (в процентах, 100-idle);
<p align="center">
    <img width="1200 height="600" src="/scr/grafana_CPU.png">
</p>

- CPULA 1/5/15;
<p align="center">
    <img width="1200 height="600" src="/scr/grafana_CPULA.png">
</p>

- количество свободной оперативной памяти;
<p align="center">
    <img width="1200 height="600" src="/scr/grafana_ram.png">
</p>

- количество места на файловой системе.
<p align="center">
    <img width="1200 height="600" src="/scr/grafana_fs.png">
</p>

Для решения этого задания приведите promql-запросы для выдачи этих метрик, а также скриншот получившейся Dashboard.
<p align="center">
    <img width="1200 height="600" src="/scr/grafana_dashboard.png">
</p>


## Задание 3

1. Создайте для каждой Dashboard подходящее правило alert — можно обратиться к первой лекции в блоке «Мониторинг».
2. В качестве решения задания приведите скриншот вашей итоговой Dashboard.
<p align="center">
    <img width="1200 height="600" src="/scr/grafana_alerts.png">
</p>

<p align="center">
    <img width="1200 height="600" src="/scr/grafana_channel.png">
</p>

<p align="center">
    <img width="1200 height="600" src="/scr/grafana_dashboard_alerts.png">
</p>


## Задание 4

1. Сохраните ваш Dashboard.Для этого перейдите в настройки Dashboard, выберите в боковом меню «JSON MODEL». Далее скопируйте отображаемое json-содержимое в отдельный файл и сохраните его.
2. В качестве решения задания приведите листинг этого файла.

**[dashboard.json](./Dashboard.json)**
---


### Как оформить решение задания

Выполненное домашнее задание пришлите в виде ссылки на .md-файл в вашем репозитории.

---
