# jshacks
JS hacks and use cases

## Stop the browser from saving scroll position on page reload

For complex animations this can cause all kinds of problems. This turns Chrome / Safari back into dumb browsers that always start at the top of the page.

    if ('scrollRestoration' in history) {
        history.scrollRestoration = 'manual';
    }

## Stop iOS from zooming

Terrible for accesibility, but sometimes you just want iOS to stop zooming. Works in iOS10.

    document.addEventListener('touchmove', function(event) {
      event = event.originalEvent || event;
      if(event.scale > 1) {
        event.preventDefault();
      }
    }, false);
