# Solcast [[Home Assistant](https://www.home-assistant.io/) Component]
This custom component integrates the Solcast API into Home Assistant.

## Basic Installation/Configuration Instructions
Copy content of custom_components to your local custom_components folder and add the following lines to your configuration.

#### Rooftop Site Configuration:
```yaml
solcast:
  api_key: XXXXXX
  resource_id: YYYYYY
```
Rooftop site configuration variables:
* **api_key**: Your API key from Solcast.
* **resource_id**: The rooftop site resouce_id from Solcast.


## Available service calls

```yaml
update_forecast:
  description: >
    Fetches the forecasts from Solcast.

update_history:
  description: >
    Fetches historical data from Solcast.

push_measurement:
  desciption: >
    Pushes PV measurements to Solcast for model fine tuning.
  fields:
    total_power:
      desciption: >
        The total power of the PV system for the given period.
      example: 1.23456
    period:
      desciption: >
        The period of the total power (e.g. PT5M, PT15M, PT30M, ...)
      example: PT5M
    period_end:
      desciption: >
        The end period of the total power in UTC timezone
      example: 2018-02-02T03:30:00.0000000Z
```
