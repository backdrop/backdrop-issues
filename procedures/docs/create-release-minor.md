Steps to create a MINOR release
=================================


## Pre-release tasks

- [ ] Merge commits @quicksketch, @serundeputy
- [ ] Create a new minor release to follow the current version
- [ ] Move all unfinished issues to the next minor release
- [ ] Draft Release notes @serundeputy, @quicksketch, @jenlampton
- [ ] Draft blog post @tomgrandy, @klonos, @jenlampton

## Release tasks

- [ ] Update bootstrap.inc with version number @quicksketch, @serundeputy
- [ ] Tag for release, push to GitHub @quicksketch, @serundeputy
- [ ] Create release notes on GitHub @serundeputy, @quicksketch, @jenlampton
- [ ] Revert version number back @quicksketch, @serundeputy
- [ ] Update the front page download link on b.org. @quicksketch
- [ ] Tweet that a new release is out @quicksketch, @jenlampton, @thejimbirch
- [ ] Publish blog post @tomgrandy, @klonos, @jenlampton

## Post-release tasks (asap)

- [ ] Update the docker image to the latest @serundeputy
- [ ] Update the Wikipedia articles to at least show the proper version number and date for latest release @klonos
  - [ ] https://en.wikipedia.org/wiki/Backdrop_CMS
  - [ ] https://en.wikipedia.org/wiki/List_of_content_management_systems

## Post-release tasks (after first bug-fix release)

- [ ] Push the minor release to the Pantheon repository (two weeks after release) @serundeputy
- [ ] Send a newsletter via MailChimp (two weeks after release) @jenlampton
