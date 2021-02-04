# library images on steroids for postgresql/postgis/pgrouting

## images pipelines
```
-> git@docker-postgis(corpusops/postgis-bare)
---> git@docker-pgrouting(corpusops/pgrouting-bare(dep postgis-bare))
-----> git@docker-postgresql
       | corpusops/postgres  (dep: None)
       | corpusops/postgis   (dep: postgis-base)
       | corpusops/pgrouting (dep: pgrouting-base)
```

## Wrapped images
- [docker-images](https://github.com/corpusops/docker-images) compatibles images (original images wrapped with tools)
- also based on
    - [postgis](https://github.com/corpusops/docker-postgis)
    - [pgrouting](https://github.com/corpusops/docker-pgrouting)
- [![.github/workflows/cicd.yml](https://github.com/corpusops/docker-postgresql/workflows/.github/workflows/cicd.yml/badge.svg?branch=master)](https://github.com/corpusops/docker-postgresql/actions?query=workflow%3A.github%2Fworkflows%2Fcicd.yml+branch%3Amaster)

| original   | wrapped  |
|------------|-----------|
| [library/postgres](https://hub.docker.com/_/postgres)                         | [corpusops/postgres](https://hub.docker.com/r/corpusops/postgres)   |
| [corpusops/pgrouting-bare](https://hub.docker.com/r/corpusops/pgrouting-bare) | [corpusops/pgrouting](https://hub.docker.com/r/corpusops/pgrouting) |
| [corpusops/postgis-bare](https://hub.docker.com/r/corpusops/postgis-bare)     | [corpusops/postgis](https://hub.docker.com/r/corpusops/postgis)     |

