---
layout: default
permalink: mirador.html
---

<!-- Include the CJS version from a CDN or from a local web server -->
<script src="https://unpkg.com/mirador@^3/dist/mirador.min.js"></script>
<!--
  N.B.: The above line will always use the latest version. If a new major version is released,
  your Mirador instance might break. Consider pinning it to a specific major version:
  <script src="https://unpkg.com/mirador@^3/dist/mirador.min.js"></script>
-->
<!-- By default uses Roboto font. Be sure to load this or change the font -->
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Roboto:300,400,500">
<!-- Container element of Mirador whose id should be passed to the instantiating call as "id" -->
<div id="my-mirador"/> 

<script type="text/javascript">
    // get manifest from embed URL
    var manifest = location.href.split("?iiif-content=")[1];
    // configure viewer
    var mirador = Mirador.viewer({
        "id": "my-mirador",
        "manifests": {
            "https://digbmc.github.io/pta-punc-server/index.json": {
            "provider": "Bryn Mawr College"
            }
        },
        "windows": [
            {
            "loadedManifest": manifest,
            "thumbnailNavigationPosition": 'off',
            }
        ],
        window: {
            allowClose: false, // Prevent the user from closing this window
            allowFullscreen: true,
            allowMaximize: false,
            allowTopMenuButton: false,
            defaultSideBarPanel: 'annotations',
            sideBarOpenByDefault: true,
            defaultSidebarPanelWidth: 250, // Configure default sidebar width in pixels
            highlightAllAnnotations: true,
            panels: { // Configure which panels are visible in WindowSideBarButtons
                info: true,
                attribution: false,
                canvas: false,
                annotations: true,
                search: false,
                layers: false,
            },
            views: [ // Only allow the user to select single and gallery view
                { key: 'single' },
            ]
        },
        workspace: {
            type: 'mosaic',
        },
        workspaceControlPanel: {
            enabled: false, // Configure if the control panel should be rendered.  Useful if you want to lock the viewer down to only the configured manifests
        },
        });
</script>