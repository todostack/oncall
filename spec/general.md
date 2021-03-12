# OnCall

OnCall is a self hosted and eventually SaaS that enables easy integration with monitoring systems, such as CloudWatch, prometheus, grafana, et al, enabling teams to be able to have a schedule to be on call for and facilitate hand-offs from one team to another.

The main ingestion point will be a set of API endpoints that will enable users to use command line, web interface or mobile applications to acknowledge, hand-off, resolve, comment and put an incident through the appropriate workflows, schedules and services needed and customized by the team.

## Notification pathways
- sms
- voice(call)
- command line
- mqtt publisher
- http
- telegram
- irc

## User management

- Single sign on
- Active directory
- ldap
- iam
- local

First user starts off as Admin.

Any new user can be added as a default responder.

From there they can be changed to:
- spectator 
- shareholder
- incident manager 
- incident analyst
- developer
- incident coordinator
- Admin

----
## Endpoints

### /api/incident
Create, resolve, hand-off, comment on incidents

### /api/timeline
Get a timeline of incidents and events in a json or rss format

### /api/schedule
View or modify schedules of team members,

### /api/notification
Each user can set their own notification pathways and disable and enable them at any time

### /api/services
Be able to add services under oncall schedules, for example, API, website, database, etc.

### /api/oncall
Modify, add, replace schedules to services.
