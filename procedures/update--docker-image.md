
## Update Official Backdrop CMS Docker Image
---

### 1. Update the backdrop-ops/docker image https://github.com/backdrop-ops/backdrop-docker

* [ ] File an [issue](https://github.com/backdrop-ops/backdrop-docker/issues)

You will need 2 things:
1. The release tag of the [latest stable Backdrop version](https://github.com/backdrop/backdrop/releases/latest) (which is usually the same as the Backdrop version).
2. The md5 hash of the [latest stable Backdrop release](https://github.com/backdrop/backdrop/releases/latest):
  2.1 Download the "Source code" .tar.gz file - NOT the .zip file (it is usually the last item in the list of links bellow the "Assets" section).
  2.1 Run `md5 {filename}.tar.gz`
  2.2 Make and note of the generated md5 hash

* [ ] Update the 2 dockerfiles:
  * [ ] Update `1/apache/Dockerfile`:
    * [ ] Update `ENV BACKDROP_VERSION` to the new release tag (point 1 above)
    * [ ] Update `ENV BACKDROP_MD5` to the new md5 hash (point 2.2 above)
  * [ ] Update `1/fpm/Dockerfile`:
    * [ ] Update `ENV BACKDROP_VERSION` to the new release tag (point 1 above)
    * [ ] Update `ENV BACKDROP_MD5` to the new md5 hash (point 2.2 above)
* [ ] Create a Pull Request against https://github.com/backdrop-ops/backdrop-docker
  * [ ] If Travis tests pass -- Merge the PR
  * [ ] Make a note of the merge commit hash, as you will need it for updating the official docker-library (see next section)

#### Update the README in https://github.com/backdrop-ops/backdrop-docker

* Edit https://github.com/backdrop-ops/backdrop-docker/blob/master/README.md
  * [ ] Update the version numbers in the "Supported tags and respective Dockerfile links" section at the top
  * [ ] more???

### 2. Tell the Docker official images to build against the latest source

* A PR needs to be submitted against the [official docker-images repo](https://github.com/docker-library/official-images/blob/master/library/backdrop)

- [ ] Update the 2 lines starting with  `Tags:`, so to reflect the latest version of Backdrop.
    For example, change from this:

    `Tags: 1.13.1, 1.13, 1, 1.13.1-apache, 1.13-apache, 1-apache, apache, latest`

    ...to this:

    `Tags: 1.13.2, 1.13, 1, 1.13.2-apache, 1.13-apache, 1-apache, apache, latest`

- [ ] Update the git commit:
  - [ ] Make sure that the PR you have filed in the previous section has been committed
    -> Head to the [commits list](https://github.com/backdrop-ops/backdrop-docker/commits/master) of the https://github.com/backdrop-ops/backdrop-docker repo.
    -> Click on the latest commit which updated the dockerfiles
    -> the full commit hash should be located at the top-right of the page, below the "Browse files" button.
  - [ ] Use the commit hash from the previous step, to update the 2 lines starting with `GitCommit:`

In order to help the Docker Library maintainers review and merge the PR, make sure to add as much useful info in the PR summary, such as:

* a link to the latest release of Backdrop
* a link to the latest commit in https://github.com/backdrop-ops/backdrop-docker/commits/master
