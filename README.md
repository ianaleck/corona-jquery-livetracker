# Corona Virus / Covid-19 JQuery Live Tracker

![Corona-Virus Live Tracker](https://github.com/ianaleck/corona-jquery-livetracker/raw/master/screenshot.png "Corona-Virus Live Tracker")

Corona Virus / Covid-19 JQuery Live Tracker is a jquery plugin, built with JQuery's Ajax to get Live data in a table and or map

This project is heavily depended on [jQuery](https://jquery.com/), [jVectorMap](https://jvectormap.com/) and [Novel COVID API](https://github.com/NovelCovid/API).

## Installation

To get started, all you need to do is include the JavaScript and CSS files for the map you want to load ( contained in the `./jquery.coronatracker` folder ).

#### Here is a sample HTML page for loading the Live Tracker for all countries with default settings:

```html
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
    <title>CoronaTracker</title>
    <link rel="stylesheet" href="jquery.coronatracker/css/coronatracker.css">
    <link rel="stylesheet" href="jquery.coronatracker/jquery-jvectormap-2.0.5/jquery-jvectormap-2.0.5.css">
    <script src="jquery-3.4.1.min.js" charset="utf-8"></script>
    <script src="jquery.coronatracker/js/jquery.coronatracker.js" charset="utf-8"></script>
    <script src="jquery.coronatracker/jquery-jvectormap-2.0.5/jquery-jvectormap-2.0.5.min.js" charset="utf-8"></script>
    <script src="jquery.coronatracker/jquery-jvectormap-2.0.5/jquery-jvectormap-world-mill-en.js" charset="utf-8"></script>
  </head>
  <body>
    
    <div id="corona_container"></div>
    
    <script type="text/javascript">
        $("#corona_container").coronaTracker({}).initialize();
    </script>
  </body>
</html>
```

Lets Customize
======

While initializing a table you can provide parameters to change its look and feel.

```js
$("#corona_container").coronaTracker({
        area:"all", 
        loop:0, 
        theme:"light", 
        title:"World Stats", 
        type:"table"
 }).initialize();
```

And then for a MAP you can also provide the following parameters

```js
$("#corona_container").coronaTracker({
        loop:0,
        theme:"light",
        type:"map"
 }).initialize();
```

### Configuration Settings

**area** *'default:all'* 

expects iso2 code of a country, all or summary. if you need to select a select few countries just supply the countries iso codes seperated by a comma eg. *us,ca,zw*.  Summary gives total statistics, all returns a list if all countries with their statistics and an iso2 code returns only the statistics of the supplied country. for iso codes visit [IBAN](https://www.iban.com/country-codes) 

**loop** *'default:5'*

This is the wait preriod in minutes before the next ajax update

**theme** *'default:light'*

Select a theme between *'dark'* and *'light'* the default being *'light'*

**title** *'default:World Statistics'*

Title of the statistics *'table'* default is *'World Statistics'* to deactive insert blank String 

**type** *'default:table'*

By default *'table'* will be selected, but you can use *'map'* for a map and this will return all countries with their statistics



# <a class="bmc-button" target="_blank" href="https://www.buymeacoffee.com/ianaleck"><img src="https://cdn.buymeacoffee.com/buttons/bmc-new-btn-logo.svg" alt="Buy me a coffee"><span style="margin-left:15px;font-size:19px !important;">Buy me a coffee</span></a>
