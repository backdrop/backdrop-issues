Steps to create a MINOR release
=================================


Accompanying Bug-Fix Release Checklist
---------------------------------------


## Pre-release tasks

- [ ] Merge commits @quicksketch, @serundeputy, @docwilmot
- [ ] Create a new bugfix release @quicksketch, @serundeputy
- [ ] Move all unfinished issues to the next bugfix release milestone @quicksketch, @serundeputy
- [ ] Draft Release notes @quicksketch, @serundeputy

## Release tasks

- [ ] Update bootstrap.inc with version number @quicksketch, @serundeputy
- [ ] Tag for release, push to GitHub @quicksketch, @serundeputy
- [ ] Create release notes on GitHub @quicksketch, @serundeputy
- [ ] Revert version number back @quicksketch, @serundeputy


Minor Release Checklist
------------------------


## Pre-release tasks

- [ ] Merge commits @quicksketch, @serundeputy, @docwilmot
- [ ] Create a new minor release to follow the current version
- [ ] Move all unfinished issues to the next minor release milestone @quicksketch, @serundeputy
- [ ] Draft Release notes @quicksketch, @serundeputy
- [ ] Draft blog post @tomgrandy, @klonos, @jenlampton
- [ ] Draft a newsletter via MailChimp

## Release tasks

- [ ] Update bootstrap.inc with version number @quicksketch, @serundeputy
- [ ] Tag for release, push to GitHub @quicksketch, @serundeputy
- [ ] Revert version number back @quicksketch, @serundeputy
- [ ] Create release notes on GitHub @serundeputy, @quicksketch
- [ ] Unpublish preview release on backdropcms.org @quicksketch, @serundeputy
- [ ] Update the front page download link on b.org. @quicksketch, @serundeputy
- [ ] Tweet that a new release is out @quicksketch, @jenlampton, @thejimbirch
- [ ] Publish blog post @tomgrandy, @klonos, @jenlampton
- [ ] email katie@phpweekly.com for a note in the PHP Weekly Newsletter @jenlampton, ??

## Post-release tasks (asap)

- [ ] Update the docker image to the latest @serundeputy
- [ ] Update the [Roadmap](https://backdropcms.org/roadmap) page on b.org, @klonos:
  - "Project History and Future" section:
    - [ ] Add a new entry for the next minor release in the list of releases
    - [ ] Move the "(current release)" pointer to the current release entry
  - Add a section for the next-to-next release in the main text:
    - [ ] Copy-paste the "New features planned for ..." section and change the version number, release date and GitHub issue tracker link
  - In the section for the current release:
    - [ ] Change the "New features planned for" to "Key features in" in the section title
    - [ ] Change the star icon to a checkbox icon (`class="fa fa-star-o"` to `class="fa fa-check-square-o"`)
    - [ ] Add a "([release notes]())" link
    - [ ] Add an [announcement]() link (when respective blog post is published)
    - [ ] Update the list of features as necessary, according to release notes
    - [ ] Remove the "See the Github issue tracker..." item
- [ ] Update the Wikipedia articles to at least show the proper version number and date for latest release @klonos
  - [ ] https://en.wikipedia.org/wiki/Backdrop_CMS
  - [ ] https://en.wikipedia.org/wiki/List_of_content_management_systems

## Post-release tasks (after first bug-fix release)

- [ ] Push the minor release to the Pantheon repository @serundeputy
- [ ] Send a newsletter via MailChimp @jenlampton
