!SLIDE title-slide
# Performance #


!SLIDE bullets incremental

## Basic Rules

* Put JS at the bottom
* Load scripts and data on demand
* Reduce set of DOM elements

!SLIDE
### Put Scripts at Bottom ##

    @@@html
    <html>
      <head>
        <title>Title</title> 
        <link type="text/css" rel="stylesheet" … /> 
        <script type="text/javascript" … ></script>
      </head>
      <body>
        ...
      </body>
    </html>

!SLIDE
### Put Scripts at Bottom ##

    @@@html
    <html>
      <head>
        <title>Title</title> 
        <link type="text/css" rel="stylesheet" … /> 
      </head>
      <body>
        ...
        <script type="text/javascript" … ></script>
      </body>
    </html>

!SLIDE

## Load on Demand ##

!SLIDE console

### Google Loader ###

    @@@html
    <script 
      type="text/javascript" 
      src="http://www.google.com/jsapi?key=XYZ"
    ></script>

<br/>

    @@@ javascript
    google.load("maps", "3", {
      other_params: "sensor=false",
      callback: api_loaded
    });

!SLIDE

### Plain JavaScript ###

    @@@ javascript
    var script = document.createElement("script"),
      url = "http://maps.google.com/maps/api/js";
      
    url += "?sensor=false";
    url += "&callback=api_loaded";
                
    script.type = "text/javascript";
    script.src = url;
    document.body.appendChild(script);


!SLIDE

### jQuery Style ###

    @@@ javascript    
    var url = "http://maps.google.com/maps/api/js?" +
      "sensor=false&";
      "callback=?";
    
    $.getJSON(url, api_loaded); 


!SLIDE bullets
## Perfomance Rules ##

* Put JS at the bottom
* Load scripts and data on demand
* Reduce set of DOM elements
* …

!SLIDE bullets
## Perfomance Rules ##

* -
* -
* -
* DO NOT USE THE JAVASCRIPT API !

