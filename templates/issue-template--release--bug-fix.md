Steps to create a BUG-FIX release
==================================
(assignments below are in order of preference from left to right)

---
Issue Title:   Backdrop 1.x.x Release checklist
---

Release scheduled for [Month] DD, 20xx 10am - 4pm PT

## Pre-release tasks

- [ ] Merge commits (assign to quicksketch / herbdool / laryn / hosef)
- [ ] Create the next bugfix milestone (assign to klonos / jenlampton / herbdool / quicksketch)
- [ ] Move all unfinished issues to the next bugfix release milestone (assign to klonos / jenlampton / herbdool / quicksketch)
- [ ] Review all closed issues in milestone: (assign to klonos / jenlampton / stpaultim )
  * Issue titles should include a complete, but very brief summary of the problem.
  * Issue titles should be in complete sentences, ending with a period.
  * Bug issue titles should start with `Fix` or `Fixed`,
  * New feature issue titles should start with `Add` or `Added`.
  * Each issue should have accurate labels, especially the "type - " labels.
- [ ] Close the milestone (assign to quicksketch / herbdool / jenlampton)
- [ ] Draft Release notes (assign to jenlampton / herbdool / quicksketch)
  - [ ] Include a short, descriptive summary of the release, for example:
    * "Maintenance release for Backdrop CMS. This update contains bug fixes and usability improvements only."
  - [ ] Include a section heading `**Notes for updating**`
    - [ ] Note if any changes were made to files outside the `core` directory, for example:
      * ``- No changes have been made to the `.htaccess`, `robots.txt` or default `settings.php` files in this release. Updating customized versions of those files is not necessary.``
      * See [this example](https://github.com/backdrop/backdrop/releases/tag/1.18.0) for updates to `.htaccess`
      * See [this example](https://github.com/backdrop/backdrop/releases/tag/1.16.0) or [this example](https://github.com/backdrop/backdrop/releases/tag/1.14.0) for updates to `settings.php`
    - [ ] Note if updates (update.php) needs to be run, for example:
      * Use the text `The database update script does **not** need to be run.`
      * or `**It will be necessary to run the update script** (located at /core/update.php) for this release.`
      * Note: you can use this command to see if any install files were changed:
      `ls -1 core/modules/*/*.install | while read filename; do echo "$(git log -1 --pretty="format:%ad %f" --date=format:"%F %R" -- $filename)" $filename; done|sort`
  - [ ] Include a section heading `**Changes since version 1.xx.x** are listed below.`
    * Navigate to [Actions](https://github.com/backdrop/backdrop-issues/actions)
    * Select the most recent time "Release Notes Generator" has been run.
    * Download the `release-notes` artifact attached to the generator.
    * Unzip the file, and copy/pate contents into release notes draft.
    * Remove any square brackets in the titles, and move those issues to their own section.

## Release tasks

- [ ] Update bootstrap.inc with version number (assign to quicksketch / herbdool / laryn / hosef)
- [ ] Tag for release, and push tag to GitHub (assign to quicksketch / herbdool / laryn / hosef)
- [ ] Revert version number back (assign to quicksketch / herbdool / laryn / hosef)
- [ ] Create release notes on GitHub, and publish release (assign to jenlampton / herbdool / quicksketch)
- [ ] Update the front page download link on b.org (assign to stpaultim / klonos / jenlampton / herbdool / quicksketch)
- [ ] Tweet that a new release is out (assign to stpaultim / jimbirch / jenlampton / quicksketch)
  - Use text like "There is a bug-fix release out for #BackdropCMS today, version 1.27.2: https://backdropcms.org."

## Immediate Post-release tasks

- [ ] Update [Tugboat](https://github.com/backdrop/backdrop-issues/wiki/Update:-Tugboat) @klonos
- [ ] Update [Composer](https://github.com/backdrop/backdrop-issues/wiki/Update:-Composer) @herbdool
- [ ] Update [Docker](https://github.com/backdrop/backdrop-issues/wiki/Update:-Docker-Image) @wylbur
- [ ] Update [Pantheon](https://github.com/backdrop/backdrop-issues/wiki/Update:-Pantheon-Upstream) @herbdool
- [ ] Update [Platform.sh](https://github.com/backdrop/backdrop-issues/wiki/Update:-Platform.sh-Template) @herbdool
- [ ] Update [Amezmo](https://github.com/backdrop/backdrop-issues/wiki/Update:-Amezmo) @jenlampton
- [ ] Update [DrupalForge](https://github.com/backdrop/backdrop-issues/wiki/Update:-Drupal-Forge-(devpanel)-Template) @izmeez
- [ ] Update the Wikipedia articles @klonos
  - [ ] https://en.wikipedia.org/w/index.php?title=Template:BackdropCMS_version&action=edit - 
    * Auto applied to:
      * https://en.wikipedia.org/wiki/Backdrop_CMS
      * https://en.wikipedia.org/wiki/List_of_content_management_systems

## Backdrop's Website updates
<!-- If this release does NOT accompany a minor release: -->

- [ ] backdropcms.org @jenlampton (or bugfolder)
- [ ] beta.backdropcms.org @bugfolder (or jenlampton)
- [ ] docs.backdropcms.org @jenlampton (or bugfolder)
- [ ] events.backdropcms.org @jenlampton (or bugfolder)
- [ ] forum.backdropcms.org @jenlampton (or bugfolder)
- [ ] localize.backdropcms.org @jenlampton (or bugfolder)

## See Also

<!-- If this release DOES accompany a minor release: -->
- [Checklist for 1.xx.x release]()
<!-- If this is a security release: -->
- [Checklist for previous minor version]()

