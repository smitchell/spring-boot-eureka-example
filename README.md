### Spring Cloud Discovery Service

This project provides discovery services for my pcf dev integration tests. For example, you can use this project with these three projects:

1) [https://github.com/smitchell/cloud-foundry-angular-example](https://github.com/smitchell/cloud-foundry-angular-example)
2) [https://github.com/smitchell/spring-boot-netflix-zuul-proxy](https://github.com/smitchell/spring-boot-netflix-zuul-proxy)
3) [https://github.com/smitchell/spring-security-5-upgrade_sso-auth-server](https://github.com/smitchell/spring-security-5-upgrade_sso-auth-server)

## How do you run this?

Start pcf dev and sign in as "user"/"pass".

```
cf dev start
cf login -a https://api.local.pcfdev.io --skip-ssl-validation
```

Clone the project, change to the project directory, built it, and push it to pcf dev.

```
git clone https://github.com/smitchell/spring-boot-eureka-example
cd [path-to-project]/spring-boot-eureka-example
mvn clean install
cf push
```

Verify the Discovery Service is running and then checkout the Eureka Console
1) Open your local [https://apps.local.pcfdev.io/](https://apps.local.pcfdev.io/) and login with "user"/"pass".
2) Navigate to the pcfdev-space. The discovery-service should be running with a route of [http://discovery-service.local.pcfdev.io/](http://discovery-service.local.pcfdev.io/)
3) Click the "discovery-service" hyperlink to open the app settings.
4) Select the Logs tab. -- OR --
5) Open the Eureka Console at [http://discovery-service.local.pcfdev.io/](http://discovery-service.local.pcfdev.io/)

## Deploy some other services

Checkout, build an deploy the services listed above.