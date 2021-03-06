.. PDOK Kaart documentation master file, created by
   sphinx-quickstart on Mon Feb  9 14:16:30 2015.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to PDOK Kaart's documentation!
======================================

PDOKKaart bestaat uit twee onderdelen: De Kaart Wizard en een JavaScript API.

.. todo:: kort beschrijven wat de Wizard en JS API zijn 

PDOKKaart is ontstaan uit de wens om (voor de nederlandse) overheid snel een eenvoudige kaartje met informatie te kunnen maken voor het gebruik in website of content management systeem (bijv. ter vervanging van Google Maps kaartjes). 
Daarbij wordt zoveel mogelijk gebruik gemaakt van Nederlandse gegevens/kaartmateriaal afkomstig van PDOK.

PDOKKaart is gebaseerd op OpenLayers. Hierdoor is het eenvoudig om de gestandaardiseerde geo-informatie diensten (WMS, WFS, WMTS, KML, GeoJSON.) van PDOK te tonen.

Kaart Wizard
------------

.. todo:: Iets meer uitleg over de Wizard

.. todo:: Noem de doelgroep en de use case

.. todo:: link naar rest van de documentatie

De Kaart Wizard genereert een URL waarin alle informatie opgeslagen is. Deze URL kan ook zonder de Wizard gemaakt worden met behulp van query parameters

::

	api.html?
	mapdiv=map_vialink&
	zoom=3&
	showlayerswitcher=true&
	showzoom=true&
	navigation=true&
	showscaleline=true&
	showmouseposition=true&
	loc=170000%2C470000&
	markersdef=http%3A%2F%2Fdemo-geoservices.rijkswaterstaat.nl%2Fpdokkaart%2Fapi%2Fjs%2Fpdok-markers.js&
	layersdef=http%3A%2F%2Fdemo-geoservices.rijkswaterstaat.nl%2Fpdokkaart%2Fapi%2Fjs%2Fpdok-layers.js&
	pdoklayers=BRT

.. todo:: plaats link naar voorbeelden

De Wizard kent een aantal beperkingen:

- lengte url
- complexiteit wizard
- wizard is bedoelt voor eenvoudige kaartjes, niet voor grote
webapplicaties (de JavaScript API kan daarvoor wel als basis dienen).

JavaScript API
--------------

.. todo:: wat is de JavaScript API?

.. todo:: wat zit er zoal in de API?

Via de globale `PDOK.api` en OpenLayers `map` JavaScript objecten kan een ontwikkelaar
met wat regels de PDOKKaart als basis gebruiken voor een (veel) uitgebreidere kaart-pagina.

.. NOTE:: in principe is PDOKKaart een dunne wrapper om OpenLayers heen, een mooie basis maar voor echt uitgebreide kaart-applicaties is het misschien net zo eenvoudig om zelf iets vanaf scratch te bouwen?

.. todo: hoe kan ik de JavaScript API gebruiken?

Alle code (pdok-api.js) wordt in principe opgehaald van een centrale
website. Alleen configuratie staat lokaal of in de webpagina.

:: 

    {
        "mapdiv":"map_101",
        "zoom":3,
        "showlayerswitcher":true,
        "showzoom":true,
        "navigation":true,
        "showscaleline":true,
        "showmouseposition":true,
        "loc":"170000, 470000",
        "baselayers":[{"id":"BRT","visible":true}],
        "markersdef":"http://demo-geoservices.rijkswaterstaat.nl/pdokkaart/api/js/pdok-markers.js",
        "layersdef":"http://demo-geoservices.rijkswaterstaat.nl/pdokkaart/api/js/pdok-layers.js"
    };

.. NOTE:: de 'standaardlagen' en de 'markers en lijnen' zijn geconfigureerd in aparte JSON bestanden, en kunnen dus worden vervangen door ander beter voor uw situatie eeigende lagen en makers/symbolen.

Ontwikkelen: zorg dat bovenin de pdok-api.js de twee meest benodigde URL's goed zijn geconfigureerd: 

::

    Pdok.ApiUrl = "http://kaart.pdok.nl/pdokkaart/api";`
    OpenLayers.ProxyHost = “http://<UWDOMEIN>.nl/cgi-bin/proxy.py”


Voorbeelden
-----------

Deel van de code in Github is ook een heel aantal voorbeelden met zowel URL als CODE voorbeelden van allerlei use-cases


header1
=======

header2
-------

header3
.......

Contents:


.. toctree::
   :maxdepth: 2

Inleiding
=========
Deze documentatie bevat de technische beschrijving van de PDOK kaart API inclusief voorbeelden.
De Github wiki wordt gebruikt voor de meer functionele beschrijving van PDOK kaartAPI.

Zoek een locatie

Voordat u een kaart voor uw website gaat maken, zult u eerst naar de plaats op de kaart willen gaan waarvoor u de kaart wilt maken. Dit kan door 

.. image:: images/zoombuttons.png


API - documentatie
==================

Code voorbeelden
================




Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

