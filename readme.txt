** NOTE ** THIS CODE IS A FORK OF ANOTHER PROJECT. I HAVE MODIFIED THIS PROJECT TO ADD SOME FUNCTIONALITY OF MY OWN. I DO NOT TAKE CREDIT FOR THIS PROJECT, ONLY THE CHANGES AND ADDITIONS MADE BY ME, WHICH ARE NOTED IN THE FILES LISTS AND DESCRIPTION BELOW -- Kelli 

2018-02-16 -- added code to sac.php to use data from freegeopip.net to create default usernames based on geolocation data. Also added code to restrict usernames that unregistered users can create in the chat box. Changes the "guestXXXX" default username to "CitySTUserXXXX".

PLEASE NOTE: If you are using WP SUPER CACHE or any other type of caching in Wordpress, you must disable it for the url(s) of the pages utilising the chat box, or usernames will be duplicated and other bad things will happen.

=== Simple Ajax Chat ===

Plugin Name: Simple Ajax Chat
Plugin URI: https://perishablepress.com/simple-ajax-chat/
Description: Displays a fully customizable Ajax-powered chat box anywhere on your site.
Tags: chat, box, ajax, forum, private, avatars, filtering, smilies, secure, antispam, html5, messaging, im, instant message
Author: Jeff Starr
Author URI: http://monzilla.biz/
Donate link: http://m0n.co/donate
Contributors: specialk
Requires at least: 4.0
Tested up to: 4.3
Stable tag: trunk
Version: 20150808
Text Domain: sac
Domain Path: /languages/
License: GPL v2 or later

Simple Ajax Chat displays a fully customizable Ajax-powered chat box anywhere on your site.

== Description ==

__IMPORTANT:__ if you are upgrading from version less than 20150316, please read the [upgrade instructions](https://wordpress.org/plugins/simple-ajax-chat/installation/)

Simple Ajax Chat makes it easy for your visitors to chat with each other on your website. There already are a number of decent chat plugins, but I wanted one that is simple yet fully customizable with all the features AND outputs clean HTML markup.

**Features**

* Strong anti-spam filters
* Plug-n-play functionality
* Designed to be the simplest possible *persistent* chat
* No configuration required, just include shortcode or template tag
* Display on any post or page with the shortcode
* Display anywhere in your theme template with the template tag
* Includes default CSS styles and enables custom CSS from the settings
* JavaScript/Ajax goodness loads new chats without refreshing the page
* Also works when JavaScript is not available on the user's browser
* Clean markup makes it easy to style the appearance as you please
* New chat messages fade-in with custom duration and color
* Includes manage-chats panel for editing and deleting chats
* Links included in chats include `_blank` target attributes
* Includes complete map of all available CSS hooks
* Includes built-in banned-phrases list
* Automatic smileys supported :)
* On-demand restoration of all default settings
* Super-slick toggling settings page
* Option to play sound alert for chat messages
* Timestamp for each chat message
* Display chat messages in ascending or descending order
* NEW: option to use logged-in username as the chat name

**Customize everything**

* Customize the update interval for the Ajax-requests
* Customize the fade-duration for new chat messages
* Customize the intro and outro colors for new chats
* Option to require login/registration to participate
* Option to enable/disable URL field for usernames
* Option to use textarea for larger input field
* Customize the default message and admin name
* Customize the appearance with your own CSS
* Option to enable/disable custom styles
* Option to load the JavaScript only when the chat box is displayed
* Add custom content to the chat box and chat form
* Built-in control panel to edit and delete chats
* Built-in blacklist to ban specific phrases from the chat

== Installation ==

= Installation =

Activate the plugin and visit the SAC settings page to customize your options.

Once everything is customized as you like it, display the form anywhere using the shortcode or template tag.

