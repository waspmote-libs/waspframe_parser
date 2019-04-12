Waspmote Frame parser
=====================

Python package to parse [Libelium Waspmote](http://www.libelium.com/products/waspmote/) Data Frame to python dict


How to use 
----------

```python
>>> import waspframe_parser as wfp
>>> INCOMING_FRAME = b"<=>\x86\x09#3B2F6F057C1054E6#MOTE1#216#BAT:71#TC:19.94#HUM:28#PRES:100857.50#CO:0.000#NO:0.001#PM1:4.1600#PM2_5:7.6200#PM10:37.7800#STR:random_str#"
>>> PARSED_FRAME = wfp.frame_to_dict(INCOMING_FRAME)
>>> print(PRASED_FRAME)
{'HEADER': {'FRAME_TYPE': 'ASCII', 'NUM_FIELDS': 9, 'WASPMOTE_ID': '3B2F6F057C1054E6', ' SEQUENCE': 216}, 'PAYLOAD': {'BAT': 71, 'TC': 19.94, 'HUM': 28, 'PRES': 100857.5, 'CO': 0, 'NO': 0.0001, 'PM1': 4.16, 'PM2_5': 7.62, 'STR': 'random_str'}}

```

Docs
----

[Data Frame Guide](http://www.libelium.com/development/waspmote/documentation/data-frame-guide/)

[Waspmote Pro API - v040](http://www.libelium.com/development/waspmote/sdk_applications)
