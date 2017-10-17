# tap-criteo

singer.io tap- Extracts data from the Criteo API, written in python 3.5.

Author: Ashwani Singh (ashwani.s@blueoceanmi.com)


1. Install

    >python setup.py install 
    >tap-criteo -h

2. Execution and configuration options:

    tap-criteo takes two inputs arguments
     
     I. --config:  It takes a configuration file as authentication parameters and parameters are "username", "password", "apptoken", "clientversion", "User-Agent", refer Criteo documentation for more information.

     II. --state: This is optional parameter define state where data extraction done last time. this parameter takes JSON file as input, two parameters will be passed in JSON file 1) "filter", format for this parameter is based on format which Criteo supports, for referenece please refer https://support.criteo.com/hc/en-us/articles/209273149-How-do-I-call-the-reporting-information-using-the-Criteo-API-.
2) "increment" option, this option to specify day bucket for between start date and end date, for one day bcuket use 0, for 2 days use 1 it should be (number of days - 1).

Note: If state is not defined start date and end date will one day prior of current date and increment option will be 0.
    
3. Running the application:
    > tap-criteo --config config.json  [--state  state.json]

