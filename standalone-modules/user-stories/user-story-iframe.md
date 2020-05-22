# Rendering Standalone Modules in an Iframe

To render the module as an iframe you will need the following code in your rendered html.

````
    <script src='https://apps.intocareers.net/javascript/iframeResizer.min.js'></script>
    <iframe src='https://apps.intocareers.net/init/app/MODULE_NAME_GOES_HERE/JWT_GOES_HERE' style="width:100%;border:none;"></iframe>
    <script>iFrameResize({log:false})</script>
````

Note: When mutliple iFrames are on the page you will need to add a unique id to the iframe dom element and target it by replacing line 3 above with:

````
<script> iFrameResize({log:false, checkOrigin: false}, '{YOUR_DOM_ELEMENT_ID')</script>
````

### JWT_GOES_HERE
The JWT created by the backend server will need to be injected here.

### MODULE_NAME_GOES_HERE
The standalone module you wish to access will go here.  I.e. for the Ability Explorer standalone you will have /init/app/AbilityExplorer/JWT_GOES_HERE
