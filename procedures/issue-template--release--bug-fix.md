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
    - Maintenance release for Backdrop CMS. This update contains bug fixes and usability improvements only.
  - [ ] Include a section containing **Notes for updating**
    - [ ] Note if any changes were made to files outside the `core` directory, for example:
      - No changes have been made to the `.htaccess`, `robots.txt` or default `settings.php` files in this release. Updating customized versions of those files is not necessary.
    - [ ] Note if updates (update.php) needs to be run, for example:
      - Use the text "The database update script does **not** need to be run."
      - or "It will be necessary to run the update script (located at /update.php) for this release."
  - [ ] Include changelog since last version
    - This changelog can be generated with `drush rn [oldtag] [newtag]`, but you need to be on the minor version branch, for example, 1.15.x

If this is a security release:
- [ ] Draft Security Advisories (assign to stpaultim / klonos / jenlampton / serundeputy / herbdool / quicksketch)

## Release tasks

- [ ] Update bootstrap.inc with version number (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Tag for release, and push tag to GitHub (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Revert version number back (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Create release notes on GitHub, and publish release (assign to jenlampton / herbdool / serundeputy / quicksketch)
- [ ] Update the front page download link on b.org (assign to stpaultim / klonos / jenlampton / serundeputy / herbdool / quicksketch)
- [ ] Tweet that a new release is out (assign to stpaultim / jimbirch / jenlampton / quicksketch)
  - Use text ""

If this is a security release:
- [ ] Publish Security Advisories on b.org (assign to stpaultim / klonos / jenlampton / herbdool / serundeputy / quicksketch)
- [ ] Mark the release node on b.org as a security release (assign to stpaultim / klonos / jenlampton / herbdool / serundeputy / quicksketch)
- [ ] We should [Request a CVE](https://github.com/backdrop/backdrop-issues/blob/master/procedures/security--request-cve.md) - (assign to jenlampton / quicksketch)

## Post-release tasks

If this release does NOT accompany a minor release:
- [ ] Push the bug-fix release to the [Pantheon Backdrop repository](https://github.com/backdrop-ops/backdrop-pantheon) (assign to herbdool / serundeputy / quicksketch)
- [ ] Create a PR to update the [Platform.sh Backdrop repository](https://github.com/platformsh/template-builder/blob/master/project/backdrop.py) (assign to serundeputy / jenlampton)
- [ ] Push the bug-fix release to the [Backdrop Composer repository](https://github.com/backdrop-ops/backdrop-composer) (assign to quicksketch / serundeputy / herbdool / bwpanda)
- [ ] Update the [Tugboat repository's](https://github.com/backdrop-ops/tugboat-demos) `config.yml` file to link to the new core release @bwpanda
  - [ ] Make new matching tag for Tugboat repo @bwpanda
  - [ ] Build new [Tugboat preview](https://dashboard.tugboat.qa/5fa46514c62ba02c640d3a67) (with no base) from new tag (then make it a base preview) @bwpanda
  - [ ] Unset all base previews except the new one, and delete all previews from two releases ago (i.e. keep last two versions only) @bwpanda
  - [ ] Update [backdropcms.org](https://backdropcms.org/admin/config/services/tugboat) to use the new Tugboat tag @bwpanda
- [ ] Update the [Backdrop Docker repository](https://github.com/backdrop-ops/backdrop-docker) ???
    - [ ] Create a PR to update the [Docker repository](https://github.com/docker-library/official-images/blob/master/library/backdrop) ???
- [ ] Update the Wikipedia articles (assign to stpaultim / klonos / jenlampton)
  - [ ] https://en.wikipedia.org/wiki/Backdrop_CMS
  - [ ] https://en.wikipedia.org/wiki/List_of_content_management_systems

If this is a security release:
- [ ] Update the Security Advisory with CVE (assign to jenlampton / quicksketch)

## Backdrop Website updates

If this release does NOT accompany a minor release:
- [ ] backdropcms.org
- [ ] api.backdropcms.org
- [ ] forum.backdropcms.org


## See Also

If this release DOES accompany a minor release:
- [Minor Release Checklist]()
If this IS a security release:
- [Checklist for previous minor version]()
