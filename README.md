The purpose of this file is to provide a set of checks that a theme reviewer can use to perform an early initial review of a theme for the .org repo. The intention is to test as many important items in as short a time as possible.

**NOTE: With an emphasis on speed some of the checks may not be full checks - only overviews.**

Aiming for the goal of performing all of these checks for a pre-review in **_10-20 minutes_**. Ultimately helping to reach an end goal of **_1 hour review time_**, if a theme is well built by the author.

## First Checks

- Screenshot - is it a proper screenshot of a theme?
- footer.php - only 1 footer credit link.
- tags - are all the tags valid .org tags? if tags are in readme do they sync with style.css?
- themes own licence statement - MUST be GPL (not just a compatible licence).

## Activation and run checks

- Does the theme activate without error?
- Does it redirect or display some kind of notice on activation? - no redirects, notices should not be global nags.
- Visit homepage - any error or notice messages from php or JS?
- Visit single page - any error or notice messages from php or JS?
- Make attempts to test all template files provided by the theme - any errors or notices?
- Theme Check Plugin - any errors?
- Theme Sniffs - any errors? Note escaping/translation warnings.
	- note that at a minimum amount of unique escaping/translation warnings __should be verified__ to actually need changed before this would be noted as a failed requirement (_remember that not all warnings shown need escaped at output_).

## Licensing scan through

Does readme indicate any kind of licensing or credits for assets? Quickly scan theme directories for images and any possible code from 3rd parties or libraries/frameworks. All assets including images in the theme and used in the screenshot need noted. Additionally any code, css or libraries used need noted.

A 'code incorporated from' notes may also be required if code is used from another project.

A licence note about the parent theme should be included if theme is a child of another theme.

## Rudimentary security audit

Theme Sniffs do a good job at spotting potential security issues where something is being output to the page (escaping).

It should be checked that themes have no code that is obviously calling home in some way. This includes any tracking prior to explicit user approval. Also `wp_remote_*` and `curl` are 2 functions worth checking for.

Check JavaScript files for any functions that look to be doing something strange. I have see a few attempts to prevent modification of the code and injecting credit links through JS.
