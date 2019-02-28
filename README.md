#Simple deployment configuration for cell-radio project (WIP)

##Prerequisites

This configuration requires docker-compose version  >=1.11 and docker version at least 17.05

##Run

`docker-compose up -f docker-compose.yml`

Deployment parameters like server and web application hosts, server HTTP and websocket ports and paths are configurable by environment variables, for example (default values are shown):

`WEBAPP_HOST=localhost BE_SRV_HOST=localhost BE_HTTP_PORT=8080 BE_HTTP_PATH=ht BE_WS_PORT=8081 BE_WS_PATH=ws docker-compose up -f docker-compose.yml`

##Use

 - Open in browser page at http://localhost:4201

 - Send POST HTTP requests to http://localhost:8080/ht/addmany with appropriate data

 - See the changes in the UI

###Example for POST HTTP requests to http://localhost:8080/ht/addmany:


```
curl -iv http://localhost:8080/ht/addmany -X POST -d '{"DftrxId":"dftrx0", "Config":{"RxGain":19, "Network":0, "2g_params":{"Arfcn":540, "Ulsc":65, "Dlsc":2}, "3g_params":{"Arfcn":10788, "Ulsc":8758542, "Dlsc":369}, "4g_params":{"Arfcn":1400, "Ulsc":5, "Dlsc":0}, "Alpha":0.017, "Slot":"0", "Celltrack":0, "Watcher":0, "Antenna":0, "GpsSrc":1, "Version":2, "App":1, "GsmMode":1, "Url":"http://localhost:8081/addmany", "Sound":1.000}, "State":{"DlMode":0, "Tune":"ul", "SignalFound":0, "Hsdpa":0, "Standard":"DCS", "Usrp":1, "Capabilities":16678719, "Expiration":1607713200000, "Compression":1, "Error":0, "Remote":0}, "GpsExt":{"Status":0, "Lat":32.097828, "Lon":34.846316, "Alt":52.6, "TS":138}, "Compass":{"Hdg":0.0, "FitErr":""}, "Timestamp":0, "Points":[{"Id":552,"SettingsVersion":0,"Channel":65,"SNR":33.2,"Angles":[{"TSi":139, "TSf":0.259143384615, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":35.9, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.54462, "Int_s":0.00000, "Int":-3.54462, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.263758769231, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":37.4, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.61846, "Int_s":0.00000, "Int":-3.61846, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.268374153846, "RSSI_m":-28.4, "RSSI_s":0.0, "SNR_m":35.9, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.54462, "Int_s":0.00000, "Int":-3.54462, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.342220307692, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":37.4, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.61846, "Int_s":0.00000, "Int":-3.61846, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.346835692308, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":40.5, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.61846, "Int_s":0.00000, "Int":-3.61846, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.351451076923, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":33.2, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.61846, "Int_s":0.00000, "Int":-3.61846, "Ant":0, "RxGain":19, "V":1}],"RSSI":-29.3,"Angle2a":0.0,"Antenna2a":22652576,"Compression":1,"Antenna":22652576,"TSi":139,"TSf":0.351451076923,"Clocks":[0, 0, 1536665497356427, 1536665497398082]}]}'
```

```
curl -iv http://localhost:8080/ht/addmany -X POST -d '{"DftrxId":"dftrx0", "Config":{"RxGain":19, "Network":0, "2g_params":{"Arfcn":540, "Ulsc":65, "Dlsc":2}, "3g_params":{"Arfcn":10788, "Ulsc":8758542, "Dlsc":369}, "4g_params":{"Arfcn":1400, "Ulsc":5, "Dlsc":0}, "Alpha":0.017, "Slot":"0", "Celltrack":0, "Watcher":0, "Antenna":0, "GpsSrc":1, "Version":2, "App":1, "GsmMode":1, "Url":"http://localhost:8081/addmany", "Sound":1.000}, "State":{"DlMode":0, "Tune":"ul", "SignalFound":0, "Hsdpa":0, "Standard":"DCS", "Usrp":1, "Capabilities":16678719, "Expiration":1607713200000, "Compression":1, "Error":0, "Remote":0}, "GpsExt":{"Status":0, "Lat":32.095, "Lon":34.846316, "Alt":52.6, "TS":138}, "Compass":{"Hdg":0.0, "FitErr":""}, "Timestamp":0, "Points":[{"Id":552,"SettingsVersion":0,"Channel":65,"SNR":36.2,"Angles":[{"TSi":139, "TSf":0.259143384615, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":35.9, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.54462, "Int_s":0.00000, "Int":-3.54462, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.263758769231, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":37.4, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.61846, "Int_s":0.00000, "Int":-3.61846, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.268374153846, "RSSI_m":-28.4, "RSSI_s":0.0, "SNR_m":35.9, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.54462, "Int_s":0.00000, "Int":-3.54462, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.342220307692, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":37.4, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.61846, "Int_s":0.00000, "Int":-3.61846, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.346835692308, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":40.5, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.61846, "Int_s":0.00000, "Int":-3.61846, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.351451076923, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":33.2, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.61846, "Int_s":0.00000, "Int":-3.61846, "Ant":0, "RxGain":19, "V":1}],"RSSI":-22.3,"Angle2a":0.0,"Antenna2a":22652576,"Compression":1,"Antenna":22652576,"TSi":139,"TSf":0.351451076923,"Clocks":[0, 0, 1536665497356427, 1536665497398082]}]}'
```

