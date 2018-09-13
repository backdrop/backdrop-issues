
Update Official Backdrop CMS Docker Image
---

##### 1. Update the backdrop-ops/docker image https://github.com/backdrop-ops/backdrop-docker

* Update  `ENV` for `BACKDROP_VERSION` to the new release tag
  * [ ] Update `1/apache/Dockerfile` with the new version string
  * [ ] Update `1/fpm/Dockerfile` with the new version string
* Update `ENV` for `BACKDROP_MD5` to the new md5 hash
  * [ ] Download the "Source code" instead of the official release
  * [ ] Run `md5 {filename}.tar.gz`
    * This will output the new md5 hash
  * [ ] Update `1/apache/Dockerfile` with the new MD5 hash
  * [ ] Update `1/fpm/Dockerfile` with the new MD5 hash
* [ ] File an issue + PR against https://github.com/backdrop-ops/backdrop-docker
  * Travis tests must pass!
* [ ] Merge `PR`
* [ ] Note merge commit hash for official docker-library


##### 2. Tell the Docker official images to build against the latest source

* A PR needs to be submitted against the [official docker-images repo](https://github.com/docker-library/official-images/blob/master/library/backdrop)

The lines in the file take the general form:

```
DOCKER_TAG: git://SOURCE_REPO@COMMIT_HASH RELATIVE_PATH_TO_DOCKERFILE
```

Example

```
1.3.4: git://github.com/backdrop-ops/backdrop-docker@ce9edf32f4263d00181cc58a5fb23437316675b3 1/apache
1.3: git://github.com/backdrop-ops/backdrop-docker@ce9edf32f4263d00181cc58a5fb23437316675b3 1/apache
1: git://github.com/backdrop-ops/backdrop-docker@ce9edf32f4263d00181cc58a5fb23437316675b3 1/apache
1.3.4-apache: git://github.com/backdrop-ops/backdrop-docker@ce9edf32f4263d00181cc58a5fb23437316675b3 1/apache
1.3-apache: git://github.com/backdrop-ops/backdrop-docker@ce9edf32f4263d00181cc58a5fb23437316675b3 1/apache
1-apache: git://github.com/backdrop-ops/backdrop-docker@ce9edf32f4263d00181cc58a5fb23437316675b3 1/apache
apache: git://github.com/backdrop-ops/backdrop-docker@ce9edf32f4263d00181cc58a5fb23437316675b3 1/apache
latest: git://github.com/backdrop-ops/backdrop-docker@ce9edf32f4263d00181cc58a5fb23437316675b3 1/apache

1.3.4-fpm: git://github.com/backdrop-ops/backdrop-docker@ce9edf32f4263d00181cc58a5fb23437316675b3 1/fpm
1.3-fpm: git://github.com/backdrop-ops/backdrop-docker@ce9edf32f4263d00181cc58a5fb23437316675b3 1/fpm
1-fpm: git://github.com/backdrop-ops/backdrop-docker@ce9edf32f4263d00181cc58a5fb23437316675b3 1/fpm
fpm: git://github.com/backdrop-ops/backdrop-docker@ce9edf32f4263d00181cc58a5fb23437316675b3 1/fpm
```

* [ ] Update the commit hashes with the merge commit hash from 1
  * Each entry will end up corresponding to the "Supported tags and respective Dockerfile links" posted over on [DOCKER HUB](https://hub.docker.com/r/library/backdrop)

* TODO: format the docker-library/official-images file to docker standards
