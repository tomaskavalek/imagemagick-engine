=== ImageMagick Engine ===
Contributors: orangelab
Tags: image, images, picture, imagemagick, gd
Requires at least: 2.9
Tested up to: 3.1.2
Stable tag: 1.2.3

Improve the quality of re-sized images by replacing standard GD library with ImageMagick.

== Description ==

Dramatically improve the quality of re-sized images by making WordPress use ImageMagick instead of standard GD image library.

Features

* Preserve embedded color profile in re-sized image
* Automatically recognize custom image sizes
* Allow regeneration of existing images (optionally for selected image sizes only)
* Configure image quality or use dynamically computed default value.

Translations: German, Swedish

Requires either ImageMagick binary or Imagick PHP module.

== Installation ==

1. Install either ImageMagick or the Imagick PHP module (see FAQ for more information).
2. Download and extract plugin files to a folder in your wp-content/plugin directory.
3. Activate the plugin through the WordPress admin interface.
4. Configure ImageMagick settings and enable it on plugin settings page.
5. Regenerate existing images to take advantage of the new features.

If you have any questions or problems please make a comment here: http://wp.orangelab.se/imagemagick-engine/

== Frequently Asked Questions ==

= What difference does it make? =

ImageMagick can result in huge improvements in the quality of re-sized images.

Take a look at the supplied screenshot, or try it yourself. More examples will be available on the plugin website (http://wp.orangelab.se/imagemagick-engine/).

Note that the new images tend to be slightly larger than those of the standard GD library, especially if you specify a very high image quality (95+).

= How do I know if I have ImageMagick installed? =

If you have the PHP module installed the plugin will find it. You can check yourself using the phpinfo() function. We also automatically check a common location for the ImageMagick executable.

If you have shell access to a Linux/UNIX server you can use "which convert" to look for the ImageMagick executable.

= How do I install ImageMagick? =

You'll need full access to your server and a bit of technical know-how. If you do not have access you'll have to ask the server administrator.

Don't do it yourself unless you know what you are doing.

Most Linux distributions have a package for "ImageMagick". Some have a package for "php5-imagick". It is possible to install the PHP module using PEAR.

You can also find binary releases at http://www.imagemagick.org including a Windows installer.

= I get a fatal error when activating plugin =

Some webhosts (1and1 for example) need to add a work-around to the .htaccess file.

You might have to add the following line to your .htaccess file:
AddType x-mapp-php5 .php

You'll probably have problems with various other plugins too unless you fix this.

== Screenshots ==

1. Example image: ImageMagick vs GD
2. Administration interface

== Changelog ==

= 1.2.3 =
* Fix bug in resize all images handling, also remove some PHP notices. Thanks to Andreas Kleinschmidt for the report
* Upgrade jQuery UI Progressbar to version 1.8.9, to match version of UI Core in WordPress

= 1.2.2 =
* Fixed filepath with spaces on Windows
* Tested with WordPress 3.1.2
* Added question to FAQ

= 1.2.1 =
* Fix deprecated warning
* Tested with WordPress 3.1

= 1.2.0 =
* Rewrite image cropping for Imagick PHP module to make sure we keep image profiles. Thanks to Christian Münch for report
* Improve test for IM executable
* Administration: AJAXify image resizing, clarify engine selection, only load css/js on actual plugin page
* Handle progressbar version incompatability for jQuery UI 1.8 (in WP 3.1) and jQuery UI 1.7 (in WP 3.0)
* Tested with WordPress 3.1-RC2

= 1.1.2 =
* Fix bug with forced resize of custom image sizes
* Fix warning with open_basedir restriction during path test
* German translation thanks to Dirk Rottig

= 1.1.1 =
* Fix search-and-replace error from 1.1 that made it impossible to change settings! Thanks to Marco M. Jaeger for report!

= 1.1 =
* Working localization
* Added Swedish translation

= 1.0 =
* Initial release

== Upgrade Notice ==

= 1.2.0 =
Fixes plugin jQuery UI script incompatibility for WordPress 3.1
