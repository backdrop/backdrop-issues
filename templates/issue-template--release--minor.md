DRAFT Steps to create a MINOR release
=====================================
(assignments below are in order of preference from left to right)

---
Issue Title:   Backdrop 1.x.x Release checklist
---

Scheduled for January/September/May 15, 20xx 10am - 4pm PT

## Pre-release tasks

- [ ] If this is the Jan 15 release, ensure that the end year in the "All Backdrop code is Copyright..." section towards the bottom of the README.md file has been updated to reflect the new/current year.
- [ ] Merge commits (assign to quicksketch / herbdool / laryn / hosef)
- [ ] Move all unfinished issues to the next bug-fix release milestone (assign to klonos / jenlampton / herbdool / quicksketch)
- [ ] Review all closed issues in milestone: (assign to klonos / jenlampton / stpaultim )
  * Issue titles should include a complete, but very brief summary of the problem.
  * Issue titles should be in complete sentences, ending with a period.
  * Bug issue titles should start with `Fix` or `Fixed`,
  * New feature issue titles should start with `Add` or `Added`.
  * Each issue should have accurate labels, especially the "type - " labels.
- [ ] Close the milestone (assign to quicksketch / herbdool / jenlampton)
- [ ] Draft Release notes (assign to jenlampton / herbdool / quicksketch)
  - [ ] Copy Preview release release notes, update as follows
    - [ ] Include a short, descriptive summary of the release, for example:
      * The Backdrop community is proud to release version 1.xx of Backdrop CMS, following our 4-month release cycle.
    - [ ] Include a section heading `**Notes for updating**`
      - [ ] Note if any changes were made to files outside the `core` directory, for example:
        * ``- No changes have been made to the `.htaccess`, `robots.txt` or default `settings.php` files in this release. Updating customized versions of those files is not necessary.``
        * See [this example](https://github.com/backdrop/backdrop/releases/tag/1.18.0) for updates to `.htaccess`
        * See [this example](https://github.com/backdrop/backdrop/releases/tag/1.16.0) or [this example](https://github.com/backdrop/backdrop/releases/tag/1.14.0) for updates to `settings.php`
      - [ ] Note if updates (update.php) needs to be run, for example:
        * Use the text `The database update script does **not** need to be run.`
        * or `**It will be necessary to run the update script** (located at /core/update.php) for this release.`
    - [ ] Include a section heading `**Changes since version 1.xx.x** are listed below.`
      * Navigate to [Actions](https://github.com/backdrop/backdrop-issues/actions)
      * Select the most recent time "Release Notes Generator" has been run.
      * Download the `release-notes` artifact attached to the generator.
      * Unzip the file, and copy/pate contents into release notes draft.
      * Re-word issue titles to indicate that the problems have been fixed.
      * Note: This list can also be copied from the list on the preview release, but review closed issuses in the milestone
    - [ ] Verify the list above matches all changes since the most recent bug-fix release

## Release tasks

- [ ] Update bootstrap.inc with version number (assign to quicksketch / herbdool / laryn / hosef)
- [ ] Tag for release, and push tag to GitHub (assign to quicksketch / herbdool / laryn / hosef)
- [ ] Branch for new minor number (e.g. `1.10.x`) and push to GitHub (assign to quicksketch / herbdool / laryn / hosef)
- [ ] Revert version number back on 1.x branch with minor number increased (e.g. `1.11.x-dev`) (assign to quicksketch / herbdool / laryn / hosef)
- [ ] Revert version number back on new minor number branch (e.g. `1.10.x-dev`) (assign to quicksketch / herbdool / laryn / hosef)
- [ ] Create release notes on GitHub, and publish release (assign to jenlampton / herbdool / quicksketch)
- [ ] Unpublish preview release on backdropcms.org (assign to stpaultim / klonos / jenlampton / herbdool / quicksketch)
- [ ] Update the front page download link on b.org (assign to stpaultim / klonos / jenlampton)
- [ ] Create a new language template file for the translation server @olaf
<!-- automate this https://github.com/backdrop-ops/localize.backdropcms.org/issues/27 -->

## Immediate Post-release tasks

### Publicity tasks

- [ ] Tweet that a new release is out @stpaultim
  * Use text like "We're thrilled to announce Backdrop version 1.18.0. This is the 19th new feature release of #BackdropCMS. https://backdropcms.org"
- [ ] Publish blog post (assign to stpaultim / tomgrandy / klonos / jenlampton)
- [ ] email katie@phpweekly.com for a note in the PHP Weekly Newsletter (assign to stpaultim / klonos / jenlampton)
- [ ] Update the roadmap page on b.org (assign to stpaultim / klonos / jenlampton)
- [ ] Update list of modules included in backdrop core (assign to bugfolder / klonos / jenlampton)
- [ ] Update list of modules included in backdrop_upgrade_status module @jenlampton
- [ ] Update the Wikipedia articles (assign to stpaultim / klonos / jenlampton)
  - [ ] https://en.wikipedia.org/w/index.php?title=Template:BackdropCMS_version&action=edit - 
    * Auto applied to:
      * https://en.wikipedia.org/wiki/Backdrop_CMS
      * https://en.wikipedia.org/wiki/List_of_content_management_systems

### Code tasks

- [ ] Update [Tugboat](https://github.com/backdrop/backdrop-issues/wiki/Update:-Tugboat) @klonos
- [ ] Update [Composer](https://github.com/backdrop/backdrop-issues/wiki/Update:-Composer) @herbdool
- [ ] Update [Docker](https://github.com/backdrop/backdrop-issues/wiki/Update:-Docker-Image) @wylbur
- [ ] Update [Pantheon](https://github.com/backdrop/backdrop-issues/wiki/Update:-Pantheon-Upstream) @herbdool
- [ ] Update [Platform.sh](https://github.com/backdrop/backdrop-issues/wiki/Update:-Platform.sh-Template) @herbdool
- [ ] Update [Amezmo](https://github.com/backdrop/backdrop-issues/wiki/Update:-Amezmo) @jenlampton
- [ ] Update [DrupalForge](https://github.com/backdrop/backdrop-issues/wiki/Update:-Drupal-Forge-(devpanel)-Template) @izmeez

### Backdrop Website updates

- [ ] beta.backdropcms.org @bugfolder (or jenlampton)
- [ ] docs.backdropcms.org @jenlampton (or bugfolder)
- [ ] events.backdropcms.org @jenlampton (or bugfolder)
- [ ] localize.backdropcms.org @jenlampton (or bugfolder)

## 2-week Post-release tasks
<!-- These should be done after the first bug-fix release or 14 days -- whichever comes sooner. -->

- [ ] backdropcms.org @jenlampton
- [ ] forum.backdropcms.org @jenlampton


### Publicity tasks

- [ ] Add a notification to the dashboard (assign to stpaultim / klonos / jenlampton)
- [ ] Send a newsletter to subscribers (assign to stpaultim / jenlampton)


See Also
---------
* [Bug-Fix Release Checklist]()
* [Preview Release Checklist]()
