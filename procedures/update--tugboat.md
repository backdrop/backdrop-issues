Backdrop CMS Tugboat Repository
----

This file contains instructions to deploy a new Backdrop CMS release tag to the `/backdrop-ops/backdrop-tugboat` source repository.

Tugboat is used to provide demo sandboxes at https://backdropcms.org/demo/create.

Setting up the Tugboat Repository
---
* Clone the [`backdrop-tugboat`](https://github.com/backdrop-ops/backdrop-tugboat) repo to your local dev environment.
  * `git clone git@github.com:backdrop-ops/backdrop-tugboat.git`
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

* Change directories to your clone of the `backdrop-ops/backdrop-tugboat` repo
  * `cd {path/to/backdrop-tugboat}`
* Pull down the changes from `backdrop/backdrop` repo
  * `git fetch core`
* Checkout the master branch of `backdrop-ops/backdrop-tugboat`
  * `git checkout master`
* Merge the latest Backdrop release tag into `master`
  * You can list the tags with `git tag -l`
  * If for example we are releasing version `1.5.1` the command would be:
    * `git merge 1.5.1`
* Now push to the `backdrop-ops/backdrop-tugboat` repo
  * `git push origin master`
* The new release of Backdrop CMS is now on Tugboat. It normally takes 24 hours for new demos to be affected. To immediately make new demos use the new version see the next section.

Rebuild the Current Tugboat Image
---

* Log into Tugboat at https://dashboard.tugboat.qa/ use your GitHub credentials.
* If necessary, request access to the backdrop-tugboat repository.
* Visit https://dashboard.tugboat.qa/5bdb5c268eabd5000137a87b to get to the Tugboat Dashboard for the Demo Sites.
* Under the "Base Preview" at the bottom of the page, select "Rebuild..." from the "Actions" dropdown.
* Check both confirmation boxes, "Yes, rebuild this preview" and "Rebuild previews built from this one when finished" note that any in-progress demos will be discarded.


