# Gridster #

## Description ##
Gridster is a WordPress plugin that makes building intuitive draggable layouts from elements spanning multiple columns. You can even dynamically resize, add and remove elements from the grid, as edit the elements content inline.

**Tags:** 							GUI, gridster, layout management, drag & drop, grid, multi-column, columns, user-friendly, shortcode

**Author URI:**       	http://carsten-bach.de

**Author:**            	Carsten Bach

**Requires at least:** 	3.3

**Tested up to:** 			3.5.1

**Stable tag:** 				1.1

**License:**            GPLv2 or later

**License URI:**        http://www.gnu.org/licenses/gpl-2.0.html
  


### General - Features ###

*  manage your contents within a grid
*  drag & drop contents as gridster widgets from your last posts, pages or custom post types
*  resize gridster widgets on the fly
*  use custom templates for all your gridster-widgets, or per post_type
*  override side wide settings for every gridster
*  inline edit every content loaded via your templates
*  images within your gridster-widgets are re-loaded on every resize of a widget, to best fit its dimensions
*  add gridsters by simply adding a generated shortcode, you'll get from the gridsters post-list 
*  this plugin recognizes your defined content width from your theme and will help you create best fitting gridsters
*  scripts & styles are loaded only if shortcode is really used, this saves load time
*  visual shortcode replacement, like you know from [gallery]-Shortcode
*  TinyMCE Button to add gridster layouts with user-friendly GUI
*  clean uninstall: all options, gridster-posts and related post-meta fields are deleted on uninstalling (not deactivation)
  


### Templates ###

Adjust the HTML output of the gridster-widgets by overriding the default template from `cbach-wp-gridster/views/gridster-default.php`.
Just copy this file into a new created directory `gridster-templates` within your theme folder and change it to your needs. 
Furthermore you can add different templates per post_type, when you create files like `gridster-YOUR_POST_TYPE_NAME.php` within these folder.

By using the later described `gridster_locate_templates_from` filter you are able to add more conditions to make your templates match more customized conditions. 



### Inline editing ###

