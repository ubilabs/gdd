
!SLIDE bullets

# Static Maps #

* No JavaScript
* Single IMG tag
* Fast as hell


!SLIDE

    @@@html
    <img 
      src="path_to_image"
      width="512"
      height="512"
    />

!SLIDE

## Styled Static Maps ##

    @@@sh
    http://maps.google.com/maps/api/staticmap?
    sensor=false&size=512x512&center=Hamburg&zoom=12

!SLIDE center

![Staticmap](staticmap.png)

!SLIDE

## Styled Static Maps ##

    @@@sh
    http://maps.google.com/maps/api/staticmap?
      sensor=false
      &size=512x512
      &center=Hamburg
      &zoom=12
      &style=
        feature:all|
        element:geometry|
        saturation:-100
      &style=
        ...


!SLIDE center
![Staticmap](staticmap.png)

!SLIDE center
![Staticstyle](staticstyle.png)

!SLIDE

## Custom Markers ##

    @@@sh
    http://maps.google.com/maps/api/staticmap?
      sensor=false
      &size=512x512
      &markers=
        icon:http://my_domain.com/marker.png|
        Hamburg

!SLIDE center
![Marker](markers.png)

!SLIDE center
![Markers Custom](markers_custom.png)
