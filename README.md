# Нейросетевой анализатор сетевого трафика
## Настройка рабочего окружения
Установку необходимых пакетов и среды разработки рекомендуется выполнять
в Anaconda (работа выполнялась и тестировалась на anaconda3). Скачать установочный
файл Anaconda можно с официального сайта.

Anaconda сразу содержит в себе среду разработки Jupyter.
Если же Jupyter не установлен в Anaconda, установить можно
при помощи следующей команды:
```
> conda install jupyter
```

Для запуска Jupyter Notebook можно использовать следущую команду:
```
> jupyter notebook
```

Также для работы кода понадобится Wireshark или Tshark.
## Установка необходимых пакетов
Обычно Anaconda уже после установки имеет в себе все необходимые для
запуска пакеты кроме TensorFlow. Установить TensorFlow можно при помощи команды
```
> pip install tensorflow
```
## Скачивание датасета
Данный код работает с датасетом IOT NETWORK INTRUSION DATASET, архив с которым **iot_intrusion_dataset.zip**
можно скачать по ссылке <https://ieee-dataport.org/open-access/iot-network-intrusion-dataset>. Там же можно
найти файл **dataset_description.xlsx**, который понадобится для фильтрации пакетов.

## Фильтрация пакетов
Для обработки и обучения используются два типа файлов: с атаками и без. Чтобы получить эти файлы из скачанного
датасета, необходимо отфильтровать пакеты при помощи Wireshark и файла **dataset_description.xlsx**, в котором 
есть фильтры Wireshark для получения пакетов с теми или иными атаками из **".pcap"**-файлов.

## Запуск нейросети
Когда пакеты сетевого трафика датасета отфильтрованы, можно запускать нейросеть! Необходимые для корректной работы
изменения кода описаны в комментариях в блокноте Jupyter. Исходный код написан на языке **Python 3**.
