# Full Migration Test

## 1.21.0 -> 2.0.0

configured: 
- user: admin : portainer
- dockerhub auth
- endpoint group: testGroup - [local]
- tag: testTag
- endpoint: local - docker socket
- registry: quay.io 
- settings:
    - snapshot interval: 5m -> 10m
    - Disable bind mounts for non-administrators: false -> true
    - Enable host management features: false -> true
    - Hidden containers: foo : bar
- stack: testStack (version: 2, services: test: image: nginx)
- user: testUser : a
- team: testTeam - [testUser (leader)]
- team: testTeam2 - [testUser (member)]
- template: testTemplate - description - nginx
- schedule: testSchedule - [local] -  0 28 15 10 4 - "test"
- uac: testStack -> testUser (restricted)
- uac: local (endpoint) -> testUser

notes after migrating:
- I can login with admin : portainer ✅
- dockerhub auth exists ✅
- endpoint group testGroup still exists ✅
- testTag exists ✅
- endpoint local exists ✅
- quay.io registry exists ✅
- settings:
    - snapshot interval is 10m ✅
    - hidden containers has foo : bar ✅
    - Disable bind mounts for non-administrators is set to true under the endpoint settings ✅
    - Host management is on ✅
- I have control over testStack ✅
- testUser exists (and I can login) ✅ 
- testUser has access to local endpoint ✅ 
- testTeam exists with teamUser leader ✅
- testTeam2 exists with teamUser member ✅
- testTemplate is gone (understandable?) ❓
- schedule is gone (not in ui anymore) ✅
- uac: testStack is restricted to testUser ✅