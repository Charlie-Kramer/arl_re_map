# Arlington Real Estate Price Appreciation Map

I built this map in d3 and JavaScript, using the Zillow Home Value Index to measure price appreciation by zip code (https://www.zillow.com/research/data/). Price appreciation is measured by simple percentage changes 

$(P_t-P_{t-s})/P_{t-s}*100$

in the ZVHI, a measure of average house value. A dropdown menu permits the selection of one-year, five-year, or ten-year percentage changes (not annualized) and a tooltip reveals the data for a zip code upon hovering. 

See the visualization [here:](https://charlie-kramer.github.io/arl_re_map/)
