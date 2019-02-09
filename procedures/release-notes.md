# Bug-Fix Release notes.
------------------------

1) Git clone repository for backdrop/backdrop (or git pull 1.x branch)
   Run the command `git pull core 1.x`
     where 'core' is the remote and '1.x' is the branch.
2) Checkout the latest bug-fix branch.
   Run the command `git checkout 1.11.x`
     where where 1.11.x is the latest bug-fix branch.
3) Get all the latest tags.
   Run the command `git fetch --tags`
4) Generate release notes.
   Run the command `drush rn 1.11.3 HEAD > ~/Desktop/notes.md`
     where 1.11.3 is the latest release.


# Minor Version Release notes.
------------------------------

1) Git clone repository for backdrop/backdrop (or git pull 1.x branch)
   Run the command `git pull core 1.x`
     where 'core' is the remote and '1.x' is the branch.
2) Get a list of all changes since the previous minor version
   Run the command `drush rn 1.11.0 HEAD`
   Review all the issues, remove anything that was committed to a bug-fix release


To check for changes to files outside the core directory:

 `git diff mybranch..1.x -- .htaccess`
 `git diff mybranch..1.x -- settings.php`
 `git diff mybranch..1.x -- robots.txt`
