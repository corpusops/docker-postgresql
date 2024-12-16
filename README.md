# library images on steroids for postgresql/postgis/pgrouting

DISCLAIMER
============

**UNMAINTAINED/ABANDONED CODE / DO NOT USE**

Due to the new EU Cyber Resilience Act (as European Union), even if it was implied because there was no more activity, this repository is now explicitly declared unmaintained.

The content does not meet the new regulatory requirements and therefore cannot be deployed or distributed, especially in a European context.

This repository now remains online ONLY for public archiving, documentation and education purposes and we ask everyone to respect this.

As stated, the maintainers stopped development and therefore all support some time ago, and make this declaration on December 15, 2024.

We may also unpublish soon (as in the following monthes) any published ressources tied to the corpusops project (pypi, dockerhub, ansible-galaxy, the repositories).
So, please don't rely on it after March 15, 2025 and adapt whatever project which used this code.




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


