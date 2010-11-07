!SLIDE

# Indexing Data #

!SLIDE bullets incremental

## Data Formats

* XML - Hard to handle
* HTML - Where to store the data?
* JSON - Small but not indexed

!SLIDE bullets incremental

## Microformats ##

* Human readable
* Recognized by Google
* YOU can map it

!SLIDE
### VCard Template

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

!SLIDE
### VCard Structure

    @@@sh
    .vcard
      .adr
        .street-address "Juliusstraße 25"
        .locality "Hamburg"
        .country-name "Germany" 
      .geo
        .latitude 53.55
        .longitude 9.99

!SLIDE bullets
### CSS

    @@@css  
    .geo { display: none; }

* 
* 
    
### Visual Output
    
    @@@html
    Juliusstraße 25, Hamburg, Germany


!SLIDE

### Map VCard Data

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

