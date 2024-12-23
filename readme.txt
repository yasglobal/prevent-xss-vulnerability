=== Prevent XSS Vulnerability ===
Contributors: sasiddiqui
Tags: attack, cross-site scripting, security, vulnerability, xss
Requires at least: 3.5
Tested up to: 6.7
Stable tag: 2.0.2
License: GPLv3
License URI: https://www.gnu.org/licenses/gpl-3.0.html

This WordPress plugin enhances website security by preventing Cross-Site Scripting (XSS) vulnerabilities. It blocks and encodes malicious characters in URLs, escapes HTML in `$_GET` variables, and provides customizable settings for website owners.

== Description ==

This plugin helps safeguard your website against two common types of Cross-Site Scripting (XSS) vulnerabilities:

* **Reflected XSS:** In Reflected XSS, malicious scripts are injected into the URL of a website. When a user clicks on a link containing this malicious script, it can be executed on their browser, potentially stealing their information or compromising their system.
* **Self-XSS:** This occurs when a user's own input on the website is reflected back to them in an insecure manner, allowing malicious scripts to be executed in their browser.

This plugin provides several layers of protection:

**Blocking:** When enabled, the plugin scans URLs for specific parameters. If any of the listed parameters are found in the URL, the plugin redirects the user to prevent potential XSS attacks. You can customize the list by excluding specific parameters you still want to allow.

* Opening Round Bracket `(`
* Closing Round Bracket `)`
* Less than Sign `<`
* Greater than Sign `>`
* Opening Square Bracket `[`
* Closing Square Bracket `]`
* Opening Curly Bracket `{`
* Pipe or Vertical Bar `|`
* Closing Curly Bracket `}`

**Encoding:** For additional security, the plugin encodes certain characters within the URL parameters. This prevents malicious code from being executed even if it's included in the URL. You can also exclude specific parameters from being encoded.

* Exclamation Mark `!`
* Double Quotation `"`
* Single Quotation `'`
* Opening Round Bracket `(`
* Closing Round Bracket `)`
* Asterisk Sign `*`
* Less than Sign `<`
* Greater than Sign `>`
* Grave Accent <code>`</code>
* Cap Sign `^`
* Opening Square Bracket `[`
* Closing Square Bracket `]`
* Opening Curly Bracket `{`
* Pipe or Vertical Bar `|`
* Closing Curly Bracket `}`

**Escaping HTML in `$_GET`:** This plugin automatically escapes HTML characters within the `$_GET` variable. This is crucial if your website retrieves data from URLs and displays it in the HTML content. This helps prevent malicious scripts from being injected through user-controlled input.

=== Important Notes: ===

* After activating the plugin, thoroughly test your website forms, especially if you use WooCommerce. Ensure the plugin doesn't disrupt your cart and checkout processes.
* Bug reports for this plugin are welcome on GitHub: [https://github.com/samiahmedsiddiqui/prevent-xss-vulnerability/issues](). Please note that GitHub is not a support forum, and only genuine bug reports will be addressed.

By implementing this plugin and following the recommendations, you can significantly enhance your website's security against XSS attacks.

== Installation ==

This process defines you the steps to follow either you are installing through WordPress or Manually from FTP.

**From within WordPress**

1. Visit 'Plugins > Add New'
2. Search for Prevent XSS Vulnerability
3. Activate Prevent XSS Vulnerability from your Plugins page.
4. Go to "after activation" below.

**Manually**

1. Upload the `prevent-xss-vulnerability` folder to the `/wp-content/plugins/` directory
2. Activate Prevent XSS Vulnerability through the 'Plugins' menu in WordPress
3. Go to "after activation" below.

**After activation**

1. Navigate to the `Prevent XSS Vulnerability` page from the Admin Dashboard
2. Make the changes as per your site functionality
3. You're done!

== Screenshots ==

* It removes the parameters from the URL which are used in XSS Attack and redirects the user (Recommended).

* It encodes the parameters from the URL which are used in XSS Attack.

* It escapes the HTML from the `$_GET` PHP variable which is mostly used to read the data from the URL (Recommended).

* Add the message in developer console for the user to alert about the XSS attack.

* Show message in developer console to alert user about the Self-XSS attack. This message can be customized from the settings page.

== Frequently Asked Questions ==

= Q. Why should I install this plugin? =

A. Installing this plugin is the easiest way to protect your site from XSS Vulnerabilities.

= Q. Does this plugin escape HTML in printing search? =

A. Yes, this plugin escapes HTML in `$_GET` variable, which is commonly used to print data from the URL to HTML. However, if your site relies heavily on `$_GET` for other purposes, you may need to conduct thorough testing to ensure compatibility.

= Q. Does this plugin have any conflict with any other plugin? =

A. While no major conflicts have been reported, it's always a good practice to test your website thoroughly after installing any new plugin.

== Changelog ==

= 2.0.2 - Dec 23, 24 =

Fix minor WPCS issues and change text for better understanding.

= 2.0.1 - Aug 19, 22 =

  * Bug
    * [Please fix Notices for use in WP_DEBUG mode](https://wordpress.org/support/topic/please-fix-notices-for-use-in-wp_debug-mode/)

= Earlier versions =

  * For the changelog of earlier versions, please refer to the separate changelog.txt file.
