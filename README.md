# WebServer

## Prerequisites

```
    mkcert -install

```

## Create a ssl for domain

```

    cd sites/ers.test
    mkcert -install
    mkcert ers.test 127.0.0.1 ::1

```

## files geenrated

```
    \sites\ers.test\certificates\ers.test.key
    sites\ers.test\certificates\ers.test.pem

```

## Setup generated file in sites\ers.test\site.conf

```

    listen 443 ssl;
    # Path used in docker-compose.yml
    ssl_certificate /etc/nginx/sites/ers.test/certificates/ers.test.pem;
    ssl_certificate_key /etc/nginx/sites/ers.test/certificates/ers.test.key;


```

## Todos

    - .env file
    - multi version php, mysql
    - Add Apache
    - Redis
    - Email

## Commands used

    docker-compose up -d
    docker-compose down
    
