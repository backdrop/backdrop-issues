Steps to create a BUG-FIX release
==================================
(assignments below are in order of preference from left to right)

---
Issue Title:   Backdrop 1.x.x Release checklist
---

Release scheduled for MM DD, 20xx 10am - 4pm PT

## Pre-release tasks

- [ ] Merge commits (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Create the next bugfix milestone (assign to klonos / jenlampton / herbdool / serundeputy / quicksketch)
- [ ] Move all unfinished issues to the next bugfix release milestone (assign to klonos / jenlampton / herbdool / serundeputy / quicksketch)
- [ ] Review all closed issues in milestone: (assign to klonos / jenlampton / stpaultim )
  * Issue titles should include a complete, but very brief summary of the problem.
  * Issue titles sould be in complete sentences, ending with a period.
  * Bug issue titles should start with `Fix` or `Fixed`,
  * New fearure issue titles should start with `Add` or `Added`.
  * Each issue should have accurate labels, especially the "type - " labels.
- [ ] Close the milestone (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Draft Release notes (assign to jenlampton / herbdool / serundeputy / quicksketch)
  - [ ] Include a short, descriptive summary of the release, for example:
      * "Maintenance release for Backdrop CMS. This update contains bug fixes and usability improvements only."
  - [ ] Include a section heading `**Notes for updating**`
    - [ ] Note if any changes were made to files outside the `core` directory, for example:
      * No changes have been made to the `.htaccess`, `robots.txt` or default `settings.php` files in this release. Updating customized versions of those files is not necessary.
      * See [this example](https://github.com/backdrop/backdrop/releases/tag/1.18.0) for updates to `.htaccess`
      * See [this example](https://github.com/backdrop/backdrop/releases/tag/1.16.0) or [this example](https://github.com/backdrop/backdrop/releases/tag/1.14.0) for updates to `settings.php`
    - [ ] Note if updates (update.php) needs to be run, for example:
      * Use the text `The database update script does **not** need to be run.`
      * or `**It will be necessary to run the update script** (located at /update.php) for this release.`
  - [ ] Include a section heading `**Changes since version 1.xx.x** are listed below.`
    * Navigate to [Actions](https://github.com/backdrop/backdrop-issues/actions)
    * Select the most recent time "Release Notes Generator" has been run.
    * Download the `release-notes` artifact attached to the generator.
    * Unzip the file, and copy/pate contents into release notes draft.
    * Remove any square bracets in the titles, and move those issues to their own section.

## Release tasks

- [ ] Update bootstrap.inc with version number (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Tag for release, and push tag to GitHub (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Revert version number back (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Create release notes on GitHub, and publish release (assign to jenlampton / herbdool / serundeputy / quicksketch)
- [ ] Update the front page download link on b.org (assign to stpaultim / klonos / jenlampton / serundeputy / herbdool / quicksketch)
- [ ] Tweet that a new release is out (assign to stpaultim / jimbirch / jenlampton / quicksketch)
  - Use text like "There is a bug-fix release out for #BackdropCMS today, version 1.17.1: https://backdropcms.org." or

## Immediate Post-release tasks

If this release does NOT accompany a minor release:
- [ ] Update [Tugboat](https://github.com/backdrop/backdrop-issues/blob/main/procedures/update--tugboat.md) @bwpanda
- [ ] Update [Pantheon](https://github.com/backdrop/backdrop-issues/blob/main/procedures/update--pantheon-upstream.md) (assign to herbdool / serundeputy / quicksketch)
- [ ] Update [Platform.sh](https://github.com/backdrop/backdrop-issues/blob/main/procedures/update--platformsh-template.md) (assign to serundeputy / jenlampton)
- [ ] Update Composer (assign to quicksketch / serundeputy / herbdool)
- [ ] Update [Docker](https://github.com/backdrop/backdrop-issues/blob/main/procedures/update--docker-image.md) (assign to ??? -- volunteer neeed)
- [ ] Update the Wikipedia articles (assign to stpaultim / klonos)
  - [ ] https://en.wikipedia.org/wiki/Backdrop_CMS
  - [ ] https://en.wikipedia.org/wiki/List_of_content_management_systems

## Backdrop's Website updates
<!-- If this release does NOT accompany a minor release: -->

- [ ] backdropcms.org (assign to @jenlampton / @bwpanda / @bugfolder)
- [ ] beta.backdropcms.org (assign to @jenlampton / @bwpanda / @bugfolder)
- [ ] docs.backdropcms.org (assign to @jenlampton / @bwpanda / @bugfolder)
- [ ] events.backdropcms.org (assign to @jenlampton / @bwpanda / @bugfolder)
- [ ] forum.backdropcms.org (assign to @jenlampton / @bwpanda / @bugfolder)
- [ ] localize.backdropcms.org (assign to @jenlampton / @bwpanda / @bugfolder)


## See Also

- [Checklist for 1.xx.x release]()
<!-- If this release DOES accompany a minor release: -->
- [Minor Release Checklist]()
<!-- If this is a security release: -->
- [Checklist for previous minor version]()

