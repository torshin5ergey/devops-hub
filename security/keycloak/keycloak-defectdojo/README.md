# SAML

## References

- https://docs.defectdojo.com/en/customize_dojo/user_management/configure_sso/#keycloak

`docker-compose.yaml`
```yaml
uwsgi:
  environment:
    DD_SESSION_COOKIE_SECURE: 'True'
    DD_CSRF_COOKIE_SECURE: 'True'
    DD_SECURE_SSL_REDIRECT: 'True'
    DD_SOCIAL_AUTH_KEYCLOAK_OAUTH2_ENABLED: 'True'
    DD_SOCIAL_AUTH_KEYCLOAK_PUBLIC_KEY: <KEYCLOAK_REALM_PUBLIC_KEY> # https://keycloak.dev.ctc.ru/realms/<REALM>/protocol/saml/descriptor
    DD_SOCIAL_AUTH_KEYCLOAK_KEY: <KEYCLOAK_CLIENT_ID>
    DD_SOCIAL_AUTH_KEYCLOAK_SECRET: <KEYCLOAK_CLIENT_SECRET>
    DD_SOCIAL_AUTH_KEYCLOAK_AUTHORIZATION_URL: 'http://keycloak.dev.ctc.ru/realms/<REALM>/protocol/openid-connect/auth'
    DD_SOCIAL_AUTH_KEYCLOAK_ACCESS_TOKEN_URL: 'http://keycloak.dev.ctc.ru/realms/<REALM>/protocol'
    # DD_SOCIAL_AUTH_KEYCLOAK_LOGIN_BUTTON_TEXT: customize the login button’s text caption
```
