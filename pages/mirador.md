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
    var manifest = location.href.split("#")[1];
    // configure viewer
    var mirador = Mirador.viewer({
        "id": "my-mirador",
        "selectedTheme": 'pta',
        themes: {
            pta:{
            palette: {
                type: 'dark',
                primary: {
                    main: '#f6754f',
                    dark: '#f6754f',
                },
                secondary: {
                    main: '#7fff00',
                },
                shades: {
                    dark: '#000000',
                    main: '#1C2122',
                    light: '#1C2122',     
                },
            },
            typography:{
                fontFamily: ['Helvetica'],
            },
            },
            dark: {
            palette: {
                type: 'dark',
                primary: {
                main: '#ba55d3',
                },
            },
            },
            light: {
            palette: {
                type: 'light',
                primary: {
                main: '#ba55d3 ',
                },
            },
            },
        },
        "manifests": {
            "https://digbmc.github.io/pta-manifests/index.json": {
            "provider": "Digital Scholarship at Bryn Mawr College"
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
            hideWindowTitle: true, // Configure if the window title is shown in the window title bar or not
            defaultSideBarPanel: 'annotations',
            sideBarOpenByDefault: true,
            defaultSidebarPanelWidth: 250, // Configure default sidebar width in pixels
            highlightAllAnnotations: true,
            panels: { // Configure which panels are visible in WindowSideBarButtons
                info: false,
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

<!--
<style>
.MuiPaper-root {
    background-color: #000000;
    color: #F8F9FA;
}

.mirador50, .mirador33 {
    background-color: #212529;
}
</style>
-->