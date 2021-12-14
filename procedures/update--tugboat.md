# Steps to update Tugboat when a new core release is out

- Go to the `latest` base preview page:
  https://dashboard.tugboat.qa/60815f1e7ceac0f234c0071e
- From the `Actions` dropdown, click `Rebuild...`
  - Tick the `Yes, rebuild this preview` checkbox
  - Click the `Rebuild` button
- Once the base preview has finished rebuilding, go to the
  `backdrop-ops/tugboat-demos` page:
  https://dashboard.tugboat.qa/5fa46514c62ba02c640d3a67
- For each regular preview, click Actions > Delete..., then Yes.

NOTE: When the base preview is rebuilt, the other previews all expand to
full-size and can make our quota go over the limit. We can therefore either
rebuild them as well, or delete them. Since rebuilding them causes them to go
back to the default state and lose all customisation, we just delete them.
