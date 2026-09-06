Scheater provides intelligent heating control by dynamically adjusting heater on/off cycles based on:
- Current temperature vs. setpoint
- External temperature
- Window/door opening detection
- Power consumption tracking
- Adaptive learning coefficients

The system uses a TPI algorithm to maintain precise temperature control while optimizing energy consumption.

## Installation

[![Open your Home Assistant instance and show the add add-on repository dialog with a specific repository URL pre-filled.](https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg)](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2FNinho67%2FScheaterAddOn)

1. Click the button above (or add `https://github.com/Ninho67/ScheaterAddOn` manually in **Settings › Add-ons › Add-on store › ⋮ › Repositories** if the button doesn't pre-fill the dialog on your Home Assistant version)
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

Full version history: [scheater.ch/changelog](https://scheater.ch/changelog).

## Quality

![Tests](https://img.shields.io/badge/tests-281%20passing-blue)
![Coverage](https://img.shields.io/badge/coverage-40.5%25-blue)

Scheater is covered by an automated test suite (xUnit v3). The coverage figure is for the
`Scheater` project only (the business logic — schedulers, licensing, backups...); it doesn't blend
in the trivially-near-100%-covered test project itself, and it excludes code that was never meant
to be unit-tested: EF Core migrations (auto-generated, regenerated wholesale on every schema
change) and local-only dev/test doubles (stand-ins for Home Assistant/MQTT used to work without
real infrastructure, never part of the shipped add-on). Blazor UI code is mostly exercised manually
rather than through unit tests. Both badges are static and updated by hand at release time — no
public CI badge yet, since the source lives in a private repository and this repo only mirrors the
add-on's config/README/Docker image, so there's nothing here for a public CI badge to build
against.

## Premium Plan

In its free version, Scheater is limited to 5 radiators, which meets the needs of most users.
To exceed this limit and/or access all features, the Premium functions can be unlocked by purchasing a licence key.

This contribution will enable me to continue developing new features in the future.

Thank you for your support !

### Offline grace period

Scheater's whole point is to keep heating your home even when things go wrong, so a network hiccup
must never turn off your Premium features. If your Home Assistant instance loses internet access,
Premium features keep working for **30 days** before a fresh license check is required — plenty of
margin for a long weekend, or longer, without connectivity.

### Exit commitment

If Scheater is ever discontinued, or if the licensing service stops working, a final version of the
add-on with all Premium features unlocked and no license check will be published on GitHub. You will
never be left with a bricked installation because the project or its licensing backend went away.

## Support
Found a bug? [Open an issue here](https://github.com/Ninho67/ScheaterAddOn/issues)