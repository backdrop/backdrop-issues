Steps to create a MAJOR release
=================================


## Pre-release tasks

- [ ] Merge commits @quicksketch, @serundeputy, @docwilmot
- [ ] Create a new minor release to follow the current version
- [ ] Move all unfinished issues to the next major release milestone @quicksketch, @serundeputy
- [ ] Draft Release notes @quicksketch, @serundeputy
- [ ] Draft blog post @tomgrandy, @klonos, @jenlampton
- [ ] Draft a newsletter via MailChimp

## Release tasks

- [ ] Update bootstrap.inc with version number @quicksketch, @serundeputy
- [ ] Tag for release, push to GitHub @quicksketch, @serundeputy
- [ ] Revert version number back @quicksketch, @serundeputy
- [ ] Create release notes on GitHub @serundeputy, @quicksketch
- [ ] Update the front page download link on b.org. @quicksketch, @serundeputy
- [ ] Tweet that a new version is out @quicksketch, @jenlampton, @thejimbirch
- [ ] Publish blog post @tomgrandy, @klonos, @jenlampton

## Post-release tasks

- [ ] Update the docker image to the latest @serundeputy
- [ ] Update the Wikipedia articles to at least show the proper version number and date for latest release @klonos
  - [ ] https://en.wikipedia.org/wiki/Backdrop_CMS
  - [ ] https://en.wikipedia.org/wiki/List_of_content_management_systems

## Post-release tasks (after first bug-fix release)

- [ ] Push the minor release to the Pantheon repository @serundeputy
- [ ] Send a newsletter via MailChimp @jenlampton
