# ups

_Due to [ADR0004](https://github.com/home-assistant/architecture/blob/master/adr/0004-webscraping.md) this integration was removed from [Home Assistant](https://github.com/home-assistant/home-assistant/tree/0.99.0) with version 0.100, and are now republished here._

⚠️ This integration scrapes a website to get the information!
⚠️ There are no one actively maintaining this repository.

The `ups` platform allows one to track deliveries by the [UPS](https://www.ups.com/). To use this sensor, you need a [My UPS Account](https://www.ups.com/mychoice).

## Example configuration.yaml

```yaml
sensor:
  - platform: ups
    username: YOUR_USERNAME
    password: YOUR_PASSWORD
```

### Configuration options

Key | Type | Required | Description
-- | -- | -- | --
`username` | `string` | `True` | The username to access the UPS My Choice service.
`password` | `string` | `True` | The password for the given username.
`name` | `string` | `False` | Name the sensor.
`scan_inverval` | `list` | `False` | Minimum time interval between updates. Default is 1 hour.
