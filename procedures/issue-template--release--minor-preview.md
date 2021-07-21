DRAFT Steps to create a MINOR PREVIEW release
=====================================

(assignments below are in order of preference from left to right)

---
Issue Title:   Backdrop 1.x.x-preview Release checklist
---

Scheduled for January/May/September 1st, 20xx 10am - 4pm PT

## Pre-release tasks

- [ ] Merge commits (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Create a new minor release milestone (assign to klonos / jenlampton / herbdool / serundeputy / quicksketch)
- [ ] Move all unfinished issues to the next minor release milestone (assign to klonos / jenlampton / herbdool / serundeputy / quicksketch)
- [ ] Review all closed issues in milestone: (assign to klonos / jenlampton / stpaultim )
  * Issue titles should include a complete, but very brief summary of the problem.
  * Issue titles sould be in complete sentences, ending with a period.
  * Bug issue titles should start with `Fix` or `Fixed`,
  * New fearure issue titles should start with `Add` or `Added`.
  * Each issue should have accurate labels, especially the "type - " labels.
- [ ] Draft Release notes (assign to jenlampton / herbdool / serundeputy / quicksketch)
  - [ ] Include a short, descriptive summary of the release, for example:
    - This is the preview release of Backdrop 1.16.0. Please use this version if you would like to help us test the features in the new version of Backdrop prior to the official release on January/May/September 15th, 20xx.
  - [ ] Include a section containing **Notes for updating**
    - [ ] Note if any changes were made to files outside the `core` directory, for example:
      * No changes have been made to the `.htaccess`, `robots.txt` or default `settings.php` files in this release. Updating customized versions of those files is not necessary.
    - [ ] Note if updates (update.php) needs to be run, for example:
      * Use the text "The database update script does **not** need to be run."
      * or "It will be necessary to run the update script (located at /update.php) for this release."
  - [ ] Include changelog since last version:
      * navigate to [Actions](https://github.com/backdrop/backdrop-issues/actions)
      * Select the most recent time "Release Notes Generator" has been run.
      * Download the `release-notes` artifact attached to the generator.
      * Unzip the file, and copy/pate contents into release notes draft.
      * Re-word issue titles to indicate that the problems have been fixed.


## Pre-release Publicity + documentation tasks

- [ ] Review issues for new features (assign to @jenlampton / @klonos / @cellear)
  - [ ] Add a conclusion suitable for blog post + release notes
  - [ ] Add `Documentation` label if the feature needs to be documented (or needs docs to be updated)
  - [ ] Add `Needs change record` label if the the issue contains an API change.
  - [ ] Add `Needs translation` label if the the issue contains string translations.
- [ ] Draft blog post for release on the 15th (assign to stpaultim / tomgrandy / klonos / jenlampton)
- [ ] Draft roadmap updates for backdropcms.org (assign to stpaultim / klonos / jenlampton)
- [ ] Create new forum topic for feedback on the release @stpaultim


## Release tasks

- [ ] Update bootstrap.inc with version number (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Tag for release, and push tag to GitHub (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Branch for new minor number (e.g. `1.10.x-preview`) and push to GitHub (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Revert version number back on 1.x branch with minor number increased (e.g. `1.11.x-dev`) (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Revert version number back on new minor number branch (e.g. `1.10.x-dev`) (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Create release notes on GitHub (assign to jenlampton / herbdool / serundeputy / quicksketch)


## Post-release Publicity + documentation tasks

- [ ] Tweet that a preview release is out (assign to stpaultim / jimbirch / jenlampton / quicksketch)
- [ ] Publish roadmap updates for backdropcms.org (assign to stpaultim / klonos / jenlampton)


See Also
---------
* [Bug-Fix Release Checklist]()
* [Minor Release Checklist]()
