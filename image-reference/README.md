# Builds

Build image.

```bash
$ docker build -t base/vuejs:v0.0.1 .
```

Inspect image.

```bash
$ docker image inspect --format='{{json .Config.Labels}}' base/vuejs:v0.0.1
```

Create container.

```bash
$ docker run --rm -it -p 8080:80 base/vuejs:v0.0.1
```

## Referencias

- [Vue Black Dashboard](https://github.com/creativetimofficial/vue-black-dashboard?tab=readme-ov-file#).
- [Dockerfile Reference](https://docs.docker.com/reference/dockerfile/#shell).
