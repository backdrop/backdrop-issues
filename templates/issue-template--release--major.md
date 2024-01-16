Steps to create a MAJOR release
=================================
(assignments below are in order of preference from left to right)

## Pre-release tasks

- [ ] Merge commits (assign to quicksketch / herbdool / laryn / hosef)
- [ ] Create a new minor release ((assign to quicksketch / serundeputy / herbdool)
- [ ] Create the next minor milestone (assign to quicksketch / jenlampton)
- [ ] Move all unfinished issues to the next major release milestone (assign to quicksketch / jenlampton)
- [ ] Review all closed issues in milestone: (assign to klonos / jenlampton / stpaultim )
  * Issue titles should include a complete, but very brief summary of the problem.
  * Issue titles should be in complete sentences, ending with a period.
  * Bug issue titles should start with `Fix` or `Fixed`,
  * New feature issue titles should start with `Add` or `Added`.
  * Each issue should have accurate labels, especially the "type - " labels.
- [ ] Close the milestone (assign to quicksketch / herbdool)
- [ ] Draft Release notes (assign to jenlampton / herbdool / quicksketch)
  - [ ] Include a short, descriptive summary of the release, for example:
    * This is the preview release of Backdrop 1.16.0. Please use this version if you would like to help us test the features in the new version of Backdrop prior to the official release on January/May/September 15th, 20xx.
  - [ ] Include a section heading `**Notes for updating**`
    - [ ] Note if any changes were made to files outside the `core` directory, for example:
      * ``- No changes have been made to the `.htaccess`, `robots.txt` or default `settings.php` files in this release. Updating customized versions of those files is not necessary.``
      * See [this example](https://github.com/backdrop/backdrop/releases/tag/1.18.0) for updates to `.htaccess`
      * See [this example](https://github.com/backdrop/backdrop/releases/tag/1.16.0) or [this example](https://github.com/backdrop/backdrop/releases/tag/1.14.0) for updates to `settings.php`
    - [ ] Note if updates (update.php) needs to be run, for example:
      * Use the text `The database update script does **not** need to be run.`
      * or `**It will be necessary to run the update script** (located at /update.php) for this release.`
  - [ ] Include a section heading `**Changes since version 1.xx.x** are listed below.`
      * navigate to [Actions](https://github.com/backdrop/backdrop-issues/actions)
      * Select the most recent time "Release Notes Generator" has been run.
      * Download the `release-notes` artifact attached to the generator.
      * Unzip the file, and copy/pate contents into release notes draft.
      * Re-word issue titles to indicate that the problems have been fixed.
- [ ] Draft blog post (assign to tomgrandy / klonos / jenlampton / quicksketch)
- [ ] Draft a newsletter via MailChimp (assign to facetinteractive / tomgrandy / jenlampton)

## Release tasks

- [ ] Update bootstrap.inc with version number (assign to quicksketch / herbdool / laryn / hosef)
- [ ] Tag for release, and push tag to GitHub (assign to quicksketch / herbdool / laryn / hosef)
- [ ] Revert version number back (assign to quicksketch / herbdool / laryn / hosef)
- [ ] Create release notes on GitHub (assign to quicksketch / jenlampton)
- [ ] Unpublish preview release on backdropcms.org (assign to quicksketch / jenlampton)
- [ ] Update the front page download link on b.org (assign to serundeputy / quicksketch / jenlampton / klonos)
- [ ] Tweet that a new release is out (assign to quicksketch / jenlampton / jimbirch)

## Post-release tasks (after first bug-fix release or 14 days -- whichever comes sooner)

- [ ] Update [Tugboat](https://github.com/backdrop/backdrop-issues/wiki/Update:-Tugboat) @klonos
- [ ] Update [Pantheon](https://github.com/backdrop/backdrop-issues/wiki/Update:-Pantheon-Upstream) @herbdool
- [ ] Update [Platform.sh](https://github.com/backdrop/backdrop-issues/wiki/Update:-Platform.sh-Template) (assign to herbdool / jenlampton)
- [ ] Update [Composer](https://github.com/backdrop-ops/backdrop-composer) @herbdool (or quicksketch)
- [ ] Update [Docker](https://github.com/backdrop/backdrop-issues/wiki/Update:-Docker-Image) @wylbur
- [ ] Update the Wikipedia articles (assign to stpaultim / klonos)
  - [ ] https://en.wikipedia.org/wiki/Backdrop_CMS
  - [ ] https://en.wikipedia.org/wiki/List_of_content_management_systems
- [ ] Publish blog post (assign to tomgrandy / klonos / jenlampton / quicksketch)
- [ ] Send a newsletter via MailChimp (assign to facetinteractive / tomgrandy / jenlampton)
- [ ] email katie@phpweekly.com for a note in the PHP Weekly Newsletter (assign to tomgrandy / klonos / jenlampton)
- [ ] Update the Wikipedia articles (assign to klonos / jenlampton)
  - [ ] https://en.wikipedia.org/w/index.php?title=Template:BackdropCMS_version&action=edit - 
    * Auto applied to:
      * https://en.wikipedia.org/wiki/Backdrop_CMS
      * https://en.wikipedia.org/wiki/List_of_content_management_systems

## See Also

<!-- If this release DOES accompany a minor release: -->
- [Minor Release Checklist]()
<!-- If this is a security release: -->
- [Checklist for previous minor version]()