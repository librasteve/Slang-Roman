[![Actions Status](https://github.com/librasteve/Slang-Roman/workflows/test/badge.svg)](https://github.com/librasteve/Slang-Roman/actions)

NAME
====

Slang::Roman - lets you use Roman numerals in your code

SYNOPSIS
========

```raku
use Slang::Roman;

say 0rI + 0rIX; # 10
my $i = 0rMMXVI; # $i = 2016
```

DESCRIPTION
===========

This bit of admittedly twisted code let you use Roman numerals in your Raku code. It patches the running grammar so you can use a Roman numeral anywhere you would use a regular integer.

Future enhancements will include expansions to printf/sprintf with a custom formatting type, and the equivalents of `hex()` to handle string conversion.

While it handles both additive and subtractive Roman numerals, it doesn't check that they're properly formatted. For instance 'IC' should be a compile-time error but instead it'll generate 101 as if nothing of consequence happened.

REFERENCE
=========

According to [Wikipedia](https://en.wikipedia.org/wiki/Roman_numerals), the standard form is:

<table class="pod-table">
<thead><tr>
<th>#</th> <th>Thousands</th> <th>Hundreds</th> <th>Tens</th> <th>Units</th>
</tr></thead>
<tbody>
<tr> <td>1</td> <td>M</td> <td>C</td> <td>X</td> <td>I</td> </tr> <tr> <td>2</td> <td>MM</td> <td>CC</td> <td>XX</td> <td>II</td> </tr> <tr> <td>3</td> <td>MMM</td> <td>CCC</td> <td>XXX</td> <td>III</td> </tr> <tr> <td>4</td> <td></td> <td>CD</td> <td>XL</td> <td>IV</td> </tr> <tr> <td>5</td> <td></td> <td>D</td> <td>L</td> <td>V</td> </tr> <tr> <td>6</td> <td></td> <td>DC</td> <td>LX</td> <td>VI</td> </tr> <tr> <td>7</td> <td></td> <td>DCC</td> <td>LXX</td> <td>VII</td> </tr> <tr> <td>8</td> <td></td> <td>DCCC</td> <td>LXXX</td> <td>VIII</td> </tr> <tr> <td>9</td> <td></td> <td>CM</td> <td>XC</td> <td>IX</td> </tr>
</tbody>
</table>

[Slurpy](https://docs.raku.org/language/signatures#Slurpy_parameters) `*@array` `if not @array`

    Required  C<$foo> 

    Optional C<@bar = default>

default A suitable default is an Object that has a distinct identity, as may be checked by the [`WHICH`](https://docs.raku.org/type/Mu#method_WHICH) method.

`if @bar === default {...}`

<table class="pod-table">
<thead><tr>
<th>Parameter kind</th> <th>Example</th> <th>Comment</th> <th>Check for no arg passed</th>
</tr></thead>
<tbody>
<tr> <td>Required</td> <td>C&lt;$foo&gt;</td> <td>Can&#39;t be omitted</td> <td>(not applicable)</td> </tr>
</tbody>
</table>

<table class="pod-table">
<thead><tr>
<th>Parameter kind</th> <th>Example</th> <th>Comment</th> <th>Check for no arg passed</th>
</tr></thead>
<tbody>
<tr> <td>L&lt;Slurpy|https://docs.raku.org/language/signatures#Slurpy_parameters&gt;</td> <td>C&lt;*@array&gt;</td> <td>Don&#39;t check using C&lt;.defined&gt;</td> <td>C&lt;if not @array&gt;</td> </tr> <tr> <td>Required</td> <td>C&lt;$foo&gt;</td> <td>Can&#39;t be omitted</td> <td>(not applicable)</td> </tr> <tr> <td>Optional</td> <td>C&lt;@bar = default&gt;</td> <td>Pick, and check, a suitable default N&lt;A suitable default is an Object that has a distinct identity,</td> <td></td> </tr> <tr> <td>as may be checked by the L&lt;C&lt;WHICH&gt;|https://docs.raku.org/type/Mu#method_WHICH&gt; method.&gt;</td> <td>C&lt;if @bar === default {...}&gt;</td> <td></td> <td></td> </tr>
</tbody>
</table>

The numerals for 4 (IV) and 9 (IX) are written using subtractive notation,where the smaller symbol (I) is subtracted from the larger one (V, or X), thus avoiding the clumsier IIII and VIIII. Subtractive notation is also used for 40 (XL), 90 (XC), 400 (CD) and 900 (CM). These are the only subtractive forms in standard use.

AUTHOR
======

Jeff Goff (DrForr)

Source can be located at: https://github.com/raku-community-modules/Slang-Roman . Comments and Pull Requests are welcome.

COPYRIGHT AND LICENSE
=====================

Copyright 2016, 2018 Jeff Goff, 2020-2023 Raku Community

This library is free software; you can redistribute it and/or modify it under the Artistic License 2.0.

