DRAFT Steps to create a MINOR release
=====================================
(assignments below are in order of prefernence from left to right)
---
Issue Title:   Backdrop 1.1x.x Release checklist
---

Scheduled for January/September/May 15, 20xx 10am - 4pm PT

## Pre-release tasks

- [ ] Merge commits (assign to quicksketch / serundeputy / herbdool)
- [ ] Create a new minor release milestone (assign to klonos / jenlampton / herbdool / serundeputy / quicksketch)
- [ ] Move all unfinished issues to the next minor release milestone (assign to klonos / jenlampton / herbdool / serundeputy / quicksketch)
- [ ] Draft Release notes (assign to jenlampton / herbdool / serundeputy / quicksketch)
  - [ ] Short, descriptive summary of the release
  - [ ] Note if any changes were made to files outside the `core` directory
  - [ ] Note if updates (update.php) needs to be run
    - Use the text "The database update script does **not** need to be run."
    - or "It will be necessary to run the update script (located at /update.php) for this release."
  - [ ] Include changelog since last version (generated with drush rn)
- [ ] Draft blog post (assign to stpaultim / tomgrandy / klonos / jenlampton)
- [ ] Draft roadmap updates for backdropcms.org (assign to stpaultim / klonos / jenlampton)


## Release tasks

- [ ] Update bootstrap.inc with version number (assign to quicksketch / serundeputy / herbdool)
- [ ] Tag for release, and push tag to GitHub (assign to quicksketch / serundeputy / herbdool)
- [ ] Branch for new minor number (e.g. `1.10.x`) and push to GitHub (assign to quicksketch / serundeputy / herbdool)
- [ ] Revert version number back on 1.x branch with minor number increased (e.g. `1.11.x-dev`) (assign to quicksketch / serundeputy / herbdool)
- [ ] Revert version number back on new minor number branch (e.g. `1.10.x-dev`) (assign to quicksketch / serundeputy / herbdool)
- [ ] Create release notes on GitHub (assign to jenlampton / herbdool / serundeputy / quicksketch)
- [ ] Unpublish preview release on backdropcms.org (assign to stpaultim / klonos / jenlampton / serundeputy / herbdool / quicksketch)
- [ ] Update the front page download link on b.org (assign to stpaultim / klonos / jenlampton / serundeputy / herbdool / quicksketch)
- [ ] Tweet that a new release is out (assign to stpaultim / jimbirch / jenlampton / quicksketch)


## Post-release tasks

- [ ] Push the minor release to the [Pantheon repository](https://github.com/backdrop-ops/backdrop-pantheon) (assign to herbdool / serundeputy / quicksketch)
- [ ] Push the minor release to the [Platform.sh Backdrop repository](https://github.com/platformsh/platformsh-example-backdrop) (assign to serundeputy / jenlampton)
- [ ] Push the minor release to the [Docker repository](https://github.com/docker-library/official-images/blob/master/library/backdrop) (assign to drupol / jenlampton / serundeputy)
- [ ] Push the minor release to the [TugBoat Backdrop repository](https://github.com/backdrop-ops/backdrop-tugboat) (assign to serundeputy / herbdool / quicksketch / jenlampton)
- [ ] Update backdropcms.org to use the latest TugBoat (assign to quicksketch)
- [ ] Publish blog post (assign to stpaultim / tomgrandy / klonos / jenlampton)
- [ ] Send a newsletter via MailChimp (assign to facetinteractive / stpaultim / tomgrandy / jenlampton)
- [ ] email katie@phpweekly.com for a note in the PHP Weekly Newsletter (assign to stpaultim / tomgrandy / klonos / jenlampton)
- [ ] Publish roadmap updates for backdropcms.org (assign to stpaultim / klonos / jenlampton)
- [ ] Update the Wikipedia articles (assign to stpaultim / klonos / jenlampton)
  - [ ] https://en.wikipedia.org/wiki/Backdrop_CMS
  - [ ] https://en.wikipedia.org/wiki/List_of_content_management_systems


See the Accompanying Bug-Fix Release Checklist
----------------------------------------------
