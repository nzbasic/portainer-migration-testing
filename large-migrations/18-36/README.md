# Full Migration Test

## 1.21.0 -> ee:pr1338

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

notes after migrating
- LDAP Fail right at the end, backup gets restored
![image](https://media.discordapp.net/attachments/882111142355435540/962573560684118016/unknown.png)
- backup.db is the resulting backup