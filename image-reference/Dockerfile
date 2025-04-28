## Build Vue JS App
FROM node:14.20.1-alpine AS build

ENV VUE_URL="https://github.com/creativetimofficial/vue-black-dashboard.git"
WORKDIR /app

RUN apk update \
    && apk upgrade \
    && apk add git \
    && rm -rf /var/cache/apk \
    && rm -rf /var/lib/apk

RUN <<EOT
    git clone ${VUE_URL}
    cd /app/vue-black-dashboard
    npm install
    npm run build
EOT

## Create Image with Vue JS App
FROM nginx:1.28.0-alpine AS artifact

LABEL autor="xNibble" \
    contact="info@xnibble.com" \
    version="v0.0.1" \
    description="Image with several sentences for Dockerfile"

WORKDIR /usr/share/nginx/html

COPY --from=build /app/vue-black-dashboard/dist .

EXPOSE 80

ENTRYPOINT ["nginx","-g","daemon off;"]
