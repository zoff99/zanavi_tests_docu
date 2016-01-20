ZANavi Tests Documentation
==========================

<b>filename:</b> [a-zA-Z0-9][_-].yaml

<b>file specs:</b>

all lines beginning with '#' are comments and are ignored by the test routine
each test file can only contain exactly 1 test with 1 success criterion

<b>file content:</b>

[type:S] -> optional to specify a "search" test, otherwise it's a routing test

<b>for routing test:</b>

from:
  lat: <latitude as float number>
  lng: <longitude as float number>
[  heading: <heading as float number>]
[optional blank lines]
to:
  lat: <latitude as float number>
  lng: <longitude as float number>
[optional blank lines]
success:
    source: '<src1>' # currently ignored
    item: '<item1>'
    value: <expected value as int number OR string value>
    operator: '<ops1>'



<b>for search test:</b>



<b>accepted values for ops1 (only the first 3 are accepted for string values):</b>
==
!=
<>
>
<
=>
>=
<=
=<

<b>accepted values for src1:</b>
dbus # only with status
gpx # only with nodes, nav<n>

<b>accepted values for item1:</b>
nodes
status
nav<n> # n is the number of the n-th navigation item to be used for the criterion