With help of the [Jeditable](http://www.appelsiini.net/projects/jeditable) library it is possible to edit loaded content directly inside the gridster workbench.
So if you are using a post called "My grandmothers apple pie is the best", you could adjust the text inside your gridster-widget to shorter version, ie. "best apple pie" without editing the original post.
Just add some CSS class to the wrapper element, where your title will appear.

For editing single lines of text, like titles add `class="gridster_edit"`.
If you want to edit texts in more comfortable textarea use `class="gridster_edit-area"`

Have a look at the `/views/gridster-default.php` inside the plugin directory to get a clue. 





## Installation ##

1.  Extract the zip file
2.  Drop the contents in the `wp-content/plugins/` directory of your WordPress installation
3.  Activate the plugin from plugins page






## Frequently Asked Questions ##
In the moment, there is no question I know about.

Maybe you've some?!
Drop me a line at gridster@carsten-bach.de




## Screenshots ##

###1. Create a new Gridster by dragging your content from the Lists of your posttypes left to the workbench on the right. (with WordPress 3.5.1)###
![Create a new Gridster by dragging your content from the Lists of your posttypes left to the workbench on the right. (with WordPress 3.5.1)](https://raw.github.com/carstingaxion/cbach-wp-gridster/master/screenshot-1.jpg)

###2. Move the Gridster-Widgets around via drag & drop. Underlying Widgets are re-layoutet on the fly. (with WordPress 3.5.1)###
![Move the Gridster-Widgets around via drag & drop. Underlying Widgets are re-layoutet on the fly. (with WordPress 3.5.1)](https://raw.github.com/carstingaxion/cbach-wp-gridster/master/screenshot-2.jpg)

###3. Resize the Gridster-Widgets and get updated Images directly inside the workbench. The Plugin looks for the best fitting size according to your defined Thumbnail-Image-Sizes. (with WordPress 3.5.1)###
![Resize the Gridster-Widgets and get updated Images directly inside the workbench. The Plugin looks for the best fitting size according to your defined Thumbnail-Image-Sizes. (with WordPress 3.5.1)](https://raw.github.com/carstingaxion/cbach-wp-gridster/master/screenshot-3.jpg)

###4. After adding a new Gridster-Widget it is pre-populated with Title and Excerpt of the fetched post. Now you are able to inline edit theese texts, without the need to modify the original post. (with WordPress 3.5.1)###
![After adding a new Gridster-Widget it is pre-populated with Title and Excerpt of the fetched post. Now you are able to inline edit theese texts, without the need to modify the original post. (with WordPress 3.5.1)](https://raw.github.com/carstingaxion/cbach-wp-gridster/master/screenshot-4.jpg)

###5. You have two different types of inline-editors: input-fields and textareas. Define the editable content blocks by customizing the Gridster-Widget Templates within your Theme. (with WordPress 3.5.1)###
![You have two different types of inline-editors: input-fields and textareas. Define the editable content blocks by customizing the Gridster-Widget Templates within your Theme. (with WordPress 3.5.1)](https://raw.github.com/carstingaxion/cbach-wp-gridster/master/screenshot-5.jpg)
  
###6. A list of all Gridster posts, also showing the Shortcodes. (with WordPress 3.5.1)###
![A list of all Gridster posts, also showing the Shortcodes. (with WordPress 3.5.1)](https://raw.github.com/carstingaxion/cbach-wp-gridster/master/screenshot-6.jpg)

###7. An embeded Shortcode inside the Editor is replaced by visual placeholder, to keep things easy for your editors. No need to write (short-)code. Besides it's possible to update, edit and delete the shortcode via icons, formerly known from the gallery-shortcode. (with WordPress 3.5.1) ###
![An embeded Shortcode inside the Editor is replaced by visual placeholder, to keep things easy for your editors. No need to write (short-)code. Besides it's possible to update, edit and delete the shortcode via icons, formerly known from the gallery-shortcode. (with WordPress 3.5.1)](https://raw.github.com/carstingaxion/cbach-wp-gridster/master/screenshot-7.jpg)






## Changelog ##

### 1.1 ###
* Added TinyMCE Button to add shortcode
* Added visual shortcode replacement inside the editor, similar to the gallery-shortcode, with handle-buttons for changing the current shortcode, editing the related gridster and deleting the shortcode from the content
* Added Pagination to post-lists available as gridster-widgets
* Added Search to post_type blocks, to look for posts (and pages and custom post_types) usable as gridster-widgets
* Updated german translation
* Updated Icons
* Clean post_metas on post deletion
* Redirect Editor to workbench, if there are no gridster posts to show on /wp-admin/edit.php
 

### 1.0 ###
* Initial release





## Arbitrary section ##


### Filters and Hooks ###
 
You can adjust the behavior of this plugin by using following filters:

* Change the `get_post_types()` call for usable post_types by filtering `gridster_get_post_types_as_widget_blocks_args`
* Change final array of used post_types by modifying `gridster_post_types_as_widget_blocks`
* Filter the list of visible / usable posts per post_type by hooking into `gridster_get_posts_by_type_query_args`
* Adjust the naming convention for used templates by filtering `gridster_locate_templates_from`

Have a look inside the plugin file to see, what variables you are able to use within your filter hooks.



### Translations  ###

* English (en_US)
* German (de_DE)

 

### Many Thanks goes out to ###

* The guys of [Ducksboard](http://ducksboard.com/) and the many github Contributors for their work on [gridster.js](https://github.com/ducksboard/gridster.js)
* [Mika Tuupola](http://www.appelsiini.net/) for his work on [Jeditable](http://www.appelsiini.net/projects/jeditable)
* [Yusuke Kamiyamane](http://p.yusukekamiyamane.com/) for his [Diagona Icons](http://www.iconfinder.com/iconsets/diagona) licensed under [Creative Commons (Attribution 3.0 Unported)](http://creativecommons.org/licenses/by/3.0/)
* [MidTone Design](http://www.midtonedesign.com/portfolio/category/portfolio/) for their [Web Injection Icons)[http://www.iconfinder.com/iconsets/webinjection]
* [Dmitry Costenco](http://www.aha-soft.com/) for his [Free Applications Icons](http://www.iconfinder.com/iconsets/freeapplication)
* [New Moon](http://code.google.com/u/newmooon/) for their [Ultimate Gnome Icons](http://www.iconfinder.com/iconsets/UltimateGnome)

