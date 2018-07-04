# Bandwidth Monitor Usage

Script needs the vnstat daemon running. You have to update vnstat with a cron job (vnstat -u) to populate for data.
This script is working in openwrt router.

## Add UserParameter
`UserParameter=net.bandwidth[*],/usr/local/bin/bandwidth_monitor.sh $1 $2 $3`

## Add Item
  + Type: Zabbix Agent type
  + Key: `net.bandwidth[eth1,rx,d]`
  + Type of information: Numeric (float)
  + Units: MB
