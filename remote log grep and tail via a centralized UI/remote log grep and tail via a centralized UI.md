# Remote log grep and tail support via a centralized UI

In this blog I will talk about two of my recent open source projects called [log-parse-agent](https://github.com/mchopker/log-parse-agent) and [log-parse-ui](https://github.com/mchopker/log-parse-ui), the reason why I wrote that and how it can help perform grep and tail operations on remote logs.

## Challenges

We had various applications (distributed in nature) deployed across dozens of virtual machines (mostly Linux). For any new feature development or debugging of production issues we had to login (via SSH) to many of these machines and look at respective logs. It was very time consuming to login to all machines and then look at respective logs, and we wanted something like a centralized user interface where we could quickly search logs on all remote machines. 

While there exist solutions like ELK, Splunk, etc. which provides many great features on log parsing, analysis, visualization and alerting, our requirement was simple to quickly identify patterns in remote logs for troubleshooting and also not have to setup big stacks like ELK, Splunk where we have to maintain central server and allocate enough storage to persist remote logs for analysis.

## Solution

I wrote [log-parse-agent](https://github.com/mchopker/log-parse-agent) project using Golang programming language which can be deployed in remote machines and configured to allow grep and tail operations on logs remotely via REST API endpoints. 

The [log-parse-ui](https://github.com/mchopker/log-parse-ui) is another project which can provide a centralized UI for all remote [log-parse-agent](https://github.com/mchopker/log-parse-agent)s to list their supported logs, perform grep and tail operations on them and view results in the UI itself.

For installation and usage details please refer to [log-parse-agent](https://github.com/mchopker/log-parse-agent) and [log-parse-ui](https://github.com/mchopker/log-parse-ui) projects.

## Future

If you have any feedback or suggestions please raise issue in [log-parse-agent](https://github.com/mchopker/log-parse-agent) and [log-parse-ui](https://github.com/mchopker/log-parse-ui) projects or email me at [mchopker@gmail.com](mailto:mchopker@gmail.com)

Thank you!