
# The Open Guide to Cloud Interface for ABB AbilityTM Smart Sensors

## Scope

- Open guide to learn how to use these [Web APIs](https://api.smartsensor.abb.com/swagger/) for ABB AbilityTM Smart Sensors.
- Provide customers with a simple Python class to communicate with the Smart Sensor Web API. This is a sample project as a starting point to build up the integration project(s).
- Create a community to share new developments, ask questions and propose suggestions for improvements based on real experience.
- For more details, please refer to the [documentation](https://search.abb.com/library/Download.aspx?DocumentID=9AKK107728&LanguageCode=en&DocumentPartId=&Action=Launch).

## Prerequisites

- Python 3 with `pip` and `setuptools` installed
- Test that you have access to the [Smart Sensor Web API](https://api.smartsensor.abb.com/swagger/)
- Obtain an API key from the [Smart Sensor website](https://smartsensor.abb.com)
- Get to know the feature codes related to the commands to be used, available in the section "Commands", available in the [documentation](https://search.abb.com/library/Download.aspx?DocumentID=9AKK107728&LanguageCode=en&DocumentPartId=&Action=Launch).

## Quick Start

1.  Install the complete package using `pip` by executing:
    
        python -m pip install .
        
    This will install the smart_sensor_client package along with its dependencies.
    **You need to do this every time you fetch an update from this repository.**

2.  Copy `settings.example.yaml` to `settings.yaml` and change the values. You can adjust your proxy settings (leave empty if none).
    You can also optionally specify your API key or username, which the Smart Sensor Client will use automatically.

3.  To run a simple use case, such as getting the latest measurements from all your assets, execute

    ```
    python use_case_1/plant_data.py
    ```
    
4.  To authenticate, enter your API key or your email address and password. The API Key can be requested by the users under your profile in the [ABB AbilityTM Smart Sensor Platform](https://smartsensor.abb.com). Go to API Keys and select the function “add new”. You will receive the API Key via email from the e-mail address noreply@smartsensor.abb.com.

5.  The sample program will display your assets in your Smart Sensor organization and their latest sensor measurements. You can check the measurements against those you see in the [ABB AbilityTM Smart Sensor Platform](https://smartsensor.abb.com).

6.  Finally, you can look at the use cases (see table below) and [SmartSensorClient](smart_sensor_client/smart_sensor_client.py) to see how it uses the Cloud Interface and how you can adapt it for your integration project.

## Use Cases

We provide code for some typical use cases of accessing the Smart Sensor Cloud Interface.
You can run each script by executing

    python <use_case_nr>/<use_case_file_name>

| Name                                             | Explanation                                      | Links                                                                                                                         |
|--------------------------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------|
| use_case_1/get_plant_data.py                     | Show all the information about a plant           | [code](use_case_1/get_plant_data.py), [usage](use_case_1)                     |
| use_case_1/get_simplified_asset_data.py          | Show all assets inside an organization           | [code](use_case_1/get_simplified_asset_data.py), [usage](use_case_1)          |
| use_case_1/get_detailed_sensor_and_asset_data.py | Show detailed information about an asset         | [code](use_case_1/get_detailed_sensor_and_asset_data.py), [usage](use_case_1) |
| use_case_2/add_notification_channel.py           | Add a notification channel to a sensor           | [code](use_case_2/add_notification_channel.py), [usage](use_case_2)           |
| TODO                                             | TODO                                             | [code](use_case_3/TODO), [usage](use_case_3)                                  |
| use_case_4/get_condition_indexes.py              | Show condition indexes of one or multiple assets | [code](use_case_4/get_condition_indexes.py), [usage](use_cases_4)             |
| use_case_5/get_historic_measurements.py          | Plot measurement values of a defined asset       | [code](use_case_5/get_historic_measurements.py), [usage](use_case_5)          |
