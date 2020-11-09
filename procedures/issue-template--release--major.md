Steps to create a MAJOR release
=================================


## Pre-release tasks

- [ ] Merge commits (assign to quicksketch / serundeputy / docwilmot)
- [ ] Create a new minor release (assign to quicksketch / serundeputy)
- [ ] Create the next minor milestone (assign to quicksketch / serundeputy / jenlampton)
- [ ] Move all unfinished issues to the next major release milestone (assign to quicksketch / serundeputy / jenlampton)
- [ ] Draft Release notes (assign to serundeputy / quicksketch / jenlampton)
  - [ ] Short, descriptive summary of the release
  - [ ] Note if any changes were made to files outside the `core` directory
  - [ ] Note if updates (update.php) needs to be run
  - [ ] Include changelog since last version (generated with drush rn)
- [ ] Draft blog post (assign to tomgrandy / klonos / jenlampton / quicksketch)
- [ ] Draft a newsletter via MailChimp (assign to facetinteractive / tomgrandy / jenlampton)


## Release tasks

- [ ] Update bootstrap.inc with version number (assign to quicksketch / serundeputy)
- [ ] Tag for release, and push tag to GitHub (assign to quicksketch / serundeputy)
- [ ] Revert version number back (assign to quicksketch / serundeputy)
- [ ] Create release notes on GitHub (assign to serundeputy / quicksketch / jenlampton)
- [ ] Unpublish preview release on backdropcms.org (assign to serundeputy / quicksketch / jenlampton)
- [ ] Update the front page download link on b.org (assign to serundeputy / quicksketch / jenlampton / klonos)
- [ ] Tweet that a new release is out (assign to quicksketch / jenlampton / jimbirch)


## Post-release tasks (after first bug-fix release or 14 days (whichever comes sooner)

- [ ] Push the major release to the [Pantheon repository](https://github.com/backdrop-ops/backdrop-pantheon) (assign to quicksketch / serundeputy)
- [ ] Push the major release to the [Platform.sh Backdrop repository](https://github.com/platformsh/template-builder/blob/master/project/backdrop.py) (assign to serundeputy / jenlampton)
- [ ] Push the major release to the [Docker repository](https://github.com/docker-library/official-images/blob/master/library/backdrop) (@jenlampton)
- [ ] Update the [Tugboat repository's](https://github.com/backdrop-ops/tugboat-demos) `config.yml` file to link to the new core release @bwpanda
  - [ ] Make new matching tag for Tugboat repo @bwpanda
  - [ ] Build new [Tugboat preview](https://dashboard.tugboat.qa/5fa46514c62ba02c640d3a67) (with no base) from new tag (then make it a base preview) @bwpanda
  - [ ] Update [backdropcms.org](https://backdropcms.org/admin/config/services/tugboat) to use the new Tugboat tag @bwpanda
  - [ ] Delete [Tugboat base preview](https://dashboard.tugboat.qa/5fa46514c62ba02c640d3a67) from two releases ago (i.e. keep last two versions only) @bwpanda
- [ ] Push the major release to the [Backdrop Composer repository](https://github.com/backdrop-ops/backdrop-composer) (assign to quicksketch / serundeputy / herbdool)
- [ ] Publish blog post (assign to tomgrandy / klonos / jenlampton / quicksketch)
- [ ] Send a newsletter via MailChimp (assign to facetinteractive / tomgrandy / jenlampton)
- [ ] email katie@phpweekly.com for a note in the PHP Weekly Newsletter (assign to tomgrandy / klonos / jenlampton)
- [ ] Update the Wikipedia articles (assign to klonos / jenlampton)
  - [ ] https://en.wikipedia.org/wiki/Backdrop_CMS
  - [ ] https://en.wikipedia.org/wiki/List_of_content_management_systems


See the Accompanying Bug-Fix Release Checklist
----------------------------------------------