```
curl -iv http://localhost:8080/ht/addmany -X POST -d '{"DftrxId":"dftrx0", "Config":{"RxGain":19, "Network":0, "2g_params":{"Arfcn":540, "Ulsc":65, "Dlsc":2}, "3g_params":{"Arfcn":10788, "Ulsc":8758542, "Dlsc":369}, "4g_params":{"Arfcn":1400, "Ulsc":5, "Dlsc":0}, "Alpha":0.017, "Slot":"0", "Celltrack":0, "Watcher":0, "Antenna":0, "GpsSrc":1, "Version":2, "App":1, "GsmMode":1, "Url":"http://localhost:8081/addmany", "Sound":1.000}, "State":{"DlMode":0, "Tune":"ul", "SignalFound":0, "Hsdpa":0, "Standard":"DCS", "Usrp":1, "Capabilities":16678719, "Expiration":1607713200000, "Compression":1, "Error":0, "Remote":0}, "GpsExt":{"Status":0, "Lat":32.0967, "Lon":34.8463, "Alt":52.6, "TS":138}, "Compass":{"Hdg":0.0, "FitErr":""}, "Timestamp":0, "Points":[{"Id":552,"SettingsVersion":0,"Channel":65,"SNR":36.2,"Angles":[{"TSi":139, "TSf":0.259143384615, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":35.9, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.54462, "Int_s":0.00000, "Int":-3.54462, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.263758769231, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":37.4, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.61846, "Int_s":0.00000, "Int":-3.61846, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.268374153846, "RSSI_m":-28.4, "RSSI_s":0.0, "SNR_m":35.9, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.54462, "Int_s":0.00000, "Int":-3.54462, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.342220307692, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":37.4, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.61846, "Int_s":0.00000, "Int":-3.61846, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.346835692308, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":40.5, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.61846, "Int_s":0.00000, "Int":-3.61846, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.351451076923, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":33.2, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.61846, "Int_s":0.00000, "Int":-3.61846, "Ant":0, "RxGain":19, "V":1}],"RSSI":-24.3,"Angle2a":0.0,"Antenna2a":22652576,"Compression":1,"Antenna":22652576,"TSi":139,"TSf":0.351451076923,"Clocks":[0, 0, 1536665497356427, 1536665497398082]},{"Id":553,"SettingsVersion":0,"Channel":65,"SNR":30.2,"Angles":[{"TSi":139, "TSf":0.259143384615, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":35.9, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.54462, "Int_s":0.00000, "Int":-3.54462, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.263758769231, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":37.4, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.61846, "Int_s":0.00000, "Int":-3.61846, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.268374153846, "RSSI_m":-28.4, "RSSI_s":0.0, "SNR_m":35.9, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.54462, "Int_s":0.00000, "Int":-3.54462, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.342220307692, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":37.4, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.61846, "Int_s":0.00000, "Int":-3.61846, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.346835692308, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":40.5, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.61846, "Int_s":0.00000, "Int":-3.61846, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.351451076923, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":33.2, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.61846, "Int_s":0.00000, "Int":-3.61846, "Ant":0, "RxGain":19, "V":1}],"RSSI":-21.3,"Angle2a":0.0,"Antenna2a":22652576,"Compression":1,"Antenna":22652576,"TSi":139,"TSf":0.351451076923,"Clocks":[0, 0, 1536665497356427, 1536665497398082]}]}'
```

##Project purpose

1. We need to create a simple web-server that will process addmany request.

POST: /addmany

