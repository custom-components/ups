# ups

_Due to [ADR0004](https://github.com/home-assistant/architecture/blob/master/adr/0004-webscraping.md) this integration was removed from [Home Assistant](https://github.com/home-assistant/home-assistant/tree/0.99.0) with version 0.100, and are now republished here._

⚠️ This integration scrapes a website to get the information!
⚠️ There are no one actively maintaining this repository.

The `ups` platform allows one to track deliveries by the [UPS](https://www.ups.com/). To use this sensor, you need a [My UPS Account](https://www.ups.com/mychoice).

## Installation

1. Using the tool of choice open the directory (folder) for your HA configuration (where you find `configuration.yaml`).
2. If you do not have a `custom_components` directory (folder) there, you need to create it.
3. In the `custom_components` directory (folder) create a new folder called `ups`.
4. Download _all_ the files from the `custom_components/ups/` directory (folder) in this repository.
5. Place the files you downloaded in the new directory (folder) you created.
6. Restart Home Assistant.
7. Move on to the configuration.

Using your HA configuration directory (folder) as a starting point you should now also have this:

```text
custom_components/ups/__init__.py
custom_components/ups/manifest.json
custom_components/ups/sensor.py
```

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

## Contributions are welcome!

If you want to contribute to this please read the [Contribution guidelines](CONTRIBUTING.md)
