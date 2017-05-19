<p align="center">
  <img src="https://s1.postimg.org/nimmn9kf3/vanillafilter.png" alt="vanillafilter" width="250" height="250" />
</p>

___

# vanillafilter
[![GitHub release](https://img.shields.io/github/release/dverleg/vanillafilter.svg)](https://github.com/dverleg/vanillafilter)
[![Travis](https://img.shields.io/travis/dverleg/vanillafilter.svg)](https://travis-ci.org/dverleg/vanillafilter)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/dverleg/vanillafilter/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/dverleg/vanillafilter/?branch=master)
[![Scrutinizer Code Coverage](https://scrutinizer-ci.com/g/dverleg/vanillafilter/badges/coverage.png?b=master)](https://scrutinizer-ci.com/g/dverleg/vanillafilter/?branch=master)
[![npm](https://img.shields.io/npm/dm/vanillafilter.svg)](https://www.npmjs.com/package/vanillafilter)

[Intro](#intro)<br>
[Usage](#usage)<br>
[Options](#options)

### Intro
VanillaJS library to bind filtering to any element of your choice. Specify the filter trigger and targets (or use the defaults) and let vanillafilter do its' magic.

:leaves: Extremely lightweight <br>
> ~1kb minified <br>
> ~500bytes gzipped

:tada: VanillaJS - no jQuery required

:zap: Lightning fast

<br><br>

### Usage
1. Install vanillafilter dependency and import it into one of your modules / scripts
```
$ yarn add vanillafilter
```

OR

Download and include the ./dist/js/vanillafilter.min.js script directly in your HTML
```javascript
<script type="text/javascript" src="[scripts-folder]/vanillafilter.min.js"></script>
```

2. Setup your HTML structure for filtering, for example:
```html
<select data-vanillatrigger>
  <option value="">Select filter</option>
  <option value="even">Even</option>
  <option value="odd">Odd</option>
</select>

<ul>
  <li data-vanillatarget="odd">First.</li>
  <li data-vanillatarget="even">Second.</li>
  <li data-vanillatarget="odd">Third.</li>
  <li data-vanillatarget="even">Fourth.</li>
</ul>
```

3. Instantiate vanillafilter
```js
<script>
  var VanillaFilter = new VanillaFilter();
</script>
```

4. That's it!

<br><br>

### Options
vanillafilter comes with a set of options for customization. The options can be set as follows:
```js
  var VanillaFilter = new VanillaFilter({
    vanillaTrigger: 'triggerDataAttribute',
    vanillaTarget: 'targetsDataAttribute',
    vanillaDisplayType: 'wantedDisplayType',
  });
```

#### vanillaTrigger
The data-attribute selector of the element(s) that should trigger the filtering, for example a select dropdown or a div.
> default: vanillatrigger <br>
> Which selects all [data-vanillatrigger] elements
```html
<select data-vanillatrigger></select>
```

> If you use a div, span or any 'clickable' element as trigger, you have to define the trigger value in the data-vanillatrigger attribute. For example:
```html
<span data-vanillatrigger="odd">Odd</span>
<span data-vanillatrigger="even">Even</span>
```

#### vanillaTarget
The data-attribute selector of the elements that you want to target for filtering, this can be any element.
> default: vanillatarget <br>
> Which selects all [data-vanillatarget] elements
```html
<ul>
  <li data-vanillatarget="filtervalue"></li>
</ul>
```

#### vanillaDisplayType
The CSS 'display' you wish to give the target elements once they're filtered (and shown).
> default: block
```css
display: block;
```
