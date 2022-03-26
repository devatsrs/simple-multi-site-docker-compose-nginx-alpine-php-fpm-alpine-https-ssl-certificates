# WebServer

## Prerequisites

```
    mkcert -install

```

## Create a ssl for domain

```

    cd sites/localhost.test
    mkcert -install
    mkcert localhost.test 127.0.0.1 ::1

```

## files geenrated

```
    \sites\localhost.test\certificates\localhost.test.key
    sites\localhost.test\certificates\localhost.test.pem

```

## Setup generated file in sites\localhost.test\site.conf

```

    listen 443 ssl;
    # Path used in docker-compose.yml
    ssl_certificate /etc/nginx/sites/localhost.test/certificates/localhost.test.pem;
    ssl_certificate_key /etc/nginx/sites/localhost.test/certificates/localhost.test.key;


```
## Todos
    - .env file
    - multi version php, mysql
    - Add Apache 
    - Redis
    - Email
    