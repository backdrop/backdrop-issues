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
- [ ] Draft Release notes (assign to jenlampton / herbdool / serundeputy / quicksketch)
  - [ ] Include a short, descriptive summary of the release, for example:
    - "Maintenance release for Backdrop CMS. This update contains bug fixes and usability improvements only."
    - or, "Security release for Backdrop CMS. This release fixes 1 security vulnerability:"
  - [ ] Include a section containing **Notes for updating**
    - [ ] Note if any changes were made to files outside the `core` directory, for example:
      - No changes have been made to the `.htaccess`, `robots.txt` or default `settings.php` files in this release. Updating customized versions of those files is not necessary.
    - [ ] Note if updates (update.php) needs to be run, for example:
      - Use the text "The database update script does **not** need to be run."
      - or "It will be necessary to run the update script (located at /update.php) for this release."
  - [ ] Include changelog since last version
    - Before the milestone has been closed, clean up issue titles for fixed issues.
    - Once the milestone has been closed, navigate to [Actions](https://github.com/backdrop/backdrop-issues/actions)
    - Select the most recent time "Release Notes Generator" has been run.
    - Download the `release-notes` artifact attached to the generator.
    - Unzip the file, and copy/pate contents into release notes draft.
    - Re-word issue titles to indicate that the problems have been fixed.
<!-- If this is a security release: -->
- [ ] Draft Security Advisories (assign to stpaultim / klonos / jenlampton / serundeputy / herbdool / quicksketch)

## Release tasks

- [ ] Update bootstrap.inc with version number (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Tag for release, and push tag to GitHub (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Revert version number back (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Create release notes on GitHub, and publish release (assign to jenlampton / herbdool / serundeputy / quicksketch)
- [ ] Update the front page download link on b.org (assign to stpaultim / klonos / jenlampton / serundeputy / herbdool / quicksketch)
- [ ] Tweet that a new release is out (assign to stpaultim / jimbirch / jenlampton / quicksketch)
  - Use text like "There is a bug-fix release out for #BackdropCMS today, version 1.17.1: https://backdropcms.org."
<!-- If this is a security release: -->
  - Use text like "There is a security release out for #BackdropCMS today, please update when you can. Backdrop core - Critical - Third-party libraries - BACKDROP-SA-CORE-2021-001"
<!-- If this is a security release: -->
- [ ] Publish Security Advisories on b.org (assign to stpaultim / klonos / jenlampton / herbdool / serundeputy / quicksketch)
- [ ] Mark the release node on b.org as a security release (assign to stpaultim / klonos / jenlampton / herbdool / serundeputy / quicksketch)
- [ ] We should [Request a CVE](https://github.com/backdrop/backdrop-issues/blob/master/procedures/security--request-cve.md) - (assign to jenlampton / quicksketch)

## Immediate Post-release tasks

If this release does NOT accompany a minor release:
- [ ] Update [Tugboat](https://github.com/backdrop/backdrop-issues/blob/master/procedures/update--tugboat.md) @bwpanda
- [ ] Update [Pantheon](https://github.com/backdrop/backdrop-issues/blob/master/procedures/update--pantheon-upstream.md) (assign to herbdool / serundeputy / quicksketch)
- [ ] Update [Platform.sh](https://github.com/backdrop/backdrop-issues/blob/master/procedures/update--platformsh-template.md) (assign to serundeputy / jenlampton)
- [ ] Update Composer (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Update [Docker](https://github.com/backdrop/backdrop-issues/blob/master/procedures/update--docker-image.md) (assign to ??? -- volunteer neeed)
- [ ] Update the Wikipedia articles (assign to stpaultim / klonos / jenlampton)
  - [ ] https://en.wikipedia.org/wiki/Backdrop_CMS
  - [ ] https://en.wikipedia.org/wiki/List_of_content_management_systems
<!-- If this is a security release: -->
- [ ] Update the Security Advisory with CVE (assign to jenlampton / quicksketch)

## Backdrop Website updates

<!-- If this release does NOT accompany a minor release: -->
- [ ] backdropcms.org (assign to @jenlampton / @bwpanda / ??)
- [ ] api.backdropcms.org (assign to @jenlampton / @bwpanda / ??)
- [ ] events.backdropcms.org (assign to @jenlampton / @bwpanda / ??)
- [ ] forum.backdropcms.org (assign to @jenlampton / @bwpanda / ??)
- [ ] localize.backdropcms.org (assign to @jenlampton / @bwpanda / ??)


## See Also

- [Checklist for 1.xx.x release]()
<!-- If this release DOES accompany a minor release: -->
- [Minor Release Checklist]()
<!-- If this is a security release: -->
- [Checklist for previous minor version]()

