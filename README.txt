Main plugins used:
Jetpack
The Events Calendar
Wp Facebook Share Like Button

﻿Theme inherits from rebalance theme. All changes in anywhere are commented by "mmmnmnm" and "mmn".

1. Changes that should not be affected by updates
 - Can be found under /wp-content/themes/rebalance-child-mmn

2. Changes that need to be re-added after theme (rebalance) update
- /wp-content/themes/rebalance/js/navigation.js (line 14): column number changed from 3 to 4 -> effect: "English content" menu shows under main manu

3. Changes that need to be re-added after Wordpress update:
-	/wp-includes/functions.php (line 106) and corresponding definition of myucfirst() function -> effect: first letter of months uppercased

4. Changes that need to re-added after Wp Facebook Share Like Button plugin change:
- wp-content/plugins/wp-fb-share-like-button/wp-fb-share-like-button.php (line 185): delete writing og:url tag:
//echo '<meta property="og:url" content="' . get_permalink() . '" />' . "\n";

Other notes:
- (Sept 1st, 2018) Changes done to restore Facebook like after HTTP -> HTTPS change (https://cognitiveseo.com/blog/13431/recover-facebook-shares-https/):
  1. (Child theme's functions.php) Change canonical for old posts (custom header action)
  2. (Child theme's functions.php) Change og:url for old posts (custom jetpack action)
  3. (See above item nr. 5) Comment out like button code for canonical (add to README) -> sajn nem konfiguralhato
  4. (See file) Add crawler exclusion to .htaccess
- Site description is currently disabled and is replaced by constant donate info (site descr. is still visible on the browser tab)
- Font does not render on some machines: SOLVED https://stackoverflow.com/questions/45715928/solved-rubik-font-not-rendering-anymore
- Default event times are altered to start11pm and to end 5am: custom tribe_events_meta_box_timepicker_default filter

TODOs:
- Display multiple category page title when multiple categories are displayed, e.g., mmmnmnm.com/category/review,interview
  - Hint: /themes/archive.php -> page title
