# jenkins-docker-test

Based on work from [Evheniy Bystrov on Hackernoon](https://hackernoon.com/continuous-delivery-of-react-app-with-jenkins-and-docker-8a1ae1511b86)

Converted to [Jenkins BlueOcean](https://jenkins.io/doc/book/blueocean) because that's apparently the new hotness in Jenkins land.

# Usage
## Startup

    docker-compose up -d

### getting the initial key

    docker-compose run --rm jenkins-blueocean \
      cat /var/jenkins_home/secrets/initialAdminPassword

## Shutdown

To just stop the containers:

    docker-compose stop

To nuke the persistent data as well:

    docker-compose down --volumes

To remove even the cached images:

    docker-compose down --rmi all
