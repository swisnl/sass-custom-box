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

## SWIS

[SWIS][link-swis] is a web agency from Leiden, the Netherlands. We love working with open source software. 

[ico-travis]: https://travis-ci.org/swisnl/sass-custom-box.svg?branch=master
[ico-swis]: https://img.shields.io/badge/%F0%9F%9A%80-made%20by%20SWIS-%23D9021B.svg

[link-travis]: https://travis-ci.org/swisnl/sass-custom-box
[link-author]: https://github.com/RoachMech
[link-contributors]: ../../contributors
[link-swis]: https://www.swis.nl
