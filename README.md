ZANavi Tests Documentation
==========================

<b>filename:</b>
<pre>
[a-zA-Z0-9_-]*.yaml
</pre>

<b>file specs:</b>
<pre>
all lines beginning with '#' are comments and are ignored by the test routine
each test file can only contain exactly 1 test with 1 success criterion
</pre>

<b>file content:</b>
<pre>
[type: '&lt;searchtype1>'] # optional, if not specified then do a routing test
</pre>


<b>for routing test:</b>
<pre>
from:
  lat: &lt;latitude as float number>
  lng: &lt;longitude as float number>
[  heading: &lt;heading as float number>]
[optional blank lines]
to:
  lat: &lt;latitude as float number>
  lng: &lt;longitude as float number>
[optional blank lines]
success:
    source: '&lt;src1>'
    item: '&lt;item1>'
    value: &lt;expected value as int number OR string value UTF-8>
    operator: '&lt;ops1>'
</pre>



<b>for search test:</b>
<pre>
input:
  street: '&lt;string UTF-8 OR empty>'
  city: '&lt;string UTF-8 OR empty>'
  housenumber: '&lt;string UTF-8 OR empty>'
[optional blank lines]
success:
    item: '&lt;item2>'
    value: &lt;expected value as int number OR string value UTF-8>
    operator: '&lt;ops2>'
</pre>



<b>accepted values for ops1 (only the first 3 are accepted for string values):</b>
<pre>
==
!=
&lt;>
>
&lt;
=>
>=
&lt;=
=&lt;
</pre>

<b>accepted values for ops2 (only the first 4 are accepted for string values):</b>
<pre>
==
!=
&lt;>
like # this is just an exact substring comparsion, NO conversion or REGEX
>
&lt;
=>
>=
&lt;=
=&lt;
</pre>

<b>accepted values for src1:</b>
<pre>
dbus # only with status
gpx # only with nodes, nav&lt;n>
</pre>

<b>accepted values for searchtype1:</b>
<pre>
RT # routing test
NS # normal search test
IS # index search test
</pre>

<b>accepted values for item1:</b>
<pre>
nodes
status
nav&lt;n> # n is the number of the n-th navigation item to be used for the criterion (counting starts from zero!)
</pre>

<b>accepted values for item2:</b>
<pre>
resultcount
result&lt;n> # n is the number of the n-th result item to be used for the criterion (counting starts from zero!)
</pre>

