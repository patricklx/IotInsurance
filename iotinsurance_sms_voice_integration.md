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
{:tip: .tip}
{:note: .deprecated}


# Enabling SMS and voice messaging (Deprecated)
{: #supportedcloud}

**This service is deprecated:** For more information, see the [deprecation announcement blog](https://www.ibm.com/blogs/bluemix/2017/11/iot-for-insurance-on-bluemix-migrated-to-saas-offering/){: new_window}.

However, {{site.data.keyword.iotinsurance_short}} is not going away. As of 31 July 2017, {{site.data.keyword.iotinsurance_short}} became a SaaS offering. The SaaS offering is available on [IBM Marketplace](https://www.ibm.com/us-en/marketplace/ibm-iot-for-insurance){: new_window}. Product documentation for the SaaS offering of {{site.data.keyword.iotinsurance_full}} is in the [IBM Knowledge Center](https://www.ibm.com/support/knowledgecenter/SSQNYQ/iot-insurance/kc_welcome.html){: new_window}.

Existing instances of this service can be used until 12 December 2018. However, you are encouraged to migrate to the SaaS offering of {{site.data.keyword.iotinsurance_short}}. If you have data from this service that you want to migrate to the SaaS offering, you must open a [ticket at https://console.bluemix.net/](https://console.bluemix.net/){: new_window} under **Support > Add Ticket**.  
{: deprecated}

---


{{site.data.keyword.iotinsurance_full}} supports integration with Twilio to enable SMS and voice messaging. Twilio is a third-party application, which you can install in your {{site.data.keyword.Bluemix_notm}} dashboard.
{: shortdesc}

## Prerequisites
To enable voice messaging, you must have an authorized Twilio account and a Twilio call-from phone number.  If you use a Twilio free account, you must also authorize a phone number to receive calls or messages. For more information, see the [Twilio documentation ![External link icon](../../icons/launch-glyph.svg)](https://support.twilio.com/hc/en-us/articles/223136107-How-does-Twilio-s-Free-Trial-work-){:new_window}.

## Creating and configuring a Twilio instance
1. Create a Twilio instance in the same {{site.data.keyword.Bluemix_notm}} organization and space in which you installed {{site.data.keyword.iotinsurance_short}}.
    1. Log in to [{{site.data.keyword.Bluemix_notm}}](https://console.ng.bluemix.net).
    2. Select the **Catalog** tab.
    3. Locate the Mobile section of the service catalog and click  **Twilio**.

    **Tip:** Click  [here ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://console.ng.bluemix.net/catalog/services/twilio/){: new_window} to go directly to the Twilio page.
    {: tip}

    4. On the Twilio page, provide your credentials and bind the application, as follows:

      1. Enter `Twilio-00` as the service name.  **Important:** You must use `Twilio-00` to connect successfully to {{site.data.keyword.iotinsurance_short}}.

      2. Enter your Twilio credentials.

      3. In the **Connect to** menu, select your iot4i-action-engine application to bind the Twilio instance to {{site.data.keyword.iotinsurance_short}}.

      4. Click **Create**.  

    The Twilio application is installed in your environment. A message prompts you to restage, or restart, your iot4i-action-engine application to enable the binding. You can restart now or wait to restart until you add the new environment variable in the next step.

2. Create an environment variable called TWILIO_FROM_NUMBER for the iot4i-action-egine component.
    1. From the Bluemix dashboard, open the iot4i-action-engine application.
    2. Select **Runtime**, then click **Environment Variables**.
    3. In the **User Defined** section, click **Add**.
    4. In the Name column, enter `TWILIO_FROM_NUMBER` and then in the Value column, enter your Twilio voice and SMS-capable number.
    5. Click **Save**.

3. Restart the Iot4i-action-engine application by clicking the Restart icon that is next to the Routes button.

## Adding the SMS and voice actions to a shield

To add SMS and voice capabilities to a shield, you must add the following actions to the shield definition:
  - `send-sms`
  - `phone-call`

For an example of a shield that contains a list of actions, see the [Create a sample shield example ![External link icon](../../icons/launch-glyph.svg)](https://github.com/IBM-Bluemix/iot4i-api-examples-nodejs/blob/master/bl/shield.js){:new_window}. In the example, the SMS and voice actions can be added to the list of actions that contains the `email` and `pushios` actions.

For more information about creating shields, see [Using the shield toolkit](iotinsurance_shield_toolkit.html).
