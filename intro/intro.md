!SLIDE title-slide

# Best Practices #
## Google Maps API ##


!SLIDE bullets

# Martin Kleppe #

* Head of Development
* http://ubilabs.net/
* http://twitter.com/aemkei

!SLIDE bullets

## Google Qualified Developer ##
* ![qualified](qualified.gif)
* http://code.google.com/qualify/

!SLIDE bullets

# Topics #

* Basics
* Core Objects, Map Controls
* Events, Overlays, Services, 
* JavaScript and HTML DOM
* Troubleshooting

!SLIDE bullets

# JS Maps API Proctor #

* [http://www.devqual.com/betatest/]()
* Maps applications
* Community participation
* References
* 2 hour exam

!SLIDE bullets

# Second Slide #

* Do not use an API Key
* API Key is domain based
* Does not work in iPhone Webviews
* Limit: Per IP



!SLIDE bullets

# Microformats #

* Are human readable
* Google will parse this
* YOU can map it


!SLIDE

    @@@html
    <div class="vcard">
      <div class="adr">
        <div>
          <span class="street-address">…</span>, 
          <span class="locality">…</span>, 
          <span class="country-name">…</span>
        </div>
      </div>
      <div class="geo">
        <span class="latitude">…</span>
        <span class="longitude">…</span>
      </div>
    </div>



!SLIDE bullets

    @@@javascript
    var $items = $(".vcard");
    
    // position every vcard element
    $items.each(function(){
      var $item = $(this),
        lat = $item.find(".latitude").html(),
        lng = $item.find(".longitude").html(),
        position = new google.maps.LatLng(lat, lng);
      ...
    });


!SLIDE bullets

# English Docs Rocks! #

* <strike>code.google.com/intl/de-DE/apis/maps/</strike>
* [code.google.com/intl/en/apis/maps/](http://code.google.com/intl/en/apis/maps/) !


!SLIDE bullets
# Fusion Tables #

!SLIDE bullets
# Google Analytics #

!SLIDE bullets
# Inspiration #

* [http://ffffound.com/home/aemkei]()
* [http://twitter.com/aemkei]()
* [http://delicious.com/aemkei]()
* [http://blog.ubilabs.net]()
