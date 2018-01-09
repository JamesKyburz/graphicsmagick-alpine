# graphicsmagick alpine image with webp support

[dockerhub](https://hub.docker.com/r/jameskyburz/graphicsmagick-alpine/)

## example dockerfile using multi-stage builds

```
FROM jameskyburz/graphicsmagick-alpine:v1.0.0 as gm
FROM jameskyburz/node:8.9.4-alpine

COPY --from=gm /usr/ /usr/

USER node

ENTRYPOINT ["node", "src/index"]
CMD []

EXPOSE 5000
```



