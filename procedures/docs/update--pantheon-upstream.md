Backdrop CMS Pantheon Upstream
----

Instructions to deploy a new Backdrop CMS release tag to the `/backdrop-ops/backdrop-pantheon` upstream.

Tracking Backdrop Pantheon Upstream and Core
---
* Clone the `backdrop-pantheon` repo to your local dev environment
  * `git clone git@github.com:backdrop-ops/backdrop-pantheon.git`
  * Add `/backdrop/backdrop` as a tracked remote
    * `git remote add core git@github.com:backdrop/backdrop.git`

* The resulting `.git/config` should have an entry like this:

```
[remote "core"]
        url = git@github.com:backdrop/backdrop.git
        fetch = +refs/heads/*:refs/remotes/core/*
```

Deploy a Release
---

* Change directories to your clone of the `backdrop-ops/backdrop-pantheon` repo
  * `cd {path/to/backdrop-pantheon}`
* Pull down the changes from `backdrop/backdrop` repo
  * `git fetch core`
* Checkout the master branch of `backdrop-ops/backdrop-pantheon`
  * `git checkout master`
* Merge the latest Backdrop release tag into `master`
  * You can list the tags with `git tag -l`
  * If for example we are releasing version `1.5.1` the command would be:
    * `git merge 1.5.1`
* Now push to the `backdrop-ops/backdrop-pantheon` repo
  * `git push origin master`
* The new release of Backdrop CMS is now available to Pantheon users!
