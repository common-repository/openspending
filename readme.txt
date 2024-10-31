=== OpenSpending ===
Author URI: http://community.openspending.org/
Plugin URI: https://github.com/openspending/openspending-wordpress-plugin/
Contributors: tryggvi
Donate link: http://okfn.org/support/
Tags: openspending, visualisation, budget, spending, data, open data, open knowledge, government, analysis
Requires at least: 3.0.1
Tested up to: 3.8
Stable tag: 0.5.1
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Create beautiful visualisations with data on OpenSpending.org using a simple, elegant user interface made available in the WordPress editor.

== Description ==

The [OpenSpending community project](http://openspending.org/) aims to build and use open source tools and datasets to gather and analyse the financial transactions of governments around the world.

Only by understanding the financial transactions that are made in their name can citizens hope to hold government to account, and begin to effect positive change they wish to see in the world.

The OpenSpending WordPress plugin provides an easy-to-use visualisation creator for financial data hosted on [OpenSpending.org](http://openspending.org). Emphasis is on making the interface more user friendly than configurable. 

Via a simple popup, users fill in necessary details of the dataset they want to visualise. This creates a shortcode that can be placed on pages or in blog posts to render beautiful, interactive, tried and tested visualisations which OpenSpending is known for.

== Installation ==

To install the OpenSpending WordPress plugin follow these steps:

1. Extract the zip file and put the included openspending directory into the `/wp-content/plugins/` directory
1. Activate the plugin through the 'Plugins' menu in WordPress
1. The visualisation wizard should now be available in the WordPress editor

== Frequently Asked Questions ==

= Can I change the default configurations? =

The WordPress plugin focuses more on simplicity of use than feature completeness. If you are interested in more configurations, please consider using the [OpenSpending visualisation library](https://github.com/openspending/openspendingjs) directly (the plugin creates a clean user interface on top of that library). 

= The bubbletree visualisation doesn't work =

Unfortunately, in the current implementation of the bubbletree visualisation there are a few errors. One is the assumption that it is impossible to drill down (click on) bubbles with only a single child (irrespective of if that child has more children). Another is the assumption that all children will have at least two other sibling bubbles. The third, and possibly the biggest problem is that because the bubbletree works via the URL more than one bubbletree per page is not possible.

= How do I get the cool OpenSpending icons? =

For both the bubbletree and the bar charts, the OpenSpending icons are automatically loaded for dimensions defining COFOG classifications. Simply choose the COFOG dimensions as the drilldowns.

= Can I create time series? =

Yes! You could for example use the bar chart and just choose your time dimension. Note that this will write out the full date. If you want to for example only show the time as the year, you would have to change the drilldown dimension in the generated shortcode from *time* to *year*.

= Aren't the historical amounts wrong because of inflation? =

Not necessarily. The plugin tries to do automatic inflation adjustment based on consumer price index data available for last year. If it cannot find the needed data then it doesn't do the adjustments and falls back to historical values.

== Screenshots ==

1. Simple, elegant user interface to create visualisations
2. Treemap visualisation
3. Bubbletree visualisation
4. Bar chart visualisation

== Changelog ==

= 0.5.1 =
* Initial release onto the WordPress plugin repository 
* Treemap visualisation
* Bubbletree visualisation
* Bar chart visualisation
* Automatic inflation adjustment if possible
* Automatic icons and colors for COFOG dimensions
