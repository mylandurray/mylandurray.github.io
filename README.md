# mylandurray.github.io

The homepage for my print-production tools: <https://mylandurray.github.io/>.

It's one self-contained `index.html` (no build step). Web apps are listed in the
`APPS` array and desktop downloads in `DOWNLOADS`; each app is served from its own
repo's Pages site at `/<repo>/`. Desktop installers are read from GitHub Releases on
the public `downloads` repo, and show "Not published yet" until a release exists.

Push to `main` and GitHub Pages republishes the site.
