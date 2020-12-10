# Slickslider Slides same height.

Normally you would just set the slicktrack as a flex box with justify content stretch. But this breaks the slickslider on IE11.

This Scripts does sets the Height of the Slides to tallest slide:

```
$(window).load(function() {
      $('.slides').on('setPosition', function () {
      $(this).find('.slick-slide').height('auto');
      var slickTrack = $(this).find('.slick-track');
      var slickTrackHeight = $(slickTrack).height();
      $(this).find('.slick-slide').css('height', slickTrackHeight + 'px');
      });
})
```
