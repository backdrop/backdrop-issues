Create a Meta Issue to Capture Relevant Cross Ports from Drupal
--------

Issue this `git` command to get the markdown for the issue:

```bash
git log 7.44..7.50 --reverse --no-merges --pretty=format:"- [ ] | #xx | [%h](http://drupalcode.org/project/drupal.git/commit/%H) | [%s](http://drupal.org/node/)" > my_tmp_markdown_file.md
```

Replacre the `7.44` and `7.50` tags with the relavant tags for the issue you are making.

Fix Up the Markdown File with links to issues
------

Open the `my_tmp_markdown_file.md` and do a find replace with the folling regex:

```
@TODO: Get regex out of Nate's Head and into docs.
```
