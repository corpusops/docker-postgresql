
DISCLAIMER - ABANDONED/UNMAINTAINED CODE / DO NOT USE
=======================================================
While this repository has been inactive for some time, this formal notice, issued on **December 10, 2024**, serves as the official declaration to clarify the situation. Consequently, this repository and all associated resources (including related projects, code, documentation, and distributed packages such as Docker images, PyPI packages, etc.) are now explicitly declared **unmaintained** and **abandoned**.

I would like to remind everyone that this project’s free license has always been based on the principle that the software is provided "AS-IS", without any warranty or expectation of liability or maintenance from the maintainer.
As such, it is used solely at the user's own risk, with no warranty or liability from the maintainer, including but not limited to any damages arising from its use.

Due to the enactment of the Cyber Resilience Act (EU Regulation 2024/2847), which significantly alters the regulatory framework, including penalties of up to €15M, combined with its demands for **unpaid** and **indefinite** liability, it has become untenable for me to continue maintaining all my Open Source Projects as a natural person.
The new regulations impose personal liability risks and create an unacceptable burden, regardless of my personal situation now or in the future, particularly when the work is done voluntarily and without compensation.

**No further technical support, updates (including security patches), or maintenance, of any kind, will be provided.**

These resources may remain online, but solely for public archiving, documentation, and educational purposes.

Users are strongly advised not to use these resources in any active or production-related projects, and to seek alternative solutions that comply with the new legal requirements (EU CRA).

**Using these resources outside of these contexts is strictly prohibited and is done at your own risk.**

This project has been transfered to Makina Corpus <freesoftware@makina-corpus.com> ( https://makina-corpus.com ). This project and its associated resources, including published resources related to this project (e.g., from PyPI, Docker Hub, GitHub, etc.), may be removed starting **March 15, 2025**, especially if the CRA’s risks remain disproportionate.

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


