# Backup Agreement

## Backup Coverage
- MySQL databases
- InfluxDB databases
- DNS bind9 configuration
- Wordpress configuration
- Grafana database & configuration
- HAProxy configuration

## Backup Coverage: Excluded Services

These services do not need to be backed up as they can easily be spun up in the case that their configuration or setup is lost.

* Exporters 
* Telegraf
* Prometheus
* Rsyslog 

## Backup Frequency & Versioning
- Full local backup every night
- Full remote backup every night
- Incremental backup on weekdays

Different versions of backups are always stored so restoring from backups is easier, more efficient and takes less space.

## Retention
Backups older than 30 days are considered to be unusuable and will be deleted as they are very old.

## Recovery Point Objective
The maximum timeframe of lost data in the event of a disaster is 1 day, considering that backups are taken only daily.

## Recovery Time Objective
The maximum tolerable downtime for services is 2 hours for extreme cases, although we aim to restore services and data from backup in maximum 1 hour.

## Usability
The integrity of our backups will be regularly tested to ensure that services can be restored from their latest backup in the event of a disaster.

## Restoration Criteria
Affected data and configuration files must be restored from backups in the event of any data loss.