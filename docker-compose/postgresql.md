
## Set up PostgreSQL with permanent volume

### Objective
In one of my projects, we use PostgreSQL with Django. Every time we restart the 

### Database service
There are numerous ways to set up PostgreSQL with docker-compose and it is well-documented. Here we use the configuration from the official documentation:

```yml
version: '3.8'
services:
  database:
    container_name: db
    image: your-repo/db-image
    expose:
    - 5432
    volumes:
    - unimorph-db:/var/lib/postgresql/data
```

