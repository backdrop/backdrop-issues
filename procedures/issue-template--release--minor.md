DRAFT Steps to create a MINOR release
=====================================
(assignments below are in order of preference from left to right)

---
Issue Title:   Backdrop 1.x.x Release checklist
---

Scheduled for January/September/May 15, 20xx 10am - 4pm PT

## Pre-release tasks

- [ ] Merge minor release commits (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Move all unfinished issues to the next bug-fix release milestone (assign to klonos / jenlampton / herbdool / serundeputy / quicksketch)
- [ ] Review all closed issues in milestone: (assign to klonos / jenlampton / stpaultim )
      - Issue titles should include a complete, but very brief summary of the problem.
      - Issue titles sould be in complete sentences, ending with a period.
      - Bug issue titles should start with `Fix` or `Fixed`,
      - New fearure issue titles should start with `Add` or `Added`.
      - Each issue should have accurate labels, especially the "type - " labels.
- [ ] Close the milestone (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Draft Release notes (assign to jenlampton / herbdool / serundeputy / quicksketch)
  - [ ] Copy Preview release release notes, update as follows
    - [ ] Include a short, descriptive summary of the release, for example:
      - The Backdrop community is proud to release version 1.xx of Backdrop CMS, following our 4-month release cycle.
    - [ ] Include a section containing **Notes for updating**
      - [ ] Note if any changes were made to files outside the `core` directory, for example:
        * No changes have been made to the `.htaccess`, `robots.txt` or default `settings.php` files in this release. Updating customized versions of those files is not necessary.
      - [ ] Note if updates (update.php) needs to be run, for example:
        * Use the text "The database update script does **not** need to be run."
        * or "It will be necessary to run the update script (located at /update.php) for this release."
    - [ ] Include changelog since last version:
        * Navigate to [Actions](https://github.com/backdrop/backdrop-issues/actions)
        * Select the most recent time "Release Notes Generator" has been run.
        * Download the `release-notes` artifact attached to the generator.
        * Unzip the file, and copy/pate contents into release notes draft.
        * Re-word issue titles to indicate that the problems have been fixed.
      - This list can also be copied from the list on the preview release, but review closed issuses in the milestone
    - [ ] Verify the list above matches all changes since the most recent bug-fix release

## Release tasks

- [ ] Update bootstrap.inc with version number (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Tag for release, and push tag to GitHub (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Branch for new minor number (e.g. `1.10.x`) and push to GitHub (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Revert version number back on 1.x branch with minor number increased (e.g. `1.11.x-dev`) (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Revert version number back on new minor number branch (e.g. `1.10.x-dev`) (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Create release notes on GitHub, and publish release (assign to jenlampton / herbdool / serundeputy / quicksketch)
- [ ] Unpublish preview release on backdropcms.org (assign to stpaultim / klonos / jenlampton / serundeputy / herbdool / quicksketch)
- [ ] Update the front page download link on b.org (assign to stpaultim / klonos / jenlampton)
- [ ] Update the roadmap page on b.org (assign to stpaultim / klonos / jenlampton)
- [ ] Create a new language template file for the translation server (assign to olaf - see https://github.com/backdrop-ops/localize.backdropcms.org/issues/27 until this is automated)

## Immediate Post-release tasks

### Code tasks

- [ ] Update [Tugboat](https://github.com/backdrop/backdrop-issues/blob/main/procedures/update--tugboat.md) @bwpanda
- [ ] Update [Platform.sh](https://github.com/backdrop/backdrop-issues/blob/main/procedures/update--platformsh-template.md) (assign to serundeputy / jenlampton)
- [ ] Update Composer (assign to quicksketch / serundeputy / herbdool)
- [ ] Update [Docker](https://github.com/backdrop/backdrop-issues/blob/main/procedures/update--docker-image.md) (assign to ??? -- volunteer neeed)

- [ ] Update the Wikipedia articles (assign to stpaultim / klonos / jenlampton)
  - [ ] https://en.wikipedia.org/wiki/Backdrop_CMS
  - [ ] https://en.wikipedia.org/wiki/List_of_content_management_systems
- [ ] update docs.backdropcms.org to latest version @jenlampton

### Publicity tasks

- [ ] Tweet that a new release is out (assign to stpaultim / jimbirch / jenlampton / quicksketch)
  - Use text like "We're thrilled to announce Backdrop version 1.18.0. This is the 19th new feature release of #BackdropCMS. https://backdropcms.org"
- [ ] Publish blog post (assign to stpaultim / tomgrandy / klonos / jenlampton)
- [ ] email katie@phpweekly.com for a note in the PHP Weekly Newsletter (assign to stpaultim / tomgrandy / klonos / jenlampton)
- [ ] Update the Wikipedia articles (assign to stpaultim / klonos / jenlampton)
  - [ ] https://en.wikipedia.org/wiki/Backdrop_CMS
  - [ ] https://en.wikipedia.org/wiki/List_of_content_management_systems

### Backdrop Website updates

- [ ] docs.backdropcms.org (assign to @jenlampton / @bwpanda / ??)
- [ ] events.backdropcms.org (assign to @jenlampton / @bwpanda / ??)
- [ ] forum.backdropcms.org (assign to @jenlampton / @bwpanda / ??)

## 2-week Post-release tasks

These should be done after the first bug-fix release or 14 days -- whichever
comes sooner.

### Code tasks

- [ ] Update [Pantheon](https://github.com/backdrop/backdrop-issues/blob/main/procedures/update--pantheon-upstream.md) (assign to herbdool / serundeputy / quicksketch)

### Publicity tasks

- [ ] Send a newsletter to subscribers (assign to @bwpanda / stpaultim / jenlampton)

### Backdrop Website updates

- [ ] backdropcms.org (assign to @jenlampton / @bwpanda / ??)


See Also
---------
* [Bug-Fix Release Checklist]()
* [Preview Release Checklist]()
