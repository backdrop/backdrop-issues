Steps to create a BUG-FIX release
==================================


## Pre-release tasks

- [ ] Merge commits (assign to quicksketch / serundeputy / docwilmot)
- [ ] Create a new bugfix release (assign to quicksketch / serundeputy)
- [ ] Create the next bugfix milestone (assign to quicksketch / serundeputy / jenlampton)
- [ ] Move all unfinished issues to the next bugfix release milestone (assign to quicksketch / serundeputy / jenlampton)
- [ ] Draft Release notes (assign to serundeputy / quicksketch / jenlampton)
  - [ ] Short, descriptive summary of the release
  - [ ] Note if any changes were made to files outside the `core` directory
  - [ ] Note if updates (update.php) needs to be run
  - [ ] Include changelog since last version (generated with drush rn)
- If this is a security release:
  - [ ] Draft Security Advisory (assign to serundeputy / quicksketch / jenlampton)

## Release tasks

- [ ] Update bootstrap.inc with version number (assign to quicksketch / serundeputy)
- [ ] Tag for release, and push tag to GitHub (assign to quicksketch / serundeputy)
- [ ] Revert version number back (assign to quicksketch / serundeputy)
- [ ] Create release notes on GitHub (assign to serundeputy / quicksketch / jenlampton)
  - [ ] Double check if any changes were made to files outside the `core` directory
- [ ] Update the front page download link on b.org (assign to serundeputy / quicksketch / jenlampton / klonos)
- [ ] Tweet that a new release is out (assign to quicksketch / jenlampton / jimbirch)
- If this is a security release:
  - [ ] Publish Security Advisory on b.org (assign to serundeputy / quicksketch / jenlampton)
  - [ ] Mark the release node on b.org as a security release (assign to serundeputy / quicksketch / jenlampton)

## Post-release tasks

- [ ] Push the bug-fix release to the [Pantheon repository](https://github.com/backdrop-ops/backdrop-pantheon) (assign to serundeputy / quicksketch)
- [ ] Push the bug-fix release to the [Platform.sh repository](https://github.com/platformsh/platformsh-example-backdrop) (assign to serundeputy / quicksketch)
- [ ] Update the Wikipedia articles (assign to klonos / jenlampton)
  - [ ] https://en.wikipedia.org/wiki/Backdrop_CMS
  - [ ] https://en.wikipedia.org/wiki/List_of_content_management_systems
