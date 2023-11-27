README
=======

### Develop requirements
    * python 3.11
    * poetry
    * docker-compose

### Use poetry to manage project, check poetry for usage details
```
poetry env use 3.11
poetry install --sync --no-root
```

### Start/Stop develop environment
```
make start_dev
make stop_dev
```

### Swagger/Redoc API Documents

* swagger: `http://localhost:8080/docs`
* redoc: `http://localhost:8080/redoc`

### Configuration 
application is configed by environments. Most of them have default values. Check docker-compose.yml for the values needed to be set
```
    TESTING: Optional[str] = None
    API_STR: str = "/api"
    PROJECT_NAME: str = 'tvmaze'
    API_KEY: str = secrets.token_urlsafe(64)
    SECRET_KEY: str = secrets.token_urlsafe(32)
    DEFAULT_JOB_COUNTRY: str = 'US'
    SQLALCHEMY_DATABASE_URI: str = 'sqlite://'
    REDIS_HOST: Optional[str] = None
    REDIS_PORT: int = 6379
    ACCESS_TOKEN_EXPIRE_MINUTES: int = 60 * 24 * 7
    SMTP_TLS: bool = True
    SMTP_PORT: Optional[int] = None
    SMTP_HOST: Optional[str] = None
    SMTP_USER: Optional[str] = None
    SMTP_PASSWORD: Optional[str] = None
    EMAILS_FROM_EMAIL: Optional[EmailStr] = None
    EMAILS_FROM_NAME: Optional[str] = None
    EMAIL_TO: Optional[EmailStr] = None
```

### Start/Stop application
```
make start
make stop
```

### Generate sample data
```
make gen_sample
```

### Unit test
```
make test
```
