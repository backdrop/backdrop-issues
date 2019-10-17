DRAFT Steps to create a MINOR PREVIEW release
=====================================

(assignments below are in order of prefernence from left to right)

---
Issue Title:   Backdrop 1.1x.x Preview Release checklist
---

Scheduled for January/September/May 1st, 20xx 10am - 4pm PT

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


## Pre-release Publicity + documentation tasks

- [ ] Draft blog post (assign to stpaultim / tomgrandy / klonos / jenlampton)
- [ ] Draft roadmap updates for backdropcms.org (assign to stpaultim / klonos / jenlampton)


## Release tasks

- [ ] Update bootstrap.inc with version number (assign to quicksketch / serundeputy / herbdool)
- [ ] Tag for release, and push tag to GitHub (assign to quicksketch / serundeputy / herbdool)
- [ ] Branch for new minor number (e.g. `1.10.x-preview`) and push to GitHub (assign to quicksketch / serundeputy / herbdool)
- [ ] Revert version number back on 1.x branch with minor number increased (e.g. `1.11.x-dev`) (assign to quicksketch / serundeputy / herbdool)
- [ ] Revert version number back on new minor number branch (e.g. `1.10.x-dev`) (assign to quicksketch / serundeputy / herbdool)
- [ ] Create release notes on GitHub (assign to jenlampton / herbdool / serundeputy / quicksketch)


## Post-release Publicity + documentation tasks

- [ ] Tweet that a new release is out (assign to stpaultim / jimbirch / jenlampton / quicksketch)
- [ ] Publish roadmap updates for backdropcms.org (assign to stpaultim / klonos / jenlampton)


See the Accompanying Bug-Fix Release Checklist
----------------------------------------------
