?> Jetzt mit GitHub Releases! 🚀

# SeaTrade Projekt

<i class="fas fa-male"></i> Arthur Schimpf E3FI3

> Das SeaTrade Projekt ist ein Schulprojekt aus dem Java Kurs und ist die Übung zur Arbeit mit einem Server.

## Releases

### CompanyApp Releases

| Version                                                                                                 | tags                                | Download                                                                                                                                |
|:---                                                                                                     |:---:                                |:---:                                                                                                                                    |
|<a href="https://github.com/iqwrwq/company_app/releases/tag/v1.1.0" target="_blank">CompanyApp_v1.1.0</a>| <small class="badge green">stable</small> <small class="badge purple">latest</small> |  <a class="badge-btn" style="color: #fff;" href="zips/CompanyApp_v1.1.zip" download><i class="fa-solid fa-download fa-xl"></i></a>| 

### ShipApp Releases

| Version                                                                                            | tags                                | Download                                                                                                                            |
|:---                                                                                                |:---:                                |:---:                                                                                                                                |
|<a href="https://github.com/iqwrwq/ship_app/releases/tag/v1.0.0" target="_blank"> ShipApp_v1.0.0</a>| <small class="badge green">stable</small> <small class="badge purple">latest</small> | <a class="badge-btn" style="color: #fff;" href="zips/ShipApp_v1.0.zip" download><i class="fa-solid fa-download fa-xl"></i></a>|

## GIT

> Die Repositories für beide Projekte sind unter GitHub öffentlich einsehbar. Das main repository ist die Zusammensetzung beider Apps, sowie dieser Dokumentation

<i class="fab fa-github"></i> <a href="https://github.com/iqwrwq/seatrade_app"> SeaTradeApp Repository [main]</a>

<i class="fab fa-github"></i> <a href="https://github.com/iqwrwq/company_app"> CompanyApp Repository [sub]</a>\
<i class="fab fa-github"></i> <a href="https://github.com/iqwrwq/ship_app">ShipApp Repository [sub]</a>

## Packet Informationen

> Das Packet beinhaltet eine ShipApp und eine CompanyApp. Die Konfigurationen der Applikationen kann unter `config/config.properties` vorgenommen werden. Die Applikationen funktionieren nur im Zusammenhang mit der SeaTradeApp.

### ShipApp Ordnerstruktur

```
├── ShipApp
│   └── config
│       └── config.properties
└── ShipApp.jar
```

### CompanyApp Ordnerstruktur

```
├── CompanyApp│   │ └── config
│   │       └── config.properties
│   └──── logs
│           └── log.txt
└── CompanyApp.jar
```

## Installation

> Um die Apps zu installieren, müssen zwei Zip Dateien <a href="/#/?id=downloads">heruntergeladen</a> und entpackt werden.

!> Die Struktur der Applikationen sollte nicht verändert werden.

### Nutzen

> Die Applikationen werden über das Terminal gestartet. Navigieren Sie über die Console in das Verzeichnis der Applikation, die Sie starten möchten.

> Befehl zum Starten Applikationen\
`.../CompanyApp/> java -jar CompanyApp.jar`\
`.../ShipApp/> java -jar ShipApp.jar`

### Konfiguration der Applikationen

#### CompanyApp Konfiguration

> Anpassungen werden in der Properties Datei under `CompanyApp/config/config.properties` vorgenommen. Hier können verschiedene Properties gesetzt werden um die Applikation anzupassen.

| Property                                      | Wert     | Funktion                                                                                                                                                                                                         |
|-----------------------------------------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| host                                          | String   | Die IP Adresse über welche Die Applikation laufen wird. Auch `localhost` möglich                                                                                                                                 |
| port                                          | Integer  | Der Port über welchen die Applikation mit der SeaTradeApp Kommunizieren kann                                                                                                                                     |
| companyName                                   | String   | Der Name der Applikation. Dieser wird auch bei der SeaTradeApp registriert                                                                                                                                       |
| maxShipsAllowed                               | Integer  | Die Anzahl der maximal erlaubten ShipApp-Verbindungen                                                                                                                                                            |
| shipServerPort                                | Integer  | Der Port über welcher der ShipServer mit den ShipApp-Verbindungen Kommunizieren kann                                                                                                                             |
| ReconnectionTimeGap                           | Integer  | Die Zeit in ms mit welcher die Applikation nach einer misslungenen Verbindung warten soll, bis eine neue Verbindung aufgebaut wird                                                                               |
| ConnectionAttempts                            | Integer  | Die Anzahl an Wieder-Verbindungsversuchen nach Misslungener Verbindung                                                                                                                                           |
| harbours                                      | String[] | Mit Komma getrennte Aufzählung an Häfen in der SeaTradeApp                                                                                                                                                       |
| initialAutoSync                               | Boolean  | Automatische Synchronisation beim starten der Applikation. Derzeit werden alle Cargos aus der SeaTradeApp synchronisiert                                                                                         |
| muteSync                                      | Boolean  | Da der Sync Befehl meist sehr unübersichtlich wird, hat man hier die Möglichkeit den Befehl im Hintergrund ohne Benachrichtigung laufen zu lassen.                                                               |
| massMove                                      | Boolean  | EXPERIMENTAL! Aktiviert den `massmove` Befehl um alle Schiffe, die sich auf Häfen befinden, welche Cargos auf sich lagern zu beladen und zum Zielhafen zu bewegen. Derzeit wird aber von der Benutzung abgeraten |
| fullAutoMode                                  | Boolean  | EXPERIMENTAL! Aktivieren um die Application sich selbst zu überlassen. Sie wird Schiff-Verbidnungen verwalten und bewegen um Profit zu generieren                                                                |

