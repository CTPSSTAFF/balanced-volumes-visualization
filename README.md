# balanced-volumes-visualization
App to visualize balanced volumes data on selected limited-access highways.

The development of the data and code for this application was initially funded
as part of UPWP Project #13291 of the Boston Region Metropolitan Planning Organization for Federal Fiscal Year 2019.
This work covered development of the balanced volumes data and visualization for I-93/SR-3 only.
The data and code were extended to to encompass additonal routes \(specifically US-1 and I-90\),
and to support the generation of visualiations for routes with both NB/SB and EB/WB orientations susbsequently.

The balanced volume data, and the data used to generate a schematic visualizationof this data, 
is found in the subdiretory __data/csv__.
 
The balanced volume data for 2019 was produced by Bill Kuttner. 
The balanced volume data for 2010, 2007 and 1999 was produced by Tom Lisco.

The GeoJSON data for the geometry of:
* I-93 and SR-3 within the MPO area,
* a portion of US-1 within the MPO area, and
* I-90 statewide  
is found in the subdirectory __data/geojson__.

This application relies upon the following libraries:
1. jQuery version 3.7.1 (see https://jquery.com/)
2. d3.js version 4.17.21 (see https://d3js.org/)
3. lodash.js version 3.10.1 (see https://lodash.com/)
4. turf.js version 5.2.0 (see https://turfjs.org/)
5. es6string.js (see https://github.com/jabez128/es6string)
6. syncscroll.js version 0.0.3 (see https://github.com/asvd/syncscroll)
7. jquery.scrollTo.js version 2.1.2 (see http://flesler.blogspot.com/2007/10/jqueryscrollto.html)
8. Google Maps JavaScript API version 3.x (see https://developers.google.com/maps/documentation/javascript/tutorial)
9. ctpsGoogleMapsUtils.js version 2.0 (see https://github.com/bkrepp-ctps/ctpsGoogleMapsUtils)

