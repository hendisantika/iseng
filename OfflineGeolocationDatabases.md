# Offline Geolocation Databases ( MySQL )

#### [Download via Google Drive](https://drive.google.com/folderview?id=0B5XAIFfgYFX4cnNna0V3U1JORXc&usp=sharing)

![total_data](https://cloud.githubusercontent.com/assets/1286932/12443687/32444ffc-bf8c-11e5-8d7c-c25ac714e4c6.png)

```sh
mysql -u username -p db_name < /path/to/mysql_semargeodata_v1.sql
```

```sql
-- sample query ( test di MySQL v.5.6.x )
SELECT *, ((ACOS(SIN(-6.9147444 * PI() / 180) * SIN(latitude * PI() / 180) + COS(-6.9147444 * PI() / 180) * COS(latitude * PI() / 180) * COS((107.6098111 - longitude) * PI() / 180)) * 180 / PI()) * 60 * 1.1515 * 1.609344) as distance FROM semargeodata HAVING distance <= 20 ORDER BY distance ASC limit 10
```

Source(s) of Data
----

[Geoname.Org](http://geonames.org)

License
----

WTFPL