#### ShipApp Konfiguration

> Auch in der ShipApp werden die Anpassungen unter `ShipApp/config/config.properties` gemacht

| Property            | Wert    | Funktion                                                                                                                           |
|---------------------|---------|------------------------------------------------------------------------------------------------------------------------------------|
| host                | String  | Die IP Adresse über welche Die Applikation laufen wird. Auch `localhost` möglich                                                   |
| port                | Integer | Der Port über welchen die Applikation mit der SeaTradeApp Kommunizieren kann                                                       |
| companyName         | String  | Der Name der Applikation. Dieser wird auch bei der SeaTradeApp registriert                                                         |
| maxShipsAllowed     | Integer | Die Anzahl der maximal erlaubten ShipApp-Verbindungen                                                                              |
| shipServerPort      | Integer | Der Port über welcher der ShipServer mit den ShipApp-Verbindungen Kommunizieren kann                                               |
| ReconnectionTimeGap | Integer | Die Zeit in ms mit welcher die Applikation nach einer misslungenen Verbindung warten soll, bis eine neue Verbindung aufgebaut wird |
| ConnectionAttempts  | Integer | Die Anzahl an Wieder-Verbindungsversuchen nach Misslungener Verbindung                                                             |

#### Kommandos

> Zum Benutzen der Applikation werden Befehle über die Console eingegeben. Alle Befehle richtigen sich hier an die CompanyApp. Befehle die sich im Kontext an die ShipApp richten werden trotzdem an die CompanyApp gerichtet. Befehlsparameter werden mit einem Leerzeichen getrennt.

#### Liste an Befehlen
| Befehl                          | Kommunikation               | Funktion                                                                                                                                                     |
|---------------------------------|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| move **SHIP_ID** **ZIEL_HAFEN** | ShipServer -> Ship<SHIP_ID> | Befiehlt dem Schiff mit der ID <SHIP_ID> sich zum <ZIEL_HAFEN> zu bewegen.                                                                                   |
| ships                           | ShipServer -> User          | Gibt eine Übersicht aller Schiffe aus, TIPP: Verwenden Sie diesen Befehl um die SHIP_ID einer ShipApp herauszufinden                                         |
| cargo                           | ShipServer -> User          | Gibt eine Übersicht über alle Cargos aus. Sollte ein Cargo neu für die Applikation sein, wird dieses im Speicher der Applikation notiert bzw. synchronisiert |
| load **SHIP_ID**                | ShipServer -> Ship<SHIP_ID> | Befiehlt dem Schiff mit der ID <SHIP_ID> das nächste Cargo am Hafen zu beladen                                                                               |
| load **SHIP_ID** **CARGO_ID**   | ShipServer -> Ship<SHIP_ID> | Befiehlt dem Schiff mit der ID <SHIP_ID> das Cargo mit der ID <CARGO_ID> zu laden                                                                            |
| unload **SHIP_ID**              | ShipServer -> Ship<SHIP_ID> | Befiehlt dem Schiff mit der ID <SHIP_ID> sein geladenes Cargo zu entladen                                                                                    |
| exit                            | User -> ShipServer          | Beendet alle ShipApp-Verbindungen und beendet den ShipServer, sowie die Verbindung zum SeaTradeServer                                                        |
| massmove                        | User -> ShipServer          | Beladen und Bewegen aller möglichen Schiffe (Muss aktiviert werden)                                                                                          |
| massunload                      | User -> ShipServer          | Abladen aller möglichen Schiffe (Muss aktiviert werden)                                                                                                      |
