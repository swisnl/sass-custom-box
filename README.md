# sass-custom-box
[![Build Status][ico-travis]][link-travis]
[![Made by SWIS][ico-swis]][link-swis]

BEM-compatible SASS mixins for styling radioboxes and checkboxes

## Install

Via NPM:

``` bash
$ npm i sass-custom-box
```

## Usage

### For checkboxes:

HTML:

``` html
<div class="my-checkbox">
    <input type="checkbox" id="my_checkbox" name="checkbox_field" class="my-checkbox__input"/>
    <label for="my_checkbox" class="my-checkbox__label">Label</label>
</div>
```

SCSS:

``` scss
@include custom-box(my-checkbox) {
    @include custom-box-input();
    @include custom-box-label();
};
```

### For radioboxes:

HTML:

``` html
<div class="my-radiobox">
    <input type="radio" id="my_radiobox1" name="radiobox_field" class="my-radiobox__input"/>
    <label for="my_radiobox1" class="my-radiobox__label">Label</label>
</div>
<div class="my-radiobox">
    <input type="radio" id="my_radiobox2" name="radiobox_field" class="my-radiobox__input"/>
    <label for="my_radiobox2" class="my-radiobox__label">Label</label>
</div>
```

SCSS:

``` scss
@include custom-box(my-radiobox, radiobox) {
    @include custom-box-input();
    @include custom-box-label();
};
```

### Customization

This library comes with a predefined theme. To customize (parts of) this theme pass a scss map to the `set-custom-box-theme()` mixin as follows:

``` scss
$my-theme: (
    container: (
        background-color: red,
        border: 1px solid black    
    )
);

@include set-custom-box-theme($my-theme);
```

Below is the scss map which contains the default theme. Each of these items can be customized using the `set-custom-box-theme()` mixin.

``` scss
// default theme

(
    container: (
        _checked: (
            background-color: #b3e5fc,
            border: 1px solid #01579b
        ),
        _focus: (
            box-shadow: 0 0 5px #01579b
        ),
        background-color: #b3e5fc,
        border: 1px solid #01579b,
        border-radius: .25rem,
        height: 1.25rem,
        margin: 0 .5rem 0 0,
        transition: all .1s ease-in-out,
        width: 1.25rem
    ),
    tick: (
        background-color: #01579b,
        transition: all .1s ease-in-out
    )
)
```

#### Customize checkbox styling

In order to change checkbox specific styling pass an scss map with your desired items to the `set-custom-box-checkbox-theme()` mixin. 
You can override any of the default checkbox items, the default checkbox theme is the default theme as shown above appended with the following scss map:

``` scss
// default checkbox theme, appended to the default theme

(
    tick: (
        border-width: .2em,
        height: .6em,
        left: .075em,
        top: .2em,
        width: .4em
    )
)
```

#### Customize radiobox styling

In order to change radiospecific styling pass an scss map with your desired items to the `set-custom-box-radiobox-theme()` mixin. 
You can override any of the default radiobox items, the default radiobox theme is the default theme as shown above appended with the following scss map:

``` scss
// default radiobox theme, appended to the default theme

(
    container: (
        border-radius: 50%,
    ),
    tick: (
        border-radius: 50%,
        height: .75rem,
        left: .25rem,
        top: .25rem,
        width: .75rem
    )
)
```

## Change log

Please see [CHANGELOG](CHANGELOG.md) for more information on what has changed recently.

## Testing

``` bash
$ npm run test
```

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) and [CODE_OF_CONDUCT](CODE_OF_CONDUCT.md) for details.

## Security

If you discover any security related issues, please email security@swis.nl instead of using the issue tracker.

## Credits

- [RoachMech][link-author]
- [All Contributors][link-contributors]

## License

The MIT License (MIT). Please see [License File](LICENSE) for more information.

## SWIS :heart: Open Source

[SWIS][link-swis] is a web agency from Leiden, the Netherlands. We love working with open source software. 

[ico-travis]: https://travis-ci.org/swisnl/sass-custom-box.svg?branch=master
[ico-swis]: https://img.shields.io/badge/%F0%9F%9A%80-made%20by%20SWIS-%23D9021B.svg

[link-travis]: https://travis-ci.org/swisnl/sass-custom-box
[link-author]: https://github.com/RoachMech
[link-contributors]: ../../contributors
[link-swis]: https://www.swis.nl