Example request (unformatted, to save space)
{"DftrxId":"dftrx0", "Config":{"RxGain":19, "Network":0, "2g_params":{"Arfcn":540, "Ulsc":65, "Dlsc":2}, "3g_params":{"Arfcn":10788, "Ulsc":8758542, "Dlsc":369}, "4g_params":{"Arfcn":1400, "Ulsc":5, "Dlsc":0}, "Alpha":0.017, "Slot":"0", "Celltrack":0, "Watcher":0, "Antenna":0, "GpsSrc":1, "Version":2, "App":1, "GsmMode":1, "Url":"http://localhost:8081/addmany", "Sound":1.000}, "State":{"DlMode":0, "Tune":"ul", "SignalFound":0, "Hsdpa":0, "Standard":"DCS", "Usrp":1, "Capabilities":16678719, "Expiration":1607713200000, "Compression":1, "Error":0, "Remote":0}, "GpsExt":{"Status":0, "Lat":32.097839, "Lon":34.846317, "Alt":52.6, "TS":138}, "Compass":{"Hdg":0.0, "FitErr":""}, "Timestamp":0, "Points":[{"Id":552,"SettingsVersion":0,"Channel":65,"SNR":33.2,"Angles":[{"TSi":139, "TSf":0.259143384615, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":35.9, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.54462, "Int_s":0.00000, "Int":-3.54462, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.263758769231, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":37.4, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.61846, "Int_s":0.00000, "Int":-3.61846, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.268374153846, "RSSI_m":-28.4, "RSSI_s":0.0, "SNR_m":35.9, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.54462, "Int_s":0.00000, "Int":-3.54462, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.342220307692, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":37.4, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.61846, "Int_s":0.00000, "Int":-3.61846, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.346835692308, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":40.5, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.61846, "Int_s":0.00000, "Int":-3.61846, "Ant":0, "RxGain":19, "V":1},{"TSi":139, "TSf":0.351451076923, "RSSI_m":-28.3, "RSSI_s":0.0, "SNR_m":33.2, "SNR_s":0.0, "Master":1, "An":0.00, "Phase":0.00, "Visible":1, "Int_m":-3.61846, "Int_s":0.00000, "Int":-3.61846, "Ant":0, "RxGain":19, "V":1}],"RSSI":-28.3,"Angle2a":0.0,"Antenna2a":22652576,"Compression":1,"Antenna":22652576,"TSi":139,"TSf":0.351451076923,"Clocks":[0, 0, 1536665497356427, 1536665497398082]}]}
Response:
In fact, the answer is almost completely consistent with the configuration that we received in the request body. Just add a few values: Command (0 for our case), Watcher (0), ScapPsc (" "), ScanTimeouts (" "), ScanUlsc(" "), Mode(0)
Example response:
{  
   "UsrpCfg":{  
      "RxGain":19,
      "Network":0,
      "2g_params":{  
         "Arfcn":540,
         "Ulsc":65,
         "Dlsc":2
      },
      "3g_params":{  
         "Arfcn":10788,
         "Ulsc":8758542,
         "Dlsc":369
      },
      "4g_params":{  
         "Arfcn":1400,
         "Ulsc":5,
         "Dlsc":0
      },
      "Alpha":0.017,
      "Slot":"0",
      "Celltrack":0,
      "Watcher":0,
      "Mode":0,
      "Antenna":0,
      "GpsSrc":1,
      "Version":3,
      "App":2,
      "ScanUARFCN":"10788",
      "ScanPSC":" ",
      "UlScStart":8000000,
      "UlScEnd":9000000,
      "ScanULSC":" ",
      "ScanTimeouts":" "
   },
   "Command":0
}
2. How to display data.
We need to implement a simple GUI to display some data, as shown in the picture below. GUI can receive this data using websocket).

[Web application](./webapp.jpg)

The data to be displayed on the map is contained in body of addmany request. Red highlights the data you need to display.
{
   "DftrxId":"dftrx0",
   ...
   "GpsExt":{  
      "Status":0,
      "Lat":32.097839,
      "Lon":34.846317,
      "Alt":52.6,
      "TS":138
   },
   "Points":[  
      {  
         "Id":552,
         "SettingsVersion":0,
         "Channel":65,
         "SNR":33.2,
         "Angles":[...],
         "RSSI":-28.3,
	  ...
      }
   ]
}

2. How to display data.
We need to implement a simple GUI to display some data, as shown in the picture below. GUI can receive this data using websocket).

The data to be displayed on the map is contained in body of addmany request. Red highlights the data you need to display.
{
   "DftrxId":"dftrx0",
   ...
   "GpsExt":{  
      "Status":0,
      "Lat":32.097839,
      "Lon":34.846317,
      "Alt":52.6,
      "TS":138
   },
   "Points":[  
      {  
         "Id":552,
         "SettingsVersion":0,
         "Channel":65,
         "SNR":33.2,
         "Angles":[...],
         "RSSI":-28.3,
	  ...
      }
   ]
}

