OpenWeather data to Elasticsearch
=================================

This is small self-educational project to get familiar with Elasticsearch.
The aim is to get data from *openweathermap.org* and store it as time series in Elasticsearch.
It consists mainly of two files:

- `openwheather/elk_idx_create.py` creates index with adequate mapping and number of replicas set to 0 for test purposes.
- `openwheather/owfilter.py` is meant to run periodically to do actual job.

Personally, I set up testing Elasticsearch with Ansible role 
debops.elasticsearch, so there is sample inventory in the 
`ansible` directory.

Also, there's additional files, which could help:

- `openweather/openweather.json` sample output from OpenWeather
- `openweather/openweather.descr` description of fields returned by OpenWeather

I intentionally avoided using third-party modules, such as Requests, but rely
only on standard library. 

Disclaimer
----------

This is *proof-of-concept* project. There is no guarantee that it is useful for any purpose. But there IS guarantee
that it contains some errors or nonsense. Use at your own risk.


Requirements
------------

You must get API key from *openweathermap.org* (registration required). 
Put it in .token file alongside owfilter.py script or OW_API_TOKEN environment 
variable. Also, you obviously need running Elasticsearch instance. 

Customization
--------------
To be written.

Dependencies
------------

To be written.


License
-------

BSD

Author Information
------------------

Edgar Kalaev  <edka@mail.ru>
