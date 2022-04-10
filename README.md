# Structure

granular-migrations contains migrations between adjacent versions. EE and CE is split, so there are only EE -> EE migrations. However, there is one CE -> EE migration for the first version of EE 

large-migrations contains 1.21.0 -> 2.0.0, 1.21.0 -> ce/ee latest, and 2.0.0 -> ce/ee latest

Inside the migrations dirs, each folder name represents a migration e.g. 18-19 = migration DB version 18 to DB version 19

For EE db versions, license has been omitted for obvious reasons 

# Version Reference

| DB Version | Portainer Version | Area of Migration (from previous)                                                                                                             |
|------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| 18         | 1.21.0            | N/A                                                                                                                                           |
| 19         | 1.22.0            | Settings                                                                                                                                      |
| 20         | 1.22.1            | Users, Settings, Schedules                                                                                                                    |
| 21         | None              |                                                                                                                                               |
| 22         | 1.23.0            | Resource Controls, Users, Roles                                                                                                               |
| 23         | 1.24.0            | Tags, Endpoint Groups                                                                                                                         |
| 24         | 1.24.1            | Settings                                                                                                                                      |
| 25         | CE 2.0.0          | Settings                                                                                                                                      |
| 26         | CE 2.1.0          | Endpoint Settings, RBAC Roles Refresh                                                                                                         |
| 27         | None              | (Marked as 2.2.0 in code, but version was skipped) Stack resource control                                                                     |
| 28, 29     | EE 2.4.0          | (2 Migrations in one version) Users, Roles, RBAC Refresh                                                                                      |
| 30         | EE 2.6.0          | Settings                                                                                                                                      |
| 31         | EE 2.7.0          | RBAC Refresh                                                                                                                                  |
| 32         | CE 2.9.0          | Registries Dockerhub Refresh RBAC Roles User Auth Volume Resource Control Admin Group Search Settings Stacks Kube Config Expiry Helm Repo URL |
| 33         | CE 2.9.1, 2.9.2   | Settings                                                                                                                                      |
| 34         | EE 2.10.0         | RBAC, User Auth                                                                                                                               |
| 35         | CE 2.9.3          | Dockerhub                                                                                                                                     |
| 36         | CE 2.11.x         | User Auth                                                                                                                                     |