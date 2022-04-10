# DB 19 -> DB 20

19 = 1.22.0\
19 = 1.22.1

## Area of Migration
- Users, Settings, Schedules

### Before Migration
- Added local endpoint (docker socket)
- Added user: testUser : password
- Added schedule
- Settings:
    - Snapshot interval: 5m -> 10m
    - Added hidden container: foo : bar
    - Enable host management features: off -> on
    - Disable bind mounts for non-administrators: off -> on
    - Edge agent poll frequency: 5s -> 10s

### After Migration Notes

Logs:
![logs]()
