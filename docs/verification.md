# Verification and evidence limits

These are observed local checks for the initial 0.1.0 source candidate, not a claim of comparative design effectiveness. Hosted checks for a particular revision are visible in the repository's Actions tab.

## Local checks

The final local combined run used Python 3.11.16 and system Chrome 155.0.8059.84:

```sh
HERMES_SOURCE=/path/to/hermes-agent HARDLIGHT_BROWSER_TESTS=1 \
HARDLIGHT_CHROME=/path/to/installed/chrome python -m pytest tests/ -q
python -m ruff check .
python -m build
```

Observed results: **133 tests passed, 81 subtests passed, no skips**; Ruff passed; wheel and source distribution built. The installed wheel was exercised from an isolated Python environment outside the checkout, with no third-party runtime dependencies. All sixteen style packets and nine craft references resolved, the CLI returned JSON, and missing optional browser dependencies produced an explicit failure instead of an installation.

The native test is a fresh subprocess with isolated HOME/HERMES_HOME and the actual Hermes PluginManager/registry. It dispatches all five tools, resolves the bundled skill, invokes the command, renders the discovery section and verifies unload. Native compatibility depends on registration APIs, not merely a version label. CI separately pins a public Hermes revision for its manually requested native job.

Hermes Doctor against a clean public staging tree loaded five tools and zero hooks. The JSON validator passed all fourteen checks without warnings. The bundled skill's selected static schema, Unicode and quality checks passed, with quality **100.0/100**. That is a documentation-quality measurement, not an artistic or security certification.

## Browser and interaction coverage

- Initial wide, narrow and reduced-motion captures cover the three authored demos; the gallery is also exercised by viewport tests.
- Interaction checks cover passage search and recovery, workspace selection/filtering/session edits, literal input rendering, cultural-program filters/disclosures, keyboard focus, direct fragments, browser Back, gallery return paths and meaningful JavaScript-off content.
- Negative browser checks cover denied targets, direct/chained cross-origin redirects, credential-bearing requests, unsupported contrast paint, missing browsers, setup/navigation failures and fresh-report replacement. Paint regressions include text-fill/stroke/SVG, inset shadows, multiple shadows and non-default background clipping on elements and ancestors, with ordinary passing/failing text and outer-shadow controls across all three captures. A denied sink must receive no request.
- A simulated cp1252 default exercises the actual example-source readers. This is regression coverage on Linux; it is not a claim that a Windows browser was run locally.
- Installed system Chrome is the real local browser path. Playwright Chromium discovery/cleanup has deterministic tests, but its real fallback launch was unavailable locally. The hosted browser job explicitly provisions Chromium and rejects skipped browser checks; inspect that run's evidence separately.

Private research captures, local project paths and test logs are not distributed. The public showcase contains only original example screenshots.

## What these checks do not establish

No user study, conversion experiment, screen-reader matrix, full WCAG audit, field Core Web Vitals measurement or statistical comparison with Impeccable was performed. The local browser runner samples initial main-document states and conservative findings; it does not click through an application or replace interaction testing. Unknown paint, iframe/shadow content, truncation and untested states are not passing results.

Source inspection needs safe POSIX no-follow/directory-relative APIs and returns an explicit unsupported-platform error otherwise. The runtime does not install itself, remove another skill, mutate a live profile, publish projects or fetch design references automatically. Source publication and successful tests are separate from activation in any running Hermes process.
