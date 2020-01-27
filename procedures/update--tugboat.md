Backdrop CMS Tugboat Repository
----

This file contains instructions to deploy a new Backdrop CMS release tag to the
`/backdrop-ops/backdrop-tugboat` source repository.

[Tugboat](https://tugboat.qa) is used to provide demo sandboxes at
https://backdropcms.org/demo/create.

Forking the `/backdrop-ops/backdrop-tugboat` repo
---
Skip to the next step if you have previously created a fork of the repo.

Visit https://github.com/backdrop-ops/backdrop-tugboat and use the "Fork" button
at the top-right.

Setting up the Backdrop CMS Tugboat repository on your local.
---
* Clone your fork of the `backdrop-tugboat` repo to your local dev environment
  (in the command below, replace the `[your-github-username]` with your actual
  GitHub username):

  `git clone https://github.com/[your-github-username]/backdrop-tugboat`

* Switch to the cloned repo:

  `cd backdrop-tugboat`

* Add [`/backdrop/backdrop`](https://github.com/backdrop/backdrop) as a tracked
  remote:

  `git remote add core https://github.com/backdrop/backdrop`

* Add [`/backdrop-ops/backdrop-tugboat`](https://github.com/backdrop-ops/backdrop-tugboat)
  as a tracked remote:

  `git remote add upstream https://github.com/backdrop-ops/backdrop-tugboat`

* Verify that the remotes have been added properly:

  `git remote -v`

  ...the output of the above command should like this:

```
core      https://github.com/backdrop/backdrop (fetch)
core      https://github.com/backdrop/backdrop (push)
origin    https://github.com/[your-github-username]/backdrop-tugboat (fetch)
origin    https://github.com/[your-github-username]/backdrop-tugboat (push)
upstream  https://github.com/backdrop-ops/backdrop-tugboat (fetch)
upstream  https://github.com/backdrop-ops/backdrop-tugboat (push)
```

Updating your version of the Backdrop CMS Tugboat repository.
---

`git fetch upstream && git merge upstream/master && git push`

Updating your local Tugboat repo with the latest realeas of Backdrop core
---

* `git fetch core`

* Run `git merge core/[latest-tag]`, replacing the `[latest-tag]` bit with the
  actual number of the latest Backdrop CMS version. For example:

  `git merge 1.15.0`

* Run the following command, to check if there are any conflicts:

  `git diff --diff-filter=U`

  If there are conflicts, resolve them using a text editor.

* Once you have confirmed that there are no conflicts, add the changes, commit,
  and finally push:

  `git add .`

  `git commit -m "Updated core to 1.15.0"`

  `git push`

* Head over to GitHub, and create a pull request against the master branch of
  https://github.com/backdrop-ops/backdrop-tugboat (in the URL below, replace
  the `[your-github-username]` bit with your actual GitHub username):

  https://github.com/backdrop-ops/backdrop-tugboat/compare/master...[your-github-username]:master

Merge the pull request.
---

Head over to https://gitter.im/backdrop/backdrop-issues and let people know that
you have created a pull request. Someone from the Backdrop CMS team with commit
access will review and merge your pull request.

Once the pull request has been merged, the new release of Backdrop CMS will now
be on Tugboat. *It normally takes 24 hours for new demos to be affected*. To
have the new version made immediately available for new demos, see the next
section.

Rebuild the Current Tugboat Image
---

* Log into Tugboat at https://dashboard.tugboat.qa/ use your GitHub credentials.
* If necessary, request access to the backdrop-tugboat repository.
* Visit https://dashboard.tugboat.qa/5bdb5c268eabd5000137a87b to get to the
  Tugboat Dashboard for the Demo Sites.
* Under the "Base Preview" at the bottom of the page, select "Rebuild..." from
  the "Actions" dropdown.
* Check both confirmation boxes, "Yes, rebuild this preview" and "Rebuild
  previews built from this one when finished" note that any in-progress demos
  will be discarded.
