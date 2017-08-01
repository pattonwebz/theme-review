==== checking prefixed functions ====

You can check theme prefixed functions with grep. This is not the ideal way but it's one way to do it:

Find all functions in php WITHOUT prefix:

`grep -PrinHo --include \*.php '(function ).*?{' . | grep -v "prefix_""`

Run from inside theme directory or swap the `.` to the root directory of theme.

Find all functions in php files WITH prefix:

`grep -PrinHo --include \*.php '(function )(!?prefix_).*?{' .`