[More info on installing WP plugins](http://codex.wordpress.org/Managing_Plugins#Installing_Plugins)

= Upgrading =

__IMPORTANT:__ the time functionality has been upgraded in version 20150316. As a result, all chat messages will be deleted when the plugin is upgraded to the latest version. If you want to save your current chats, please make a backup BEFORE upgrading. This applies only to people who are upgrading from a version less than 20150316.

__ALSO:__ After upgrading, if your chat box displays something like "you need at least one message..", do the following:

1. Backup or make a note of your chat settings (so you can restore them)
2. Click the "Restore default settings" button
3. Reconfigure your settings and done

Apologies for the inconvenience, but the plugin is better off using WP time functionality.

= Shortcode =

Use this shortcode to display the chat box on a post or page:

`[sac_happens]`

= Template tag =

Use this template tag to display the chat box anywhere in your theme template:

`&lt;?php if (function_exists('simple_ajax_chat')) simple_ajax_chat(); ?&gt;`

= Stopping spam =

This plugin works in two modes:

* "Open air" mode - anyone can comment
* "Private" mode - only logged in users may comment

In terms of chat spam, the "open air" mode is much improved at blocking spam, but some spam still gets through the filters. As a general rule, the longer your chat forum is online, the more of a target it will be for spammers.

If you absolutely don't want any spam, run the plugin in "private" mode. In private mode, the chat forum will require login to view and use, and no spam should make it through.

Alternately/optionally you may use the included .htaccess file to add some simple rules to block users by IP and other variables.

= Other notes =

If the chat form looks messed up on your theme, try disabling the checkbox for "Enable custom styles?"

If that doesn't help, you can include your own custom CSS. To do so, replace the "Custom CSS styles" with your own, and then enable the "Enable custom styles?" setting. Alternately, you may include custom CSS via your theme's stylesheet.

If your site's `wp-blog-header.php` and `wp-config.php` are not located in the usual default location (i.e., you have moved them to a custom location), you will need to edit the paths in `/simple-ajax-chat.php` (line 4) and `/resources/sac.php` (line 9). At some point I will be revamping the way that these files are included so that this modification won't be necessary.

== Upgrade Notice ==

__IMPORTANT:__ the time functionality has been upgraded in version of the plugin. As a result, all chat messages will be deleted when the plugin is upgraded to the latest version. If you want to save your current chats, please make a backup BEFORE upgrading.

__ALSO:__ After upgrading, if your chat box displays something like "you need at least one message.." do the following:

1. Backup or make a note of your chat settings (so you can restore them)
2. Click the "Restore default settings" button
3. Reconfigure your settings and done

Apologies for the inconvenience, but the plugin is better off using WP time functionality.

== Screenshots ==

Screenshots available at the [SAC Homepage](https://perishablepress.com/simple-ajax-chat/#screenshots).

Live Demo available at [WP-Mix](https://wp-mix.com/chat/).

== Changelog ==

= 20150808 =

* Tested on WordPress 4.3
* Updated minimum version requirement
* Fixed 404/500 error for certain setups

= 20150507 =

* Tested with WP 4.2 + 4.3 (alpha)
* Changed a few "http" links to "https"
* Fixed XSS vulnerability with add_query_arg()
* Added primary key flag to create database function
* Bugfix: form not submitting when JavaScript disabled
* Improved logic in simple-ajax-chat.php
* Added nonce security to chat form
* Added support for SSL/https
* Added sac_censor_replace filter to customize censored words
* Added isset() to stop PHP warning

= 20150316 =

* Tested with latest version of WP (4.1)
* Increased minimum version to WP 3.8
* Added $sac_wp_vers for version check
* Added Text Domain and Domain Path to file header
* Removed deprecated screen_icon()
* Added alert notice for donations
* Streamline/fine-tune plugin code
* Replaced time() with current_time() throughout plugin
* Added timestamp for each chat via data-time attribute
* Replace $user_level and $sac_admin_user_level with current_user_can()
* New feature: option to set max number of allowed chats
* New feature: option to set max number of characters per chat
* New feature: option to set max number of characters in username
* Replaced hard-coded values for max chats/chars/name with options
* Revamped chat-order functionality (Thanks to MartinW2)
* Added line breaks to initJavaScript()
* Added rows="5" cols="50" to chat message textarea
* Updated auto-link regex, fixes backslash appended to URL
* Think I fixed the backslash-before-apostrophes issue, let me know!
* Replaced default .mo/.po templates with .pot template

= 20140923 =

* Tested on latest version of WordPress (4.0)
* Increased minimum version requirement to WP 3.7
* Added conditional check to min-version function
* Added option to display logged-in username as chat name
* Improved logic of simple_ajax_chat()
* Improved logic of sac_addData()
* Improved logic in core and admin files
* Increased default username max-length
* Fine-tuned plugin settings page
* Removed vestigial killswitch variable
* Fixed issue where special characters were not displaying correctly
* Replaced hardcoded paths with WP tags (e.g., wp-content directory)
* Replaced $user_nickname global with wp_get_current_user()
* Minified portions of the SAC JavaScript file for better performance
* Added conditional check for $sac_lastID is numeric
* Now using sanitize_text_field() for IPs
* Replaced htmlspecialchars() with sanitize_text_field()
* Replaced sac_special_chars() with esc_url() for user URL
* Replaced htmlentities(), stripslashes(), sac_clean() with sanitize_text_field()
* Replaced PHP tags with WP tags in sac_special_chars()
* Updated mo/po translation files

= 20140305 =

* New feature: added setting to display chats in ascending or descending order (beta)
* Improved logic for creating chat db table, fixes "mysql_list_tables" deprecated error
* Added various CSS selectors to chat messages for custom styling
* Added support for localization/translation

= 20140123 =

* Tested with latest WordPress (3.8)
* Added trailing slash to load_plugin_textdomain()
* Fixed 3 incorrect _e() tags in simple-sjax-chat-admin.php
* Edited setting description for "Require log in?" for accuracy

= 20131107 =

* Removed `delete_option('sac_delete');` from uninstall.php
* Replaced `application/x-javascript` with `` in sac.php
* Replaced `add_plugin_links` with `add_sac_links` in simple-ajax-core.php

= 20131106 =

* Replaced original header codes and WP includes in sac.php

= 20131105 =

* Removed 3x "&Delta;" from die() for better security
* Added "rate this plugin" link on Plugins and SAC settings screens
* Replaced 3x "wpdb->escape" with "esc_sql" in simple-ajax-chat-core.php
* Filter server variables with built-in simple-ajax-chat-admin.php (lines 65/66)
* Improved security when submitted chat fails (simple-ajax-chat.php)
* Specified no border for smileys in filter_smilies()
* Added localized timestamp of last chat to span.name in sac.php
* Localized "ago" in sac-admin, sac-core, and sac-form
* Localized sac_time_since() in simple-ajax-core.php
* Improved header codes and WP includes in sac.php
* Fixed bug where chats don't work if audio is disabled
* Added uninstall.php to remove options and chat table upon uninstall
* Enhanced functionality of plugin settings page
* Tested with latest version of WordPress (3.7)
* General code maintenance and cleanup
* Added support for localization

= 20130725 =

* Tightened form security
* Tightened plugin security
* Updated deprecated functions
* Resolved some PHP Notices

= 20130713 =

* Improved localization support
* Replaced some deprecated template tags

= 20130712 =

* Reorganized file/directory structure
* Separated Ajax stuff from core plugin
* Implemented strong anti-spam measures
* Many functions rewritten to maximize native WP functionality
* Improved audio support for chat alerts, fixed Safari bug
* Fixed: case-insensitive banned phrases
* Fixed: default options not working on install
* Fixed: a bunch of annoying PHP Notices
* Added .sac-reg-req for registration message div#sac-panel
* Updated CSS skeleton with new selector (@ "/resources/sac.css")
* Fixed: enable/disable links for usernames now works properly
* General code check n clean
* added comments to the .htaccess file (no active rules are included)

= 20130104 =

* Added JavaScript to set up sound-alerts (fixes undefined variable error)

= 20130103 =

* Added margins to submit buttons (now required in WP 3.5)
* Added "div#sac-panel p {}" to default CSS
* Added links to demo in readme.txt file
* Updated all instances of $wpdb->prepare with new syntax
* Added option for sound to play for new chat messages (note: chat-sound technique is borrowed from "Pierre's Wordspew")

= 20121206 =

* Edited line 217 to define variable and fix "timeout" error
* Enhanced markup for custom content
* Custom content may be added before and/or after the chat form and/or the list of chat messages

= 20121119 =

* Fixed PHP Warning: [function.stristr]: Empty delimiter (line 282)
* Removed fieldset border in default form styles (plugin settings)
* Added placeholders for name, URL, and chat message

= 20121110 =

* Initial release.

== Frequently Asked Questions ==

Question: "Can we auto delete after some minutes all the chats?"

Answer: Yes, please see this post: [WordPress Cron Tips](https://wp-mix.com/wordpress-cron-tips/)

Question: "I'm interested to know if your chat plugin has the option to respond to chats via an iPhone app or another chat software. I didn't see how the chats are received."

Answer: Yep, the chat plugin works great on iPhones, Android devices, and more.. the functionality is achieved using Ajax.

Question: "In some cases a backslash is added before a single apostrophe "`'`", how do I fix?"

Answer: In the plugin settings, add a backslash "`\`" to the exclude list ("Banned Phrases" panel).

Question: "How do I change the maximum number of characters/messages?"

Answer: This is possible by editing the variables in `simple-ajax-core.php` (see "plugin variables"). Note: the planned "Pro" version of the plugin will include plugin settings for controlling these variables.

Question: "Is it possible to whitelist SAC plugin files?"

Answer: Yes, check out [Simple Ajax Chat .htaccess whitelist](https://wp-mix.com/simple-ajax-chat-htaccess-whitelist/) and/or [Whitelist POST access with .htaccess](https://wp-mix.com/whitelist-post-access-htaccess/)

To ask a question, visit the [SAC Homepage](https://perishablepress.com/simple-ajax-chat/) or [contact me](https://perishablepress.com/contact/).

== Donations ==

I created this plugin with love for the WP community. To show support, you can [make a donation](http://m0n.co/donate) or purchase one of my books: 

* [The Tao of WordPress](https://wp-tao.com/)
* [Digging into WordPress](https://digwp.com/)
* [.htaccess made easy](https://htaccessbook.com/)
* [WordPress Themes In Depth](https://wp-tao.com/wordpress-themes-book/)

Links, tweets and likes also appreciated. Thanks! :)
