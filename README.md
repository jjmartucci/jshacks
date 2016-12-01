# jshacks
JS hacks and use cases

## Stop the browser from saving scroll position on page reload

For complex animations this can cause all kinds of problems. This turns Chrome / Safari back into dumb browsers that always start at the top of the page.

if ('scrollRestoration' in history) {
  history.scrollRestoration = 'manual';
}
