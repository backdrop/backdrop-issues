# Bug-Fix Release notes

1) Git clone repository for backdrop/backdrop (or git pull 1.x branch)  
   Run the command `git pull core 1.x`  
   (where 'core' is the remote and '1.x' is the branch)
2) Checkout the latest bug-fix branch  
   Run the command `git checkout 1.11.x`  
   (where 1.11.x is the latest bug-fix branch)
3) Get all the latest tags  
   Run the command `git fetch --tags`
4) Generate release notes  
   Run the command `drush rn 1.11.3 HEAD > ~/Desktop/notes.md`  
   (where 1.11.3 is the latest release)


# Minor Version Release notes

The release notes for minor versions are generated automatically, based on
issues assigned to the minor version's milestone.

1) Go to the 'Milestones' page in the `backdrop-issues` repo:
   https://github.com/backdrop/backdrop-issues/milestones
2) Close the milestone for this minor version (this triggers the generation of
   the release notes)
3) Go to the 'Actions' page in the `backdrop-issues` repo:
   https://github.com/backdrop/backdrop-issues/actions
4) A 'Release Notes Generator' workflow should be in progress - wait until it's
   done, then click on it
5) Scroll down to the 'Artifacts' section and click on the 'release-notes'
   download - this ZIP file contains a markdown file with the generated release
   notes for this minor version
