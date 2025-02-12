## class Length

Data type, represents length and percent units as they used in CSS.

JavaScript in Sciter is extended to support length literals, so these are valid declarations:

```JS
const width = 12px;
const fontSize = 10pt;
```

Length literals are JS numbers immediately follwoed by unit charactes.

List of supported units, standard CSS units: 

* `px` 
* `pt`
* `em`
* `ch`
* `rem`
* `ex`
* `in`
* `cm`
* `mm`
* `pc`
* `vw`
* `vh`
* `vmin`
* `vmax`
* `pct`

Sciter specific units 

* `ppx` - physical pixels, always integer number.
* `dip` - device independent pixel (1/96 of inch(n):length` `px` and `dip` are equivalents in default Sciter configuration. 
* `fx` - Sciter's flex units. `style.width = 1fx` in script is equivalent to `width:1*` (or just `width:*`) in CSS.

### properties:

* `length.quantity:number`

reports number of units in the length. For `12px` it will return `12`.

* `length.units:string`

reports unit name. For `12px` it will return `"px"`.

### methods:

* `length.valueOf():number`

returns number of pixels.

* `length.toString():number`

returns string representation.

* `length.add(length):length`

sum of two lengths. Lengths can be of different units, this:

```const sum = 12px.add(24pt);```

is legal, result will be in `px` units.

* `length.sub(length):length`

subtraction of two lengths. Lengths can be of different units.

* `length.mul(number):length`

multiplies the length by number.

* `length.div(number):length`

divides the length by number.

### static methods:

 * `Length.px(n):length`
 * `Length.em(n):length`
 * `Length.ex(n):length`
 * `Length.pct(n):length`
 * `Length.fx(n):length`
 * `Length.in(n):length`
 * `Length.cm(n):length`
 * `Length.mm(n):length`
 * `Length.pt(n):length`
 * `Length.pc(n):length`
 * `Length.dip(n):length`
 * `Length.percentOfWidth(n):length`
 * `Length.percentOfHeight(n):length`
 * `Length.vw(n):length`
 * `Length.vh(n):length`
 * `Length.vmin(n):length`
 * `Length.vmax(n):length`
 * `Length.rem(n):length`
 * `Length.ppx(n):length`
 * `Length.ch(n):length`

 These above are static constructors of length values.