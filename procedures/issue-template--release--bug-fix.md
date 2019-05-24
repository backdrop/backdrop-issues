Steps to create a BUG-FIX release
==================================


## Pre-release tasks

- [ ] Merge commits (assign to quicksketch / serundeputy / herbdool)
- [ ] Create a new bugfix release (assign to quicksketch / serundeputy / herbdool)
- [ ] Create the next bugfix milestone (assign to jenlampton / quicksketch / serundeputy / herbdool)
- [ ] Move all unfinished issues to the next bugfix release milestone (assign to quicksketch / serundeputy / herbdool / jenlampton)
- [ ] Draft Release notes (assign to jenlampton / serundeputy / herbdool / quicksketch)
  - [ ] Short, descriptive summary of the release
  - [ ] Note if any changes were made to files outside the `core` directory
  - [ ] Note if updates (update.php) needs to be run
    - Use the text "The database update script does need to be run."
    - or "It will be necessary to run the update script (located at /update.php) for this release."
  - [ ] Include changelog since last version (generated with drush rn)

If this is a security release:
- [ ] Draft Security Advisories (assign to serundeputy / herbdool / quicksketch / jenlampton)

## Release tasks

- [ ] Update bootstrap.inc with version number (assign to quicksketch / serundeputy / herbdool)
- [ ] Tag for release, and push tag to GitHub (assign to quicksketch / serundeputy / herbdool)
- [ ] Revert version number back (assign to quicksketch / serundeputy / herbdool)
- [ ] Create release notes on GitHub (assign to jenlampton / serundeputy / quicksketch)
- [ ] Update the front page download link on b.org (assign to jenlampton / klonos / stpaultim)
- [ ] Tweet that a new release is out (assign to jenlampton / stpaultim / quicksketch)

If this is a security release:
- [ ] Publish Security Advisories on b.org (assign to jenlampton / serundeputy / herbdool / quicksketch)
- [ ] Mark the release node on b.org as a security release (assign to jenlampton / serundeputy / herbdool / quicksketch )
- [ ] We should [Request a CVE](https://github.com/backdrop/backdrop-issues/blob/master/procedures/security--request-cve.md) - (assign to quicksketch or jenlampton or ?)

## Post-release tasks

- [ ] Push the bug-fix release to the [Platform.sh Backdrop repository](https://github.com/platformsh/platformsh-example-backdrop) (assign to serundeputy or jenlampton)
- [ ] Push the bug-fix release to the [Pantheon Backdrop repository](https://github.com/backdrop-ops/backdrop-pantheon) (assign to serundeputy / quicksketch / herbdool)

If this release does not accompany a minor release:
- [ ] Push the bug-fix release to the [TugBoat Backdrop repository](https://github.com/backdrop-ops/backdrop-tugboat) (assign to serundeputy / quicksketch / jenlampton)
- [ ] Push the bug-fix release to the [Docker Backdrop repository](https://github.com/docker-library/official-images/blob/master/library/backdrop) (assgign to @jenlampton)
- [ ] Update the Wikipedia articles (assign to stpaultim / klonos / jenlampton)
  - [ ] https://en.wikipedia.org/wiki/Backdrop_CMS
  - [ ] https://en.wikipedia.org/wiki/List_of_content_management_systems

If this is a security release:
- [ ] Update the Security Advisory with CVE (assign to quicksketch)
