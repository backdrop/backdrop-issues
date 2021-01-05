
Backdrop Core Commit Procedure
==============================

For a particular pull request (PR):

* Make sure the logic is sound and simple
* Make sure it meets Backdrop's [coding & documentation standards](https://api.backdropcms.org/documentation/coding-and-documentation-standards)
* Make sure it passes automated tests
  * Assess whether it needs a new test(s) (usually when it introduces new functionality)
* Test the PR manually in the PR sandbox
* Test the PR manually in your local environment
  * Verify the problem (e.g. check `/admin/reports/dblog` for errors/warnings)
  * Pull down the PR or apply the patch
  * Verify the fix/feature
* Make sure you're familiar with the [merging guidelines](https://gist.github.com/quicksketch/d633d8f850fd11b2ef5f222aa0a3b5af) (summarized below)
* Merge into `1.x`
  * Use the 'Squash and merge' button in the PR
  * Make sure the commit message follows the pattern: `Issue #XXXX: Fix type on /admin/blah.` (it should be a complete sentence)
  * Add a commit description giving credit to the people involved (e.g. `By @jenlampton, @quicksketch & @klonos`)
* Bug fixes/tasks also get merged into the latest version branch (`1.y.x`)
  * ```php
    # Make sure 1.y.x is up-to-date
    git checkout 1.y.x
    git pull backdrop 1.y.x
    # Pull down latest commits on 1.x.
    git fetch backdrop
    git cherry-pick [commit-hash]
    git push backdrop 1.y.x
    ```
* Post a message in the PR saying which branches it's been merged into
* Post a message in the linked issue thanking everyone involved (by name) and mentioning which PR was merged and into which branches.
