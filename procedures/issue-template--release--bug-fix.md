Steps to create a BUG-FIX release
==================================
(assignments below are in order of preference from left to right)

---
Issue Title:   Backdrop 1.x.x Release checklist
---

Release scheduled for MM DD, 20xx 10am - 4pm PT


## Pre-release tasks

- [ ] Merge commits (assign to quicksketch / serundeputy / herbdool)
- [ ] Create the next bugfix milestone (assign to klonos / jenlampton / herbdool / serundeputy / quicksketch)
- [ ] Move all unfinished issues to the next bugfix release milestone (assign to klonos / jenlampton / herbdool / serundeputy / quicksketch)
- [ ] Draft Release notes (assign to jenlampton / herbdool / serundeputy / quicksketch)
  1. [ ] Include a short, descriptive summary of the release, for example:
    - Maintenance release for Backdrop CMS. This update contains bug fixes and usability improvements only.
  1. [ ] Include a section containing **Notes for updating**
    - [ ] Note if any changes were made to files outside the `core` directory, for example:
      - No changes have been made to the `.htaccess`, `robots.txt` or default `settings.php` files in this release. Updating customized versions of those files is not necessary.
    - [ ] Note if updates (update.php) needs to be run, for example:
      - Use the text "The database update script does **not** need to be run."
      - or "It will be necessary to run the update script (located at /update.php) for this release."
  1. [ ] Include changelog since last version
        This changelong can be generated with `drush rn [oldtag] [newtag]`, but you need to be on the minor version branch, for example, 1.15.1

If this is a security release:
- [ ] Draft Security Advisories (assign to stpaultim / klonos / jenlampton / serundeputy / herbdool / quicksketch)

## Release tasks

- [ ] Update bootstrap.inc with version number (assign to quicksketch / serundeputy / herbdool)
- [ ] Tag for release, and push tag to GitHub (assign to quicksketch / serundeputy / herbdool)
- [ ] Revert version number back (assign to quicksketch / serundeputy / herbdool)
- [ ] Create release notes on GitHub, and publish release (assign to jenlampton / herbdool / serundeputy / quicksketch)
- [ ] Update the front page download link on b.org (assign to stpaultim / klonos / jenlampton / serundeputy / herbdool / quicksketch)
- [ ] Tweet that a new release is out (assign to stpaultim / jimbirch / jenlampton / quicksketch)
  - Use text ""

If this is a security release:
- [ ] Publish Security Advisories on b.org (assign to stpaultim / klonos / jenlampton / herbdool / serundeputy / quicksketch)
- [ ] Mark the release node on b.org as a security release (assign to stpaultim / klonos / jenlampton / herbdool / serundeputy / quicksketch)
- [ ] We should [Request a CVE](https://github.com/backdrop/backdrop-issues/blob/master/procedures/security--request-cve.md) - (assign to jenlampton / quicksketch)

## Post-release tasks


- [ ] Push the bug-fix release to the [Pantheon Backdrop repository](https://github.com/backdrop-ops/backdrop-pantheon) (assign to herbdool / serundeputy / quicksketch)
- [ ] Push the bug-fix release to the [TugBoat Backdrop repository](https://github.com/backdrop-ops/backdrop-tugboat) (assign to quicksketch / jenlampton / serundeputy / herbdool)
- [ ] Create a PR to update the [Platform.sh Backdrop repository](https://github.com/platformsh/template-builder/blob/master/project/backdrop.py) (assign to serundeputy / jenlampton)
- [ ] Push the bug-fix release to the [Docker Backdrop repository](https://github.com/docker-library/official-images/blob/master/library/backdrop) (assign to drupol / jenlampton / serundeputy)
- [ ] Push the bug-fix release to the [Backdrop Composer repository](https://github.com/backdrop-ops/backdrop-composer) (assign to quicksketch / serundeputy / herbdool)
- [ ] Update the Wikipedia articles (assign to stpaultim / klonos / jenlampton)
  - [ ] https://en.wikipedia.org/wiki/Backdrop_CMS
  - [ ] https://en.wikipedia.org/wiki/List_of_content_management_systems

If this is a security release:
- [ ] Update the Security Advisory with CVE (assign to jenlampton / quicksketch)

## Backdrop Website updates

- [ ] backdropcms.org
- [ ] api.backdropcms.org
- [ ] forum.backdropcms.org
