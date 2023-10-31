# Graylog_Content_Pack_VMWare-8.X-for VCSA/ESXI

Tested with VMWARE vSphere 8.0.2 and ESXI 8.0.0 and Graylog 5.1.4. Should work with all Stormshield 4.X version.

The Content Pack should be compatible with all Graylog 5.X version.

**Note this was built without extractors, only pipeline rules.**

## Includes

* 2 Inputs (Syslog/TCP/1515 for VCSA and Syslog/TCP/1514)
* 2 Streams (VCSA) and ESXI
* Pipeline Rule w/ Stages (Extract key/values pipeline function)
* Dashboards (24h) (VCSA Components / Esxi Components)


## Requirements
* Graylog 5.0 
* VCENTER Appliance and ESXI integrated with VCENTER
* VCSA configured to send logs
* ESXI configured to send log
* Open port 1514+1515 for TCP on the graylog host and/or docker compose file
 
## Install the content pack




## VCSA Syslog configuration

## ESXI Syslog configuration




## Screenshots
