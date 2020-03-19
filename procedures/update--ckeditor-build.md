
How to update the custom CKEditor build we use for Backdrop CMS
---------------------------------------------------------------

1) Visit http://ckeditor.com/builder.
1) Upload the core/misc/ckeditor/build-config.js file to the site, indicating
   the plugins that are desired.
1) Save/expand the downloaded archive.
1) Remove the following files/directories from the expanded archive
   - samples
   - ckeditor/skins/moono-lisa/readme.md
   - ckeditor/styles.js
1) Copy the new files into core/misc/ckeditor/*.
