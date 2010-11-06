!SLIDE  
# Styled Maps #

!SLIDE center
![Stytle Sample 1](stytle_sample_1.png)

!SLIDE center
![Stytle Sample 1](stytle_sample_2.png)


!SLIDE

### Style Definitions ###

    @@@javascript
    var styles = [
     {
        featureType: "water",
        elementType: "all",
        stylers: [
          { saturation: 50 },
          { hue: "#0091ff" },
          { lightness: -30 }
        ]
      },
      ...
    ];

!SLIDE center
![Wizzard 1](wizzard_1.png)

!SLIDE center
![Wizzard 1](wizzard_2.png)


!SLIDE

    @@@javascript
    var styles = [ ... ];
    var my_style = new google.maps.StyledMapType(
      styles, 
      { map: map, name: 'My Style' }
    );

    map.mapTypes.set('My Style', my_style);
    map.setMapTypeId('My Style');
