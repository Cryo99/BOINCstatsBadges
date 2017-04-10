# BOINCstatsBadges

### Description
This script adds a new tab containing badge statistics for projects that award badges to your [BOINCstats.com][1] statistics page. Enter your BOINC project user IDs into the configuration dialogue which can be accessed from GreaseMonkey's "User Script Commands" menu. The script will then retrieve your badge statistics and display them.

It works with all of the thirteen languages available on the site. The basic layout is localized but anyone who would like to assist with corrections or the remaining language strings for the configuration dialogue is welcome to contact me.

Version 2 includes a substantial internal reorganization that provides more robust error checking and attempts to wait for the AJAX calls to complete and the new tab to be rendered before trying to render the badges. Configuration now includes the ability to tweak the timings so you are able to adjust them to suit faster or slower networks, software, systems, etc.

The AJAX timeout determines how long the script will wait while retrieving each project's stats. The stats are retrieved asynchronously and in parallel, so times are per project, not cumulative.

The tab load delay determines how long the script will wait to try and make sure that the tab has rendered and is ready before rendering the badges. This delay occurs after the stats have been retrieved or the attempt has timed out and so the cumulative total is the worst case delay for each project.

You can try increasing these values if you find that the badges aren't appearing or you receive the connection error message.

You can find your stats on BOINCstats by going to your member page for any BOINC project and clicking the "BOINCstats" link next to "Cross-project statistics" in the "Computing and credit" section, by visiting [BOINCstats.com][1], entering your BOINC user name into the search box at top left and hitting return or by browsing to one of these URLs:

http&#58;//boincstats\.com/en/stats/-1/user/detail/**userid**/  
http&#58;//boincstats\.com/en/stats/-1/user/detail/**cpid**/

where **userid** is your BOINCstats user ID and **cpid** is your cross-project ID, also available from any BOINC project member page in "Cross-project statistics".

[1]: https://boincstats.com/

### History

#### V 3.0.1
* Fixed row highlighting.
* Added Amicable Numbers.

#### V 3.0.0
* Fixed new Collatz rank badges.
* Added Atlas@home
* Added Citizen Science Grid
* Added DENIS@Home
* Added GoofyxGrid@Home
* Added SRBase
* Added TN-Grid
* Added Universe@Home
* Retired Convector, OProject and Wildlife.
* Made icon sizes more consistent across projects.
* Updated PrimeGrid icon tooltips.
* Updated WUProp to support multiple badges.
* Changed to better versioning.
* Fixed NumberFields to work with the new site layout.


#### V 2.11
* Improved tooltips for PrimeGrid projects.
* Reduced default delay values to zero as they shouldn't really be needed now.

#### V 2.1
* Added Milkway@Home.
* Added NFS@Home.
* Added theSkyNet POGS.
* Added Odd Weird Search to Yoyo@home.
* Added % RAC to Collatz Conjecture.
* Fixed breakage caused by GM 2.0 update security changes.
* Fixed Wildlife@Home breakage after image src format change.
* Fixed issue with badges not loading if the HTML wasn't already displayed.
* Fixed a bug in delay prefs.

#### V 2.01
* Fixed a bug in delay prefs.

#### V 2.0
* Enabled Collatz Conjecture.
* Added Wildlife@Home.
* Changed things so that badges graphics are loaded after the AJAX call returns, to prevent them not rendering if the tab is selected before the HTML finishes rendering.
* Added failure to connect message.
* Added delay configuration.
* Updated the configuration dialogue to match the site.

#### V 1.07
* Added Collatz Conjecture but left it disabled until the server is back up.
* Added default GPUGrid badge for no publications.

#### V 1.06
* Added WUProp.
* Fixed an error with GPUGrid tooltips.

#### V 1.05
* Added NumberFields and Radioactive.
* Improved error handling.

#### V 1.04
* Updater tweak.

#### V 1.03
* Tried another updater.

#### V 1.02
* Removed the updater as it's dead. :-(

#### V 1.01
* Added updater.
* Added icon.

#### V 1.0
* Initial release
