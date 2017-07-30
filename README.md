The purpose of this file is to provide a set of checks that a theme reviewer can use to perform an early initial review of a theme for the .org repo. The intention is to test as many important items in as short a time as possible.

NOTE: With an emphasis on speed some of the checks may not be full checks - only overviews.

Aiming for the goal of performing all of these checks for a pre-review in 10-20 minutes. Ultimately helping to reach an end goal of 1 hour review time should themes be well built by the author.

== First Checks ==

- Screenshot - is it a proper screenshot of a theme?
- footer.php - only 1 footer credit link.
- tags - are all the tags valid .org tags? if tags are in readme do they sync with style.css?
- themes own licence statement - MUST be GPL (not just a compatible licence).

== Activation and run checks ==

- does the theme activate without error?
- does it redirect or display some kind of notice on activation? - no redirects, notices should not be global nags.
- visit homepage - any error messages from php or JS?
- visit single page - any error messages from php or JS?
- if you have time test any custom pages and other templates such as author.php or archive.php
- Theme Check Plugin - any errors?
- Theme Sniffs - any errors? Note escaping/translation warnings.
	- note that at a minimum amount of unique escaping/translation warnings should be verified to actually need changed before this would be noted as a failed requirement (remember that not all warnings do need escaping at output).

== Licensing scan through ==

Does readme indicate any kind of licensing or credits for assets? Quickly scan theme directories for images and any possible code from 3rd parties or libraries/frameworks. All assets including images in the theme and used in the screenshot need noted. Additionally any code, css or libraries used need noted.

== Rudimentary security audit ==

Theme Sniffs do a good job at spotting potential security issues where something is being output to the page. Additionally it should be checked that themes have no other code that is obviously calling home in some way.
