---
title: Airpatrol
description: Instructions on how to integrate Airpatrol air conditioning controllers into Home Assistant.
ha_category:
  - Climate
  - Sensor
ha_release: 2025.9
ha_iot_class: Cloud Polling
ha_config_flow: true
ha_codeowners:
  - '@antondalgren'
ha_domain: airpatrol
ha_platforms:
  - climate
  - sensor
ha_integration_type: integration
ha_quality_scale: bronze
---

The **Airpatrol** {% term integration %} allows you to control air conditioning units that can be controlled through  [Airpatrol](https://www.airpatrol.com/) into Home Assistant.

## Prerequisites

{% important %}
Your Airpatrol WiFi unit must be configured via the native Airpatrol application prior to being discoverable in the integration. This includes setting up the WiFi connection and any initial device configuration.
{% endimportant %}

{% include integrations/config_flow.md %}

## Entities

### Climate

The integration will create a climate entity for each air conditioning system found. The climate entity allows you to control:

- **HVAC Mode**: Set the operation mode (off, heat, cool)
- **Target Temperature**: Set the desired temperature for heating or cooling
- **Fan Mode**: Control the fan speed if supported by your system

### Sensor

The integration provides various sensors to monitor your air conditioning system:

- **Current Temperature**: The current room temperature
- **Humidity**: Current humidity level (if supported)

## Configuration

{% configuration_basic %}
Email:
    description: The email to your account with the Airpatrol application
Password:
    description: The password to your account with the Airpatrol application
{% endconfiguration_basic %}


### Limited functionality

Some features may not be available depending on your specific Airpatrol model and firmware version. Check the Airpatrol documentation for your specific device to understand available features. This integration has only been tested with **Airpatrol Wifi v5**.

