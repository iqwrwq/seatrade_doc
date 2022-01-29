# SeaTrade Projekt
## Arthur Schimpf E3FI3

> Das SeaTrade Projekt ist ein Schulprojekt aus dem Java Kurs und ist die Übung zur Arbeit mit einem Server.

##Packet Informationen
>Das Packet beinhaltet eine ShipApp und eine CompanyApp. Die Konfigurationen der Applikationen kann unter `config/config.properties` vorgenommen werden. Die Applikationen funktionieren nur im Zusammenhang mit der SeaTradeApp.

###ShipApp Ordnerstruktur
```
├── ShipApp
│   └── config
│       └── config.properties
└── ShipApp.jar
```

###CompanyApp Ordnerstruktur
```
├── CompanyApp
│   └── config
│       └── config.properties
└── CompanyApp.jar
```

##Installation
> Um die Apps zu installieren, müssen zwei Zip Dateien heruntergeladen und entpackt werden. Die Struktur der Applikationen sollte nicht verändert werden.

###Nutzen
>Die Applikationen werden über das Terminal gestartet. Navigieren Sie über die Console in das Verzeichnis der Applikation, die Sie starten möchten.

>Befehl zum Starten Applikationen\
`.../CompanyApp/> java -jar CompanyApp.jar`\
`.../ShipApp/> java -jar ShipApp.jar`

###Konfiguration der Applikationen
####CompanyApp Konfiguration
>Anpassungen werden in der Properties Datei under `CompanyApp/config/config.properties` vorgenommen. Hier können verschiedene Properties gesetzt werden um die Applikation anzupassen.

| Property         | Wert     | Funktion |
|--------------|-----------|------------|
| host | String      | Die IP Adresse über welche Die Applikation laufen wird. Auch `localhost` möglich        |
| port      | Integer  | Der Port über welchen die Applikation mit der SeaTradeApp Kommunizieren kann       |
| companyName | String      | Der Name der Applikation. Dieser wird auch bei der SeaTradeApp registriert        |
| maxShipsAllowed      | Integer  | Die Anzahl der maximal erlaubten ShipApp-Verbindungen       |
| shipServerPort | Integer      | Der Port über welcher der ShipServer mit den ShipApp-Verbindungen Kommunizieren kann        |
| ReconnectionTimeGap      | Integer  | Die Zeit in ms mit welcher die Applikation nach einer misslungenen Verbindung warten soll, bis eine neue Verbindung aufgebaut wird       |
| ConnectionAttempts | Integer      | Die Anzahl an Wieder-Verbindungsversuchen nach Misslungener Verbindung        |

####ShipApp Konfiguration
>Auch in der ShipApp werden die Anpassungen unter `ShipApp/config/config.properties` gemacht

| Property         | Wert     | Funktion |
|--------------|-----------|------------|
| host | String      | Die IP Adresse über welche Die Applikation laufen wird. Auch `localhost` möglich        |
| port      | Integer  | Der Port über welchen die Applikation mit der SeaTradeApp Kommunizieren kann       |
| companyName | String      | Der Name der Applikation. Dieser wird auch bei der SeaTradeApp registriert        |
| maxShipsAllowed      | Integer  | Die Anzahl der maximal erlaubten ShipApp-Verbindungen       |
| shipServerPort | Integer      | Der Port über welcher der ShipServer mit den ShipApp-Verbindungen Kommunizieren kann        |
| ReconnectionTimeGap      | Integer  | Die Zeit in ms mit welcher die Applikation nach einer misslungenen Verbindung warten soll, bis eine neue Verbindung aufgebaut wird       |
| ConnectionAttempts | Integer      | Die Anzahl an Wieder-Verbindungsversuchen nach Misslungener Verbindung        |