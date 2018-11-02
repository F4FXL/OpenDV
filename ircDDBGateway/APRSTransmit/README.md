
# APRSTransmit and APRSTransmitD
APRSTransmit and APRSTransmitD allow both to transmit APRS data over DStar i.e. turning it to DPRS. Newer radios like ID51+, ID5100 and ID4100 have extended DPRS capability and are able to handle various data types such as weather and objects. Yet not all APRS formats are supported by Icom : Mic-E, Compressed. When possible the APRS data is converted so that it can be parsed by Icom radios.

# APRSTransmit
APRSTransmit sends one single APRS frame to the specified repeater. The frame can be sent directly on the command line, be sure to escape it into single quotes.
```sh
aprstransmit N1RPT__c -aprs 'N0CALL>APRS:!3842.78N/00759.76E>208/023/Hello'
```
It can also read data from a single file. For example, this comes handy if you run a weather station with weewx and want to broadcast it over DPRS
```sh
aprstransmit N1RPT__C -file /path/to/your/file/containing/one/line/of/aprs/data
```
