# Arlington Real Estate Price Appreciation Map

I built this map in d3 and JavaScript, using the Zillow Home Value Index to measure price appreciation by zip code (https://www.zillow.com/research/data/). Price appreciation is measured by simple percentage changes 

$(P_t-P_{t-s})/P_{t-s}*100$

in the ZVHI, a measure of average house value. A dropdown menu permits the selection of one-year, five-year, or ten-year percentage changes (not annualized) and a tooltip reveals the data for a zip code upon hovering. 

Zillow provides two low-level groupings for real estate data: neighborhood and ZIP code. Use of ZIP Code data is [not best practice](https://carto.com/blog/zip-codes-spatial-analysis) for a number of reasons, including that ZIP codes represent routes rather than regions, ZIP codes may overlap with one another, and generally do not represent areas of socioeconomic interest. Neighborhood data would have been preferable but I was unable to find reliable information on the definition of neighborhood boundaries. Arlington County does not maintain official definitions of neighborhoods; while there are definitions for civic associations, these do not correpond to Zillow's neighborhood definitions. I contacted Zillow but unfortunately they were not able to provide boundary information for their neighborhood definitions.

I filtered GeoJSON data for Virginia ZIP codes to include only Arlington, then similarly filtered the Zillow data and computed percentage changes (see the Jupyter Notebook file). The d3/JavaScript code joins the location and real estate data and binds it to the SVG, with a pull-down menu in the upper left to choose the time horizon.

Note that ZIP code 22211 represents the Ft. Myer military base, hence the lack of price data (I include it on the map to provide a familiar view to people knowledgeable about Arlington County).

See the visualization [here:](https://charlie-kramer.github.io/arl_re_map/)
