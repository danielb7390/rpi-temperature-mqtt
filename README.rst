DS18B20 Temperature to mqtt for Raspberry Pi
=============================

Reads the the temperature of DS18B20 sensors and sends it to a mqtt broker.


Installation:
-------------------

    pip install rpi-temperature-mqtt

Configuration:
-------------------

Needs a json configuration file as follows (don't forget to change ip and credentials ;-)):

.. code:: json

    {
        "mqtt_client_id": "power_meter",
        "mqtt_host": "192.168.0.210",
        "mqtt_port": "1883",
        "sources": [
            {
              "serial": "10-0008031e4d9e",
              "topic": "halti/stweg/temperature_heating"
            },
            {
              "serial": "10-0008031e804b",
              "topic": "halti/stweg/temperature_water"
            },
            {
              "serial": "10-0008031eaac7",
              "topic": "halti/stweg/temperature_solar"
            }
          ]
    }



Start:
-------------------

    rpi-temperature-mqtt config.json
