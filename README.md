# Solcast [[Home Assistant](https://www.home-assistant.io/) Component]
This custom component integrates the Solcast API into Home Assistant.

## Basic Installation/Configuration Instructions:
Copy content of custom_components to your local custom_components folder and add the following lines to your configuration.

#### Rooftop Site Configuration:
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

<hr>
