<!doctype html>
<html lang="en" class="h-100" data-bs-theme="dark">
  <head prefix="og: http://ogp.me/ns#">
    {% include head/head.html %}
  </head>
  <body>
    <main id="maincontent" role="main" class="flex-shrink-0">
      <div class="container-fluid my-4">
    {{ content }}
        </div>
    </main>
  </body>

  <script>
    function addNoOpener(link) {
      let linkTypes = (link.getAttribute('rel') || '').split(' ');
      if (!linkTypes.includes('noopener')) {
        linkTypes.push('noopener');
      }
      link.setAttribute('rel', linkTypes.join(' ').trim());
    }

    function addNewTabMessage(link) {
      if (!link.querySelector('.visually-hidden')) {
        link.insertAdjacentHTML('beforeend', ' <svg class="bi icon-sprite external-link-icon" aria-hidden="true"><use xlink:href="{{ '/assets/lib/icons/box-arrow-up-right.svg' | relative_url }}"/></svg><span class="visually-hidden">(opens in a new tab)</span>');
      }
    }

    document.querySelectorAll('a[target="_blank"]').forEach(link => {
      addNoOpener(link);
      addNewTabMessage(link);
    });
  </script>
</html>
