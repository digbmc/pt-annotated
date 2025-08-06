---
layout: default
permalink: glycerine.html
---

<!-- Create a container for the Glycerine Viewer -->
<div id="viewer"></div>

<!-- Include the Glycerine Viewer script -->
<script src="https://unpkg.com/glycerine-viewer@latest/jslib/glycerine-viewer.umd.cjs"></script>

<script>
    // Get the container element for the viewer.
    const ele = document.getElementById('viewer')

    // Create a new GlycerineViewer instance.
    const viewer = new GlycerineViewer(ele, {
        width: '100%',
        height: '100vh',
        manifest: location.href.split("#")[1],
        defaultInfoPanel: false,
        showIndexButton: false,
        showAboutPaneButton: false,
        showAnnotationViewButton: false,
        showSettingPaneButton: false,
        enableDropManifest: false,
    });
    
    // Initialize the viewer.
    viewer.init();
</script>