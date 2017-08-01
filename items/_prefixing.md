### checking for un-prefixed functions

You can check theme prefixed functions with grep. These commands are not ideal but they work well. My local machine had GNU grep with PCRE available but many distros do not have the GNU version. Without reliable PCRE for proper lookaround this is a good alternative.

Run from inside theme directory or swap the `.` to the root directory of theme.

Find all functions in php WITHOUT prefix:

`grep --color=always -PrinHo --include \*.php '(function ).*?{' . | grep -v "prefix_""`

Find all functions in php files WITH prefix:

`grep -PrinHo --include \*.php '(function )(!?prefix_).*?{' .`
