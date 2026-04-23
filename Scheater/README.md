Scheater provides intelligent heating control by dynamically adjusting heater on/off cycles based on:
- Current temperature vs. setpoint
- External temperature
- Window/door opening detection
- Power consumption tracking
- Adaptive learning coefficients

The system uses a TPI algorithm to maintain precise temperature control while optimizing energy consumption.

## Installation

1. Add this repository to your Home Assistant Add-on store
2. Install the "Scheater" add-on
3. Configure the add-on (see Configuration section below)
4. Start the add-on
5. Access the Scheater web interface through Home Assistant

## Configuration

### Required Configuration

- **homeassistant_token**: Long-lived access token from Home Assistant
    - Create one in your Home Assistant profile settings
- **mqtt_broker**: MQTT broker hostname (default: `core-mosquitto` for Home Assistant's built-in broker)
- **mqtt_port**: MQTT broker port (default: `1883`)

### Optional Configuration

- **mqtt_username**: MQTT username (if authentication is enabled)
- **mqtt_password**: MQTT password (if authentication is enabled)
- **log_level**: Logging level (Trace, Debug, Information, Warning, Error, Fatal) (default: `Information`)

### Example Configuration

```json
{
  "mqtt_broker": "core-mosquitto",
  "mqtt_port": 1883,
  "mqtt_username": "",
  "mqtt_password": "",
  "log_level": "Information"
}
```
## Web Interface

Access the Scheater web interface through Home Assistant Ingress.

![](https://raw.githubusercontent.com/Ninho67/ScheaterAddOn/main/Scheater/scheater_perpsective_dark.png)

## Docs & Support

For more details, please refer to the [Scheater documentation](https://scheater.ch/documentation).

## Premium Plan

In its free version, Scheater is limited to 5 radiators, which meets the needs of most users.
To exceed this limit and/or access all features, the Premium functions can be unlocked by purchasing a licence key.

This contribution will enable me to continue developing new features in the future.

Thank you for your support !

## Support
Found a bug? [Open an issue here](https://github.com/Ninho67/ScheaterAddOn/issues)