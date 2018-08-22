<!SLIDE>

## Octobox layout

    @@@ render-diagram
    graph LR
      octobox-service(octobox-service type=LoadBalancer)
      octobox-deployment
      octobox-ingress{octobox-ingress}
      postgresql-service(postgresql-service type=ClusterIP)
      postgresql-deployment
      redis-service(redis-service type=ClusterIP)
      redis-deployment
      traefik{traefik}

      subgraph octobox-namespace
        octobox-deployment ==> octobox-service
        postgresql-deployment ==> postgresql-service
        redis-deployment ==> redis-service
      end

      octobox-ingress ==> traefik
