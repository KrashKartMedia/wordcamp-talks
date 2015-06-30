# WordCamp Talks
A plugin that displays your WordCamp Talks on your WordPress Blog.

## Installation - WordPress Dashboard
1. Download plugin
2. Log into your WordPress Site
3. Visit Plugins > Add New > Upload Plugin > Choose File
4. Locate the plugin .zip file
5. Select .Zip file
6. Click Install Now
7. Activate WordCamp Talks Plugin

## Installation - FTP Client
1. Download plugin
2. Unzip (Extract) plugin .zip file to folder location of your choice
3. Open ftp client & connect to your WordPress Site
4. Locate folder that the plugin resides in
5. Upload Plugin folder to wp-content/plugins directory
6. Log into to WordPress Dashboard
7. Visit Plugins > Installed Plugins
8. Activate WordCamp Talks Plugin

##Shortcodes
[wordcamp=talks] //put this on a page to display all WordCamp Talks
<br>
[wc-presentation-url] //links to the presentation url<br>
[wc-talk-video] //links to the presentation video<br>
[wc-talk-url] //links to the session description<br>

## Hooks & Filters
This plugin has several actions (hooks and filters) that you can remove if you wish. 

1. add_action( 'init', 'create_wordcamp_talks_taxonomies', 0 ); //creates taxonomy called wordcamp-cities<br>
2. add_action( 'init', 'create_wordcamp_year_taxonomies', 0 ); //creates taxonomy called wordcamp-years<br>
3. add_shortcode('wc-presentation-url', 'get_custom_field_wc_talk_year'); //creates shortcode [wc-presentation-url]<br>
4. add_shortcode('wc-talk-video', 'get_custom_field_wc_talk_video'); //creates shortcode [wc-talk-video]<br>
5. add_shortcode('wc-talk-url', 'get_custom_field_wc_talk_url'); //creates shortcode [wc-talk-url]<br>
6. add_shortcode('wordcamp-talks', 'get_cpt_wc_talks'); //creates shortcode [wordcamp-talks]<br>
7. add_filter( 'the_content', 'wc_links_after_content' ); // adds metabox info after the content on a single post<br>
8. add_filter( 'the_content', 'wc_links_after_content_cpt_archive' ); //adds metabox info after the content on archive <br>
