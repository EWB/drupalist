About
=====
Integrates the FlexSlider library into Drupal.

Current Options
---------------
Allows you to use FlexSlider in a few different ways


- As a library to be used with any other theme or module by calling flexslider_add() (N.B. You may also use drupal_add_library('flexslider', 'flexslider') however this is not recommended)
- Integrates with Views Slideshow with FlexSlider Views submodule (80% feature complete) (flexslider_views_slideshow)
- Integrates with Fields (flexslider_fields)
- Adds a Views display mode (flexslider_views)

About FlexSlider
----------------

Library available at https://github.com/woothemes/FlexSlider

- Simple, semantic markup
- Supported in all major browsers
- Horizontal/vertical slide and fade animations
- Multiple slider support, Callback API, and more
- Hardware accelerated touch swipe support
- Custom navigation options
- Use any html elements in the slides
- Built for beginners and pros, alike
- Free to use under the MIT license


Installation
============

1. Download the FlexSlider library from https://github.com/woothemes/FlexSlider
2. Unzip the file and rename the folder to "flexslider" (pay attention to the case of the letters)
3. Put the folder in a libraries directory
    - Ex: sites/all/libraries
4. The first two files are required and the last is optional (required for javascript debugging)
    - jquery.flexslider-min.js
    - flexslider.css
    - jquery.flexslider.js
5. Ensure you have a valid path similar to this one for all files
    - Ex: sites/all/libraries/flexslider/jquery.flexslider-min.js

That's it!

Drush Make
----------

You can also use Drush Make to download the library automatically. Simply copy/paste the 'flexslider.make.example' to 'flexslider.make' or copy the contents of the make file into your own make file.

Usage
======

Option Sets
-----------

No matter how you want to use FlexSlider (with fields, views or views slideshow) you need to define "option sets" to tell FlexSlider how you want it to display. An option set defines all the settings for displaying the slider. Things like slide direction, speed, starting slide, etc... You can define as many option sets as you like and on top of that they're all exportable! Which means you can carry configuration of your Flex Slider instances from one site to the next or create features.

Go to admin/config/media/flexslider

From there you can edit the default option set and define new ones. These will be listed as options in the various forms where you setup FlexSlider to display.  NOTE: under advanced options, you can set a namespace prefix for the optionset.  This will allow you to build custom CSS for each optionset.  Start by copying the flexslider_img.css from the assets subfolder to your theme.  Build new custom CSS for each prefix in your optionsets.

Carousels
---------

Carousels can be created with Flexslider2 by setting an Item Width for images and a Margin Width in the optionset.  Use the flexslider_thumbnail image style and set your item width to fit the desired number of images into the div space available.  NOTE: the margin width setting should correspond IN PIXELS to the margin widths set by your img CSS in your theme.  This will allow Flexslider to properly calculate the "total width" of the image+margins so that horizontal scrolling behaves properly.

Flexslider Views
----------------

Flex Slider Views allows you to build views which display their results in Flex Slider. Similarly to how you can output fields as an "HTML List" or "Table", you can now select "Flex Slider" as an option.

Create or edit a view and ensure it can load a content type which contain image fields. Set your display fields to include an image field. In the field settings, DO NOT SET THE FORMATTER TO FLEXSLIDER. This will attempt to put Flex Sliders inside other Flex Sliders and will just get messy. Ensure you don't include any wrapper markup, labels or container markup for the field value itself. Save your field.

Next, go to "Format" in the main Views windows. Click and select "Flex Slider", then select your option set. Save your view and you should see your results displayed in Flex Slider.

Debugging
---------

You can toggle the development version of the library in the administrative settings page. This will load the unminified version of the library.  Uncheck this when moving to a production site to load the smaller minified version.

Export API
==========

You can export your FlexSlider option presets using CTools exportables. So either using the Bulk Export module or Features.

External Links
==============

- [Wiki Documentation for FlexSlider 2](https://github.com/woothemes/FlexSlider/wiki/FlexSlider-Properties)