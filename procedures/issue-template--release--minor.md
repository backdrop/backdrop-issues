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
- [ ] Draft Release notes (assign to jenlampton / herbdool / serundeputy / quicksketch)
  - [ ] Copy Preview release release notes, update as follows
    - [ ] Include a short, descriptive summary of the release, for example:
      - The Backdrop community is proud to release version 1.xx of Backdrop CMS, following our 4-month release cycle.
    - [ ] Include a section containing **Notes for updating**
      - [ ] Note if any changes were made to files outside the `core` directory, for example:
        - No changes have been made to the `.htaccess`, `robots.txt` or default `settings.php` files in this release. Updating customized versions of those files is not necessary.
      - [ ] Note if updates (update.php) needs to be run, for example:
        - Use the text "The database update script does **not** need to be run."
        - or "It will be necessary to run the update script (located at /update.php) for this release."
    - [ ] Include list of major new features
      - This list can be generated from the list on the preview release, but review closed issuses in the milestone
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

## Post-release tasks

### Code tasks

- [ ] Update the [Tugboat repository's](https://github.com/backdrop-ops/tugboat-demos) `config.yml` file to link to the new core release @bwpanda
  - [ ] Make new matching tag for Tugboat repo @bwpanda
  - [ ] Build new [Tugboat preview](https://dashboard.tugboat.qa/5fa46514c62ba02c640d3a67) (with no base) from new tag (then make it a base preview) @bwpanda
  - [ ] Update [backdropcms.org](https://backdropcms.org/admin/config/services/tugboat) to use the new Tugboat tag @bwpanda
  - [ ] Delete [Tugboat base preview](https://dashboard.tugboat.qa/5fa46514c62ba02c640d3a67) from two releases ago (i.e. keep last two versions only) @bwpanda
- [ ] Create a PR to update the [Platform.sh Backdrop repository](https://github.com/platformsh/template-builder/blob/master/project/backdrop.py) @jenlampton
- [ ] Push the minor release to the [Backdrop Composer repository](https://github.com/backdrop-ops/backdrop-composer) @serundeputy
- [ ] Update the [Backdrop Docker repository](https://github.com/backdrop-ops/backdrop-docker) ???
    - [ ] Create a PR to update the [Docker repository](https://github.com/docker-library/official-images/blob/master/library/backdrop) ???
- [ ] update api.backdropcms.org to latest version @jenlampton

### Publicity tasks

- [ ] Tweet that a new release is out (assign to stpaultim / jimbirch / jenlampton / quicksketch)
- [ ] Publish blog post (assign to stpaultim / tomgrandy / klonos / jenlampton)
- [ ] email katie@phpweekly.com for a note in the PHP Weekly Newsletter (assign to stpaultim / tomgrandy / klonos / jenlampton)
- [ ] Update the Wikipedia articles (assign to stpaultim / klonos / jenlampton)
  - [ ] https://en.wikipedia.org/wiki/Backdrop_CMS
  - [ ] https://en.wikipedia.org/wiki/List_of_content_management_systems

## 2 weeks Post-release tasks

- [ ] Push the minor release to the [Pantheon repository](https://github.com/backdrop-ops/backdrop-pantheon) @quicksketch
- [ ] Send a newsletter to subscribers (assign to facetinteractive / stpaultim / tomgrandy / jenlampton)
- [ ] update backdropcms.org to latest version @jenlampton
- [ ] update forum.backdropcms.org to latest version @jenlampton

See Also
---------
* [Bug-Fix Release Checklist]()
* [Preview Release Checklist]()
