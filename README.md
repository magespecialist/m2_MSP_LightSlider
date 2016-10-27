# Magento 2 LightGallery module

This module lets you use [lightSlider](https://github.com/sachinchoolur/lightslider) with Magento 2 throught requirejs.

## Installation
```
composer require msp/lightSlider
bin/magento module:enable MSP_LightSlider
bin/magento setup:upgrade
```
## Usage
You must include the css via layout XML, for example if you want to use the gallery in the product page add to ```catalog_product_view.xml```:

    <head>
        ...
        <css src="MSP_LightSlider::css/lightslider.min.css"/>
        ...
    </head>

You can init the gallery with `data-mage-init`:

```
<div id="your-slider" data-mage-init='{
    "LightSlider": {
        "item": 1
    }
}'>
    <a href="img/kitten1.jpg">
        <img src="img/kitten1-thumb.jpg" />
    </a>
    <a href="img/kitten2.jpg">
        <img src="img/kitten2-thumb.jpg" />
    </a>
    <a href="img/kitten3.jpg">
        <img src="img/kitten3-thumb.jpg" />
    </a>
</div>
```

or with a `<script type="text/x-magento-init">`:

```
<div id="your-gallery">
    <a href="img/kitten1.jpg">
        <img src="img/kitten1-thumb.jpg" />
    </a>
    <a href="img/kitten2.jpg">
        <img src="img/kitten2-thumb.jpg" />
    </a>
    <a href="img/kitten3.jpg">
        <img src="img/kitten3-thumb.jpg" />
    </a>
</div>
<script type="text/x-magento-init">
     {
         "#your-slider": {
             "LightSlider": {
                 "item": 1
             }
         }
     }
</script>
```
