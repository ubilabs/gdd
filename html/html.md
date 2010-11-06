!SLIDE bullets incremental

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



!SLIDE bullets incremental

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

