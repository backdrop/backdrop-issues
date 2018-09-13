
Backdrop Core Commit Procedure
==============================

* Choose an issue
  * Make sure it meets [coding standards](https://api.backdropcms.org/coding-standards)
  * Make sure the logic is sound and simple
  * Make sure it passes automated tests
  * Assess whether it needs a new test(s) (usually because it is introducing new functionality)
  * Test the PR manually in the ZenCI sandbox
  * Pull down PR verify problem before PR; and test locally too (for example check /admin/reports/dblog for errors or warnings)
  * Make sure the commit message follows pattern: "Issue #XXXX: Fix type on /admin/blah."
    * Should be complete sentence
  * Feature PRs just get merged to `1.x`, bugs and patches merge to both `1.x` and `cherry-pick` to `1.y.x`


