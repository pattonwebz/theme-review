### checking for un-prefixed functions

#### REGEX:

Loose regex match for all functions in theme. This will still match functions indide of classess or namespaces.

`function .*?\(.*?\).?{`

#### GREP:

Run from inside theme directory or swap the `.` to the root directory of theme.

Find all functions in php WITHOUT prefix:

`grep --color=always -PrinHo --include \*.php '(function ).*?{' . | grep -v "prefix_""`

Find all functions in php files WITH prefix:

`grep -PrinHo --include \*.php '(function )(!?prefix_).*?{' .`
