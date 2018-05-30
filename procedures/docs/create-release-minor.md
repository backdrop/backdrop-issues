DRAFT Steps to create a MINOR release
=====================================


## Pre-release tasks

- [ ] Merge commits (assign to quicksketch / serundeputy / docwilmot)
- [ ] Move all unfinished issues to the next bugfix release milestone @quicksketch, @serundeputy
- [ ] Draft Release notes (assign to serundeputy / quicksketch / jenlampton)
  - [ ] Short, descriptive summary of the release
  - [ ] Note if any changes were made to files outside the `core` directory
  - [ ] Note if updates (update.php) needs to be run
  - [ ] Include changelog since last version (generated with drush rn)


## Release tasks

- [ ] Update bootstrap.inc with version number (assign to quicksketch / serundeputy)
- [ ] Tag for release, and push tag to GitHub (assign to quicksketch / serundeputy)
- [ ] Revert version number back (assign to quicksketch / serundeputy)
- [ ] Create release notes on GitHub (assign to serundeputy / quicksketch / jenlampton)
  - [ ] Double check if any changes were made to files outside the `core` directory
- [ ] Unpublish preview release on backdropcms.org (assign to serundeputy / quicksketch / jenlampton)
- [ ] Update the front page download link on b.org (assign to serundeputy / quicksketch / jenlampton / klonos)
- [ ] Tweet that a new release is out (assign to quicksketch / jenlampton / jimbirch)


## Post-release tasks

- [ ] Push the minor release to the [Pantheon repository](https://github.com/backdrop-ops/backdrop-pantheon) (assign to quicksketch / serundeputy)
- [ ] Push the minor release to the [Platform.sh repository](https://github.com/platformsh/platformsh-example-backdrop) (@serundeputy)
- [ ] Push the minor release to the [Docker repository](https://github.com/docker-library/official-images/blob/master/library/backdrop) (@jenlampton)
- [ ] Publish blog post (assign to tomgrandy / klonos / jenlampton / quicksketch)
- [ ] Send a newsletter via MailChimp (assign to facetinteractive / tomgrandy / jenlampton)
- [ ] email katie@phpweekly.com for a note in the PHP Weekly Newsletter (assign to tomgrandy / klonos / jenlampton)
- [ ] Update the Wikipedia articles (assign to klonos / jenlampton)
  - [ ] https://en.wikipedia.org/wiki/Backdrop_CMS
  - [ ] https://en.wikipedia.org/wiki/List_of_content_management_systems


See the Accompanying Bug-Fix Release Checklist
----------------------------------------------
