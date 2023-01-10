# djangoflow-df-configurations
Djangoflow configuration management

1. Manage templates
2. Managem templates value
3. Manage configuration files instances (YAML)
4. Saving rendered configuration files onto configurable storage (local, bucket, configmap)


Later the configuration files will be consumed by dnangoflow project with https://github.com/vmware/django-yamlconf

AbstractKeyValue (django-df-kv ?)  model that has key/value (with type? number/string/ pair and can be inherited by different apps

namespace
key
value

Namespace
prefix
parent

e.g. user_profile.gender => namespace = userfile, key gender

e.g. for djangoflow
Project -> ProjectConfig
Environment -> EnvironmentConfig
Deployment -> DeploymentConfig
Notifications -> NotificationChannel -> NotificationChannelConfig

We need a way to cobine the key/values for a combination of Project / Environment / Deployment -> config file data * config template -> config file instance

Yet another application is remote config for a mobile app via /remote_config endpoint
take template, defaults and get_context() will be overriden at the Serializer level(?) -> to generate dynamic app configuation,
  - a/b testing i.e. 50/50 - red backgroud / blue background
  - if male - this, if female - that
  - if app version = 1 -> that
  
