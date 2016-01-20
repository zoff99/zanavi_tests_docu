ZANavi Tests Documentation
==========================

<b>filename:</b>
<pre>
[a-zA-Z0-9][_-].yaml
</pre>

<b>file specs:</b>
<pre>
all lines beginning with '#' are comments and are ignored by the test routine
each test file can only contain exactly 1 test with 1 success criterion
</pre>

<b>file content:</b>
<pre>
[type:S] -> optional to specify a "search" test, otherwise it's a routing test
</pre>


<b>for routing test:</b>
<pre>
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
</pre>



<b>for search test:</b>
<pre>
</pre>



<b>accepted values for ops1 (only the first 3 are accepted for string values):</b>
<pre>
==
!=
<>
>
<
=>
>=
<=
=<
</pre>

<b>accepted values for src1:</b>
<pre>
dbus # only with status
gpx # only with nodes, nav<n>
</pre>

<b>accepted values for item1:</b>
<pre>
nodes
status
nav<n> # n is the number of the n-th navigation item to be used for the criterion
</pre>

