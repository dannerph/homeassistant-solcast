# Solcast PV Forecasting
This custom component integrates the Solcast API into Home Assistant.

## Rooftop Site Configuration:
```yaml
solcast:
  api_key: XXXXXX
  resource_id: YYYYYY
  api_limit: 10
  disable_ssl_check: False
  disable_automatic_forecast_fetching: False
```
Switch configuration variables:
* **api_key**: Your API key from Solcast.
* **resource_id**: The rooftop site resouce_id from Solcast.
* **api_limit** (optional): Number of API calls that should be used for the history over the day, default is 10.
* **disable_ssl_check** (optional): Disable SSL certificate check, only  enable this if you are facing connection problems.
* **disable_automatic_forecast_fetching** (optional): if you want to set forecasting fetching via automation.

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
