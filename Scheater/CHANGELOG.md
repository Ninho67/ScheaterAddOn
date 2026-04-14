# Changelog

## 1.10.0 - *In progress*
- License checking added
- Prepared for Home Assistant install as add-on
- UI : styles and layouts fixed
- Favicon fixed
- Bugfix: cache handling on zone deletion
- Bugfix: heater settings per zone were not created properly
- Bugfix: Zone override form fixed
- Useless controllers deleted

## 1.9.3 - 24/01/2026
- UI issues fixed

## 1.9.2 - 16/01/2026
- Other optimizations

## 1.9.1 - 16/01/2026
- Bugfix: Index page was lagging after some time
- Optimization: less acquisitions are shown in cards

## 1.9.0 - 15/01/2026
- Some HA entities are no longer needed and will stored in Scheater directly
- Set point offsets can now be configured per heaters in a zone
- First version of sensor pairing wizard created (Easy setup)
- Charts are now created with Apex
- Power counter algorithm optimized and is now very precise
- Bugfixes

## 1.8.0 - 19/12/2025
- New modern UI design
- Power consumption page improved
- Regulation coefficients are now auto-tuned
- Users can now be created to handle partial absences

## 1.7.3 - 06/12/2025
- Power counting bug fixed
- Optimizations

## 1.7.2 - 29/11/2025
- Cosmetic improvements

## 1.7.1 - 29/11/2025
- Bugfix: Applied temperature was wrong after recent changes
- Verbosity of scheduler reduced
- Bugfix: Heating state display was wrong on main page

## 1.7.0 - 29/11/2025
- Power consumption settings added (peak hours, currency)
- Power counter added
- Power consumption charts added
- A chart now displays temperature acquisitions for each zone
- Caching added to improve performance
- Thermostat statuses added to Diagnostics page

## 1.6.0 - 15/11/2025
- Thermostat fine tuned
- Heating state added to zone cards
- Performance metrics are now logged
- Bugfixes

## 1.5.0 - 09/11/2025
- Extended MQTT diagnostics for tests
- Temperature offset is now displaxed in the zone card
- HA diagnostics page added
- YAML config generator added to simplify setup
- External temperature entity added in settings (now displayed on dashboard)
- HA automation for regulation dropped in favor of new thermostat service

## 1.4.0 - 25/10/2025
- Special temperatures (absence, no freeze, comfort) offsets are now configurable
- HA entities can now be tested in heater dialog
- Battery indicators added to cards
- MQTT client added for diagnostics

## 1.3.2 - 13/10/2025
- Minor UI improvements

## 1.3.1 - 12/10/2025
- Bugfix: The temperature displayed on override cards was wrong
- New calendar component added

## 1.3.0 - 11/10/2025
- Upgraded .net runtime
- Current temperature is now displayed for each radiator
- Scheduling activation mode is now configurable
- Override mode created to allow manual override of the schedule
- Absence handling added
- Overall UI restyling

## 1.2.3 - 27/09/2024
- Fixed HA's default IP address

## 1.2.2 - 02/09/2024
- Fixed CORS issue

## 1.2.1 - 17/11/2023
- Dropped quartz lib for a simpler solution

## 1.2.0 - 17/11/2023
- Backup and restore of of schedules
- Better handling of overlapping time slots

## 1.1.3 - 09/11/2023
- Upgraded .net runtime
- Overall cleanup

## 1.1.2 - 02/12/2022
- Fixed: Quartz job now uses the database settings

## 1.1.1 - 02/12/2022
- Fixed: the filter to get one specific setpoint from a schedule was incomplete and was hence causing errors

## 1.1.0 - 27/11/2022
- Bugfixes
- Default set point is now 15°C
- Can edit heaters
- Can edit zones
- UI improvements
- Handling of comfort modes
- Localized (FR, EN)

## 1.0.0 - 23/10/2022
- First version
- Can create/delete radiators
- Can create/delete zones
- Can configure heating time slots for each zone
- Depends on automations in HA for regulation