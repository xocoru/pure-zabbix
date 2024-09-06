# Pure Storage FlashArray Zabbix 6.x Template 

A repository of Zabbix template to monitor Pure Storage FlashArrays using OM Exporter (https://github.com/PureStorage-OpenConnect/pure-fa-openmetrics-exporter)

## Installation

* Import the template to Zabbix
* Add PureStorage FlashArray as a host and attach the template
* Override macros {$EXPORTER}, {$API_TOKEN} on host level

## Metrics collection

There is only one item (HTTP Agent) that fetches "https://{$EXPORTER}/metrics?endpoint={HOST.HOST}" every 1 min, all other items and LLD are dependant items.
