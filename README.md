## Synopsis

Better Mysql Dashboard template for DataDog 

## How to import dashboard into DataDog 

* Grab the latest [Better Mysql Plugin](https://github.com/ovaistariq/dd-agent/blob/master/checks.d/mysql.py) from Ovais' repo if you haven't already
* Deploy it to your DataDog installation  /opt/datadog-agent/agent/checks.d/better-mysql.py 
* Deploy plugin configuration to /etc/dd-agent/conf.d/better-mysql.yaml
* Note: you need to tag DB instances in DataDog configuration with tags: `- dbinstanceidentifier:my_own_instance_name`
* Get Datadog API Key and Application Key from [DataDog dashboard](https://app.datadoghq.com/account/settings#api)
* Import Better Mysql Dashboard:

```
api_key=<your_api_key>
app_key=<your_app_key>
curl  -X POST -H "Content-type: application/json" -d @better_mysql_dashboard.json "https://app.datadoghq.com/api/v1/dash?api_key=${api_key}&application_key=${app_key}"
```

## License

[Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0)

