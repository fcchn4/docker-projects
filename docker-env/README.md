# POC CONFIG FILES WITH ENV VARS

## Commands

- Docker command without envs.

```bash
docker build -t tmp:v1 \
--build-arg APITOKEN_ENV="ControlValues" \
--build-arg APIEMAIL_ENV="EmailValues" \
--build-arg APIURL_ENV="http://thisisaurl.com" \
--no-cache .
```

- Docker commands with env vars.

```bash
export VALUE1="estoEsUnToken"
export VALUE2="esto@esunemail.com"
export VALUE3="http://envvalues.com"

docker build -t tmp:v1 \
--build-arg APITOKEN_ENV=${VALUE1} \
--build-arg APIEMAIL_ENV=${VALUE2} \
--build-arg APIURL_ENV=${VALUE3} \
--no-cache .
```
