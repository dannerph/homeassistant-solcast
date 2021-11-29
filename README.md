# Solcast [[Home Assistant](https://www.home-assistant.io/) Component] (Discontinued)
[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg?style=for-the-badge)](https://github.com/custom-components/hacs)

**!!! This component is no longer maintained.!!!**

Please have a look at this alternative: https://github.com/oziee/ha-solcast-solar


## Basic Installation/Configuration Instructions:
Copy content of custom_components to your local custom_components folder and add the following lines to your configuration.

#### Rooftop Site Configuration:
```yaml
solcast:
  api_key: XXXXXX
  resource_id: YYYYYY
  api_limit: 20
  disable_ssl_check: False
  disable_automatic_forecast_fetching: False
  disable_automatic_history_fetching: False
```
Switch configuration variables:
* **api_key**: Your API key from Solcast.
* **resource_id**: The rooftop site resouce_id from Solcast.
* **api_limit** (optional): Number of API calls that should be used for the history over the day, default is 10.
* **disable_ssl_check** (optional): Disable SSL certificate check, only  enable this if you are facing connection problems.
* **disable_automatic_forecast_fetching** (optional): if you want to set forecasting fetching via automation.
* **disable_automatic_history_fetching** (optional): if you want to set history fetching via automation (or you do not care about historical values at all).

<hr>

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
