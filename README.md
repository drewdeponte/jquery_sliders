jQuery Sliders Plugin
=====================

The jQuery Sliders Plugin is a simple slideshow plugin that attempts to be very generic. It does so by allowing the slides to be any HTML element and leaving the sizing, positioning, and styling in general to CSS as it should be.

Basic Setup
-----------

This plugin provides two necessary files in order to use this plugin.

### jquery.sliders.js

The first is ```jquery.sliders.js```. This is the actually jQuery Sliders plugin file. It must be included in the head section of your page similar to the following:

    <script language="javascript" type="text/javascript" src="../jquery.sliders.js"></script>

Note: The above example was pulled from ```examples/index.html``` so your path is likely going to be different as you will need to include ```jquery.sliders.js``` in your web application somewhere.

### jquery.sliders.css

The second is ```jquery.sliders.css```. This is a starter stylesheet for the jQuery Sliders plugin. It is setup to match the defaults in the jQuery Sliders plugin options. It must be included in the head section of your page similar to the following:

    <link rel="stylesheet" type="text/css" href="../stylesheets/jquery.sliders.css">

Note: The above example was pulled from ```examples/index.html``` so your path is likely going to be different as you will need to include ```jquery.sliders.css``` in your web application somewhere.

The ```jquery.sliders.css``` file tries to provide you with the bare minimum styling for the defaults of the plugin so that the plugin will function properly, yet it won't interefere with other styles in your application. It also gives you the capabilities of further defining the styles of your slides and the slideshow in your application.

Basic Usage
-----------

Once the setup has been completed and the ```jquery.sliders.js``` is being loaded properly nad the ```jquery.sliders.css``` is being loaded properly. It is time to actually use the jQuery Sliders plugin. For sake of discussion lets assume that if you have the following HTML on your page.

    <div id="slideshow1" class="sliders">
      <div class="active-slide slide">hello</div>
      <div class="slide">world</div>
      <div class="slide">again</div>
    </div>

Inside of the ```head``` tags provide the following snippet call the most basic usage of the jQuery Sliders plugin assume the above HTML.

    <script type="text/javascript">
      $(document).ready(function () {
        $("#slideshow1").sliders();
      });
    </script>

The above code initializes the jQuery Sliders plugin with default options on the jQuery selector ```#slideshow1```.

Advanced Usage (Options)
------------------------

The jQuery Sliders plugin gives you some flexibility by providing the option to override the default options. You can do this by passing a hash of the option keys and values to the sliders() method. An example is provided below.

    <script type="text/javascript">
      $(document).ready(function () {
        $("#slideshow1").sliders({
            interval: 2000,
            selector: "#car_slide"
          });
      });
    </script>

### Options

The following are the available options and what they mean:

 * interval - interval at which the slides will change in milliseconds
 * selector - selector used to identify slides (think how do I identify a slide)
 * active_class - class used to identify the active slide (should only be used if you are twiddling with the CSS)
 * last_active_class - class used to identify the last active slide (should only be used if you are twiddling with the CSS)
