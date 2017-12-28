---

copyright:
  years: 2016, 2017
lastupdated: "2017-12-28"
---

<!-- Common attributes used in the template are defined as follows: -->
{:new_window: target="blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:note: .deprecated}


# Extending the service with APIs (Deprecated)
{: #iot4i_extending_service}

**This service is deprecated:** For more information, see the [deprecation announcement blog](https://www.ibm.com/blogs/bluemix/2017/11/iot-for-insurance-on-bluemix-migrated-to-saas-offering/){: new_window}.

However, {{site.data.keyword.iotinsurance_short}} is not going away. As of 31 July 2017, {{site.data.keyword.iotinsurance_short}} became a SaaS offering. The SaaS offering is available on [IBM Marketplace](https://www.ibm.com/us-en/marketplace/ibm-iot-for-insurance){: new_window}. Product documentation for the {{site.data.keyword.iotinsurance_full}} SaaS offering is in the [IBM Knowledge Center](https://www.ibm.com/support/knowledgecenter/SSQNYQ/iot-insurance/kc_welcome.html){: new_window}.

Existing instances of this service can be used until 12 December 2018. However, you are encouraged to migrate to the {{site.data.keyword.iotinsurance_short}} SaaS offering. If you have data from this service that you want to migrate to the SaaS offering, you must open a [ticket at https://console.bluemix.net/](https://console.bluemix.net/){: new_window} under **Support > Add Ticket**.  
{: deprecated}

---

{{site.data.keyword.iotinsurance_full}} provides APIs to customize and extend your {{site.data.keyword.iotinsurance_short}} solution.
{:shortdesc}

{{site.data.keyword.iotinsurance_short}} comes with built-in support for Wink water leak sensors. By using the provided APIs, you can customize the {{site.data.keyword.iotinsurance_short}} solution to support new device types and vendors. {{site.data.keyword.iotinsurance_short}} relies on cloud-to-cloud communication to get sensor data from devices. By creating new transformation micro-services, you can customize {{site.data.keyword.iotinsurance_short}} to read the sensor data from new devices, pass it to the rest of the system through the {{site.data.keyword.iot_short_notm}} service, and then take actions as appropriate.

For a full set of example code, see the [API examples GitHub repository ![External link icon](../../icons/launch-glyph.svg)](https://github.com/IBM-Bluemix/iot4i-api-examples-nodejs/#iot-for-insurance-api-examples){: new_window}.

For complete information about the APIs, see the [API documentation ![External link icon](../../icons/launch-glyph.svg)](https://iot4i-api-docs.mybluemix.net/){: new_window}.
