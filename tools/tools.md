HTTP Web Services (Geocoding, Elevation, Directions)


!SLIDE
# Spreadsheets #

    @@@javascript
    var geocoder = Maps.newGeocoder();

    function GEOCODE(address) {
      if (!address){ return ""; }
      var results = geocoder.geocode(address).results;
      if (results && results.length){
        var location = results[0].geometry.location;
        return location.lat + "," + location.lng;
      } 
      return "";
    }
    

!SLIDE

    @@@sh
    =GEOCODE(D11;E11)


!SLIDE

    @@@javascript
    $.getJSON(
      MY_PUPLIC_SHEET_URL, 
      data_loaded
    );
    
    function data_loaded(data){
      $.each(data.feed.entry, function(){
        var geocode = this["gsx$geocode"]["$t"];
        var lat_lng = geocode.split(","),
        var position = new google.maps.LatLng(
          lat_lng[0], 
          lat_lng[0]
        );
      });
    }