# Sid-Meier-s-Civilization-6-modding

## Table of Contents

* <a href=https://github.com/je-suis-tm/Sid-Meier-s-Civilization-6-modding#map-introductions>Map Introductions</a>
* <a href=https://github.com/je-suis-tm/Sid-Meier-s-Civilization-6-modding#script-instructions>Script Instructions</a>
* <a href=https://github.com/je-suis-tm/Sid-Meier-s-Civilization-6-modding#mod-demonstrations>Mod Demonstrations</a>

## Map Introductions

* <a href=https://github.com/je-suis-tm/Sid-Meier-s-Civilization-6-modding/blob/main/output/arctique.Civ6Map>Arctic Circle</a>

Arctic circle is a regional map that covers the majority of the northern hemisphere. The haute couture of this map is the very north. Strategic resources in this map is scarcely distributed across the continents yet concentrated inside Arctic circle. Mineral resources are modified so they can be spawned and mined on the terrains such as snow and snow hill. Leaders in this map have been given carte blanche to tap into the potential resources under the ice. Imagine a war on Greenland or Svalbard over the occurrence of aluminum. Arctic shipping routes become the new normal. This might be the future we are about to live in.

![alt text](https://github.com/je-suis-tm/Sid-Meier-s-Civilization-6-modding/blob/main/preview/civ6map.png)

* <a href=https://github.com/je-suis-tm/Sid-Meier-s-Civilization-6-modding/blob/main/output/le%20monde%20entier.Civ6Map>Distorted Earth</a>

The problem with TSL earth/huge earth is the ocean, simply too much water on the surface. Civilizations are spending a lot of time sailing rather than exploring. Whereas in distorted earth, only 30% of the surface is water. The map bears a resemblance to TSL earth with a much smaller Atlantic and Pacific. The exciting news is distorted earth doesn’t only preserve most of the terrains, features and resources in TSL earth, but it also includes all the natural wonders, city states and resources which do not get spawned in TSL earth.

![alt text](https://github.com/je-suis-tm/Sid-Meier-s-Civilization-6-modding/blob/main/preview/distorted%20earth.png)

* <a href=https://github.com/je-suis-tm/Sid-Meier-s-Civilization-6-modding/blob/main/output/ukraine.Civ6Map>Ukraine</a>

To defend people, liberty, sovereignty and civilization, this map focuses on Black Sea and Caspian Sea. To be more specific, the map is a salute to the warriors in Ukraine who bravely fight against the dictator and his invasion. Unfortunately, there is no Ukrainian leader in the game. There are only two options left – Jadwiga of Poland and Tamar of Georgia. Fight for the post-soviet prosperity, fight for the honor and fight for the democracy!

![alt text](https://github.com/je-suis-tm/Sid-Meier-s-Civilization-6-modding/blob/main/preview/ukraine.png)

## Script Instructions

* <a href=https://github.com/je-suis-tm/Sid-Meier-s-Civilization-6-modding/blob/main/basemap2civ6map.ipynb>Basemap2Civ6map Converter</a>

The script leverages python to create fantastic in-game map from basemap package (of any latitude, longitude, altitude, angle and projection). This can even be replicated on any image with designated color2terrain mapping. It will automate the geotagging of natural wonders, terrains, features, continents, resources, rivers, true start locations of civilizations and city-states. An example is showed below.

Arctic circle from Python Basemap

![alt text](https://github.com/je-suis-tm/Sid-Meier-s-Civilization-6-modding/blob/main/preview/basemap.png)

Arctic circle converted to Civ6Map

![alt text](https://github.com/je-suis-tm/Sid-Meier-s-Civilization-6-modding/blob/main/preview/civ6map.png)

*Source of all geospatial data can be found <a href=https://github.com/je-suis-tm/Sid-Meier-s-Civilization-6-modding/blob/main/data/source.md>here</a>.*

* <a href=https://github.com/je-suis-tm/Sid-Meier-s-Civilization-6-modding/blob/main/choropleth%20reader.ipynb>Choropleth Reader</a>

The script can process a choropleth image and reverse engineer colors back to the original scale-free data with latitudes and longitudes.

* <a href=https://github.com/je-suis-tm/Sid-Meier-s-Civilization-6-modding/blob/main/tifreader.ipynb>Geotiff Image Reader</a>

Best tool to recover spatial dataset from geotiff images and filter 95 percentile of the data.

* <a href=https://github.com/je-suis-tm/Sid-Meier-s-Civilization-6-modding/blob/main/mindat.ipynb>Mindat ETL Pipeline</a>

<a href=https://www.mindat.org>Mindat</a> is an excellent and free mineral database. The script scrapes the website to extract localities of different mineral deposits and dump into a nice and tidy dataframe.

* <a href=https://github.com/je-suis-tm/Sid-Meier-s-Civilization-6-modding/blob/main/shpreader.ipynb>Shape File Reader</a>

Similar to geotiff image reader, the script utilizes the same package to extract coordinates from shape file.

* <a href=https://github.com/je-suis-tm/Sid-Meier-s-Civilization-6-modding/blob/main/xmlreader.ipynb>XML Reader</a>

All relevant information regarding terrains, features and resources are stored inside XML files across DLC folders and Base Gameplay folders. This is a friendly helper to aggregate information such as tile size, spawning conditions and probabilities.

## Mod Demonstrations

The river is one of the most complicated features in civ6map. The lack of documentation took me a whole damn afternoon to grasp on how it works in the database. Rivers pass on the edge of each hexagon. There are six edges for each hexagon but each hexagon effectively controls only three edges -- the bottom left, the bottom right and the right. 

![alt text](https://github.com/je-suis-tm/Sid-Meier-s-Civilization-6-modding/blob/main/preview/riveredge.png)

![alt text](https://github.com/je-suis-tm/Sid-Meier-s-Civilization-6-modding/blob/main/preview/riverdiretion.png)

![alt text](https://github.com/je-suis-tm/Sid-Meier-s-Civilization-6-modding/blob/main/preview/riverflow.png)
