# Graylog Content Pack for VMWare 8.X (VCSA and ESXI)

# ONLY VCENTER CONTENT PACK IS AVAILABLE FOR NOW - ESXI AVAILABLE SOON

This content Pack is only intended for Security Monitoring.
If you noticed some data about security that is not parsed, you can open an issue and I will update the Content Pack.

Tested with VMWARE vSphere 8.0.2 and ESXI 8.0.0 and Graylog 5.2.0. Should work with all Stormshield 4.X version.

The Content Pack should be compatible with all Graylog 5.X version.

**Note this was built without extractors, only pipeline rules.**





## Includes

* 1 Input (Syslog/TCP/1515 for VCSA)  
* 1 Streams (VCSA)
* Pipeline Rule w/ Stages (Extract key/values pipeline function)
* Dashboards (24h) (VCSA ComponentS) + VCenter (SSO Activities / VM Activities)

## INCLUDES SOON AVAILABLE 
* 1 Input (Syslog/TCP/1514 for ESXI)
* 1 Stream (ESXI)
*  Pipeline Rule w/ Stages (Extract key/values pipeline function)
* Dashboards (24h) (ESXI Components) + ESXI (SSO Activities / VM Activities)
  
## Requirements
* Graylog 5.0+ 
* VCENTER Appliance and ESXI integrated with VCENTER
* VCSA configured to send logs
* ESXI configured to send log
* Open port 1514+1515 for TCP on the graylog host and/or docker compose file
 
## Install the content pack

Go to System > Content Pack > Upload (Drag and drop file or Select)
Then click install, 

I recommend you to create a specific Indice for VCSA, and apply the VCSA Stream to it.


## VCSA Syslog configuration

- Access management interface:
https://your_vcsa_ipaddress:5480/

Go to Syslog > Edit

<img width="1283" alt="image" src="https://github.com/s0p4L1n3/Graylog_Content_Pack_VMWare-8.X-forVCSA-ESXI/assets/126569468/b0e64847-30a9-416d-8810-5142e246d925">


## ESXI Syslog configuration

Available soon


## Screenshots

- VCenter Dashboard
  
<img width="1880" alt="VCenter_basic_event_field" src="https://github.com/s0p4L1n3/Graylog_Content_Pack_VMWare-8.X-forVCSA-ESXI/assets/126569468/8e83774b-ec3e-409d-ad80-2b1109ee9450">

<img width="1867" alt="VCENTER_SSO_Activities" src="https://github.com/s0p4L1n3/Graylog_Content_Pack_VMWare-8.X-forVCSA-ESXI/assets/126569468/f66cf389-c4c9-44e8-876e-1589762831fa">

<img width="1871" alt="VCENTER_Virtual_machine_activities" src="https://github.com/s0p4L1n3/Graylog_Content_Pack_VMWare-8.X-forVCSA-ESXI/assets/126569468/a88a0cc3-833c-446c-b13f-a181904d8f44">

## Known ISSUE

I did not find how to parse VCenter splitted message in two parts, see this thread: https://community.graylog.org/t/pipeline-rules-for-messages-splitted-in-2-or-more-parts/30511/5
