# Steps to update Tugboat when a new core release is out

- Go to the `latest` base preview page:
  https://dashboard.tugboat.qa/60815f1e7ceac0f234c0071e
- From the `Actions` dropdown, click `Rebuild...`
- Tick the following checkboxes:
  - Yes, rebuild this preview
  - Rebuild previews built from this one when finished
- Click the `Rebuild` button
- Once the base preview has finished rebuilding, go to the
  `backdrop-ops/tugboat-demos` page:
  https://dashboard.tugboat.qa/5fa46514c62ba02c640d3a67
- For each regular preview, click Actions > Rebuild..., then Yes.
