# StatePlane_CoordinateSystem
pystateplane
Get the local state plane projection for geographica coordinates, and automatically convert between coordinates and the local state plane projection.

Includes state plane projections for the 50 states, DC, Puerto Rico, American Samoa, Guam and the US Virgin Islands.


Functions
stateplane.identify(lon, lat, fmt=None, statefp=None)
from_latlon(lat, lon, epsg=None, fips=None, abbr=None, statefp=None, countyfp=None)
from_lonlat(lon, lat, epsg=None, fips=None, abbr=None, statefp=None, countyfp=None)
For these functions, epsg, fips or abbr can be used to specify a projection. The statefp parameter can be used to specify a two-digit state (or territory) FIPS code, while results in more efficient checking. Use countyfp to specify a five-digit county FIPS code. Or, in combination with statefp, use the three-digit county stem.

to_latlon(easting, northing, epsg=None, fips=None, abbr=None)
to_lonlat(easting, northing, epsg=None, fips=None, abbr=None)
For these functions, as least one of epsg, fips and abbr must be provided.

Caveats
This module is really just a convenience wrapper for the excellent pyproj library. Big speed gains could be achieved by doing the conversions natively. Pull requests are gladly accepted.
