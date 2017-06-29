# Deploy EC2

## requirements

**python**
3.6.1

**pip**

```
pip install -r requirements.txt
```

## Create secret config file

### Project structure
```
project_folder/
	.conf_secret/
		settings_common.json
		settings_debug.json
		settings_deploy.json
```

### settings_common.json

```
{
  "django": {
    "secret_key": "8k-&6us0jevlsplq-3-y%3vrmrz^#8yy2+8fw^&3b5&=mk+*ow"
  }
}
```

### settings_debug.json

```
{
  "django": {
    "allowed_hosts": [
      "*"
    ]
  }
}
```

### settings_deploy.json

```
{
  "django": {
    "allowed_hosts": [
      "*"
    ]
  }
}
```

### runserver

```
# local developement
python3 manage.py runserver --settings=config.settings.debug
```