
How to update the custom CKEditor build we use for Backdrop CMS
---------------------------------------------------------------

1) Visit http://ckeditor.com/builder.
1) Upload the core/misc/ckeditor/build-config.js file to the site, indicating
   the plugins that are desired.
1) Save/expand the downloaded archive.
1) Remove the following files/directories from the expanded archive
   - `README.md`,
   - `adapters`,
   - `config.js`,
   - `contents.css`,
   - `samples`,
   - `skins/moono-lisa/readme.md`,
   - `styles.js`,
1) Copy the new files into core/misc/ckeditor/*.
1) Double check that the `build-config.js` file retains 2 sections of code
   that are specific to Backdrop:
   - Docblock at the very top of the file
   - Around line 60, list of files that need to be removed from the build
1) Update the `define('CKEDITOR_VERSION', 'x.y.z');` line in
   `core/modules/ckeditor/ckeditor.module` to reflect the new CKEditor
   version.
