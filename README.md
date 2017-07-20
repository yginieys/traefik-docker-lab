# traefik-docker-lab

1) Start traefik
> docker-compose up -d

See traefik console
> http://localhost:8080/

3) Start drupal site1
> cd site1
> docker-compose up -d

See site1
> http://drupal.docker.localhost/

Make a change in site name.

4) Start drupal site 2
> cd site2
> docker-compose up -d

Reload http://drupal.docker.localhost/ multiple times
Should see site name change => Load balancing

6) Stop site1
> cd site2
> docker-compose stop

Reload http://drupal.docker.localhost/ multiple times
No error, see only site1 => failover.

