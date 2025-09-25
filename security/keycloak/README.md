# Keycloak

Basic Keycloak install/setup/deploy.

**Table of Contents:**
- [References](#references)
- [Docker deploy](#docker-deploy)
- [Author](#author)

## References

- [Getting Started With Keycloak Identity Provider (free Identity Server alternative by Milan Jovanović)](https://www.youtube.com/watch?v=fvxQ8bW0vO8)
- [How do I create a permanent admin account in Keycloak 26.0.0?](https://github.com/keycloak/keycloak/discussions/33803)
- [All configuration](https://www.keycloak.org/server/all-config)
- [Keycloak Account Console Status Code: 403 Forbidden ](https://keycloak.discourse.group/t/status-code-403-forbidden/10854/2)

## Docker deploy

- Go to project directory
```bash
cd security/keycloak
```
- Build Docker container
```bash
docker build -t cnd-keycloak .
```
- Setup preferred databse and edit config parameters for database in `keycloak.conf`
- Run Docker container
```bash
docker run \
  --name cnd-keycloak \
  -p 8080:8080 \
  -v ./keycloak.conf:/opt/keycloak/conf/keycloak.conf:ro \
  cnd-keycloak \
  start --optimized
```
- Access with web browser `http://localhost:8080` with `bootstrap-admin:qwerty` credentials

## Author

Sergey Torshin [@torshin5ergey](https://github.com/torshin5ergey)
