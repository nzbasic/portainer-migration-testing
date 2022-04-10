# DB 18 -> DB 19

18 = 1.21.0\
19 = 1.22.0

## Area of Migration
- Settings

### Before Migration
- Added local endpoint (docker socket)
- Settings:
    - Snapshot interval: 5m -> 10m
    - Added hidden container: foo : bar
    - Enable host management features: off -> on
    - Disable bind mounts for non-administrators: off -> on

### After Migration Notes
- Everything was same in UI

Logs:
![logs](https://media.discordapp.net/attachments/882111142355435540/962587329938219008/unknown.png?width=2160&height=317)
