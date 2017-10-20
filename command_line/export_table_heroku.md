**Export tables from heroku to a local csv file**


**Connect to psql in heroku**

```

heroku pg:psql

```

**Export Data**

```
\copy (SELECT * FROM stats) TO stats.csv CSV DELIMITER ',' HEADER

``
