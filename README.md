# geo_coder
Scraping text data from sites, parsing geodata from Yandex-Geocoder.

Данный скрипт реализует парсинг координат по адресам из сервиса Яндекс.Геокодер. Доступ осуществляется по API. Для получения доступа к API необходимо зарегистрироваться на [сервисе](https://yandex.ru/dev/maps/geocoder/) и получить уникальный ключ. Бесплатная лицензия позволяет осуществить до 1000 запросов в день, месячное ограничение составляет 10000 запросов. 

Также реализована созможность отрисовки координат на карте для визуальной проверки корректности парсинга. 

<div id="map" align="center">
  <img src="https://github.com/nboravlev/geo_coder/blob/main/изображение_2023-07-30_122847890.png" alt=""/>
</div>


Скрипт использует библиотеки:
* Pandas - для получения данных их excel и преобразования в ДатаФрейм;
* Geopandas - для преобразования excel в geojson;
* Requests - для отправки запросов к сервису;
* Folium - для работы с координатами на карте.

Скрипт принимает документ в формате excel со списком адресов для парсинга. Полный адрес включает данные - страна-область-район-улица-дом, и возвращает документ excel, в котором адресу присваиваются его координаты. Далее с помощью библиотеки GeoPandas спискок координат можно преобразовать в geojson объект и вывести точки на карту.
