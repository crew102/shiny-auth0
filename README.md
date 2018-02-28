# Auth0 + Shiny proxy

Adapted from https://github.com/auth0/shiny-auth0 to accomdate use of docker secrets

.env file must contain the following env vars (with correct values):

````bash
AUTH0_DOMAIN=myCoolDomain
AUTH0_CALLBACK_URL=https://my.url.com/
SHINY_HOST=localhost
SHINY_PORT=3838
PORT=3000
````

App will read secret vars from:

/run/secrets/auth0-client-secret
/run/secrets/auth0-client-id
/run/secrets/cookie-secret

Which are mapped into docker container by docker secrets
