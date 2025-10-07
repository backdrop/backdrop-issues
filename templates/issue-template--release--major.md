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
  * Bug issue titles should start with `Fix` or `Fixed`,
  * New feature issue titles should start with `Add` or `Added`.
  * Each issue should have accurate labels, especially the "type - " labels.
- [ ] Close the milestone (assign to quicksketch / herbdool)
- [ ] Draft Release notes (assign to jenlampton / herbdool / quicksketch)
  - [ ] Include a short, descriptive summary of the release, for example:
    * This is the preview release of Backdrop 1.16.0. Please use this version if you would like to help us test the features in the new version of Backdrop prior to the official release on January/May/September 15th, 20xx.
  - [ ] Include a section heading `## Notes for updating*`
    - [ ] Note if any changes were made to files outside the `core` directory, for example:
      * ``- No changes have been made to the `.htaccess`, `robots.txt` or default `settings.php` files in this release. Updating customized versions of those files is not necessary.``
      * See [this example](https://github.com/backdrop/backdrop/releases/tag/1.18.0) for updates to `.htaccess`
      * See [this example](https://github.com/backdrop/backdrop/releases/tag/1.16.0) or [this example](https://github.com/backdrop/backdrop/releases/tag/1.14.0) for updates to `settings.php`
    - [ ] Note if updates (update.php) needs to be run, for example:
      * Use the text `The database update script does **not** need to be run.`
      * or `**It will be necessary to run the update script** (located at /core/update.php) for this release.`
      * Note: you can use this command to see if any install files were changed:
      `ls -1 core/modules/*/*.install | while read filename; do echo "$(git log -1 --pretty="format:%ad %f" --date=format:"%F %R" -- $filename)" $filename; done|sort`
  - [ ] Include a section heading `## Changes since version 1.xx.x`
      * navigate to [Actions](https://github.com/backdrop/backdrop-issues/actions)
      * Select the most recent time "Release Notes Generator" has been run.
      * Download the `release-notes` artifact attached to the generator.
      * Unzip the file, and copy/pate contents into release notes draft.
        - Move the headings to H3, add another `#` before the `##` to get `###`.
      * Re-word issue titles to indicate that the problems have been fixed.
- [ ] Draft blog post (assign to tomgrandy / klonos / jenlampton / quicksketch)
- [ ] Draft a newsletter via MailChimp (assign to facetinteractive / tomgrandy / jenlampton)

## Release tasks

- [ ] Update bootstrap.inc with version number (assign to quicksketch / herbdool / laryn / hosef)
- [ ] Tag for release, and push tag to GitHub (assign to quicksketch / herbdool / laryn / hosef)
- [ ] Revert version number back (assign to quicksketch / herbdool / laryn / hosef)
- [ ] Create release notes on GitHub (assign to quicksketch / jenlampton)
- [ ] Unpublish preview release on backdropcms.org (assign to quicksketch / jenlampton)
- [ ] Social Media: Post/Tweet/Toot/Skeet that a new version is out (assignments below)
  * Use text like "We're thrilled to announce Backdrop version 1.x. This is the 2nd major release of #BackdropCMS. https://backdropcms.org"
  - [ ] Post to Bluesky @stpaultim
  - [ ] Post to Mastodon @stpaultim
  - [ ] Post to Twitter @stpaultim
  - [ ] Post to Facebook @stpaultim or @cellear
  - [ ] Post to LinkedIn @yorkshirepudding
- [ ] Publish blog post (assign to stpaultim / klonos / jenlampton)

## Post-release tasks (after first bug-fix release or 14 days -- whichever comes sooner)

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
- [ ] Publish blog post (assign to tomgrandy / klonos / jenlampton / quicksketch)
- [ ] Send a newsletter via MailChimp (assign to stpaultim / bugfolder / jenlampton)
- [ ] email katie@phpweekly.com for a note in the PHP Weekly Newsletter (assign to tomgrandy / klonos / jenlampton)


## See Also

<!-- If this release DOES accompany a minor release: -->
- [Minor Release Checklist]()
<!-- If this is a security release: -->
- [Checklist for previous minor version]()