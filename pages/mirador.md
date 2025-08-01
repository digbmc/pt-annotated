---
layout: default
permalink: mirador.html
---

<!-- Include the CJS version from a CDN or from a local web server, pinned to Mirador v3 -->
<script src="https://unpkg.com/mirador@^3/dist/mirador.min.js"></script>
<!-- By default uses Roboto font. Be sure to load this or change the font -->
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Roboto:300,400,500">
<!-- Container element of Mirador whose id should be passed to the instantiating call as "id" -->
<div id="my-mirador"/> 

<script type="text/javascript">
    // get manifest from embed URL (assuming format <site baseurl>/mirador.html#<manifest url>)
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
                        main: '#f8c667',
                    },
                    shades: {
                        dark: '#000000',
                        main: '#252525',
                        light: '#252525',     
                    }
                }
            },
            dark: {
                palette: {
                    type: 'dark',
                    primary: {
                    main: '#ba55d3',
                    }
                }
            },
            light: {
                palette: {
                    type: 'light',
                    primary: {
                    main: '#ba55d3 ',
                    }
                }
            }
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
            allowWindowSideBar: false,
            hideWindowTitle: true, // Configure if the window title is shown in the window title bar or not
            defaultSideBarPanel: 'annotations',
            sideBarOpenByDefault: true,
            defaultSidebarPanelWidth: 200, // Configure default sidebar width in pixels
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