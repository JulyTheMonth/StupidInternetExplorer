# Object-Fit

The css attribute object-fit is not supported by internet explorer.

Following script changes all images to div with background image with background-size cover.

```
 if (document.documentMode || /Edge/.test(navigator.userAgent)) {
        jQuery('.StartbildschirmSlider img').each(function(){
            var t = jQuery(this),
                s = 'url(' + t.attr('src') + ')',
                p = t.parent(),
                d = jQuery('<div></div>');

            p.append(d);
            d.css({
                'height'                : t.parent().css('height'),
                'background-size'       : 'cover',
                'background-repeat'     : 'no-repeat',
                'background-position'   : '50% 20%',
                'background-image'      : s,
                'width'                 : "100%"
            });
            t.hide();
        });
    }
```
