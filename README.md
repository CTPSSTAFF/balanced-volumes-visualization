# balanced-volumes-visualization
App to visualize balanced volumes data on selected limited-access highways.

The development of the data and code for this application was initially funded
as part of UPWP Project #13291 of the Boston Region Metropolitan Planning Organization for Federal Fiscal Year 2019.
This work covered development of the balanced volumes data and visualization for I-93/SR-3 only.
The data and code were extended to to encompass additonal routes \(specifically US-1 and I-90\),
and to support the generation of visualiations for routes with both NB/SB and EB/WB orientations susbsequently.

The balanced volume data, and the data used to generate a schematic visualization of this data, 
is found in the subdiretory __data/csv__.
 
The balanced volume data for 2019 was produced by Bill Kuttner. 
The balanced volume data for 2010, 2007 and 1999 was produced by Tom Lisco.

The GeoJSON data defining the the geometry of the following routes is found in the subdirectory __data/geojson__:
* I-93 and SR-3 within the MPO area,
* a portion of US-1 within the MPO area, and
* I-90 statewide  

The schema of the 'wireframe and volumes' CSV files that drive the visualization is as follows:

| Column Name | Description |
| --- | --- |
| data_id | Symbolic identifier of road segment or ramp |
| description | Description of road segment or ramp |
| nlanes | Number of lanes in road segment or ramp |
| yr_1999 | 1 = segment was present in 1999; 0 = segment was not present in 1999 |
| yr_2007 | 1 = segment was present in 2007; 0 = segment was not present in 2007 |
| yr_2010 | 1 = segment was present in 2010; 0 = segment was not present in 2010 |
| yr_2019 | 1 = segment was present in 2019; 0 = segment was not present in 2019 |
| awdt_yyyy | Balanced average weekday daily traffic volume in year 'yyyy' |
| peak_yyyy_6_to_7_am | Balanced volume between 6:00 a.m. to 7:00 a.m. in year 'yyyy' |
| peak_yyyy_7_to_8_am | Balanced volume between 7:00 a.m. to 8:00 a.m. in year 'yyyy' |
| peak_yyyy_8_to_9_am | Balanced volume between 8:00 a.m. to 9:00 a.m. in year 'yyyy' |
| peak_yyyy_9_to_10_am | Balanced volume between 9:00 a.m. to 10:00 a.m. in year 'yyyy' |
| peak_yyyy_3_to_4_pm | Balanced volume between 3:00 p.m. to 4:00 p.m. in ear 'yyyy' |
| peak_yyyy_4_to_5_pm< | Balanced volume between 4:00 p.m. to 5:00 p.m. in year 'yyyy' |
| peak_yyyy_5_to_6_pm | Balanced volume between 5:00 p.m. to 6:00 p.m. in year 'yyyy' |
| peak_yyyy_6_to_7_pm | Balanced volume between 6:00 p.m. to 7:00 p.m. in year 'yyyy' |
| cum_yyyy_6_to_9_am | Balanced volume in morning peak period (6:00 a.m. to 9:00 a.m.) in year 'yyyy' |
| cum_yyyy_3_to_6_pm | Balanced volume in afternoon peak period (3:00 p.m. to 6:00 p.m.) in year 'yyyy' |

A value of -9999 in any field indicates 'NO DATA' for that field.

Note: Balanced volumes were __not__ produced for all routes within the MPO or across 
tht state \(depending upon which agency funded the work\) for every year. For any given
route, the coverage from year-to-year was 'spotty', with gaps of 10 years \(sometimes more \)
between each set of blanced volume data. The direct consequence of this is that the 
schema of the CSV files varied from route to route, depending upon the years for 
which balanced volume data was produced for that route. Hence the use of 
the term 'generic schema', above.

The years for which balanced volume data was available for and included in the app 
for the routes currently supported by the app is as follows:

| Route | 1999 | 2007 | 2010 | 2019 |
| --- | --- | --- | --- | --- |
| I-93/SR-3 | yes | no | yes | yes |
| US-1 | no | yes | no | yes |
| I-90 | no | no | yes | yes |

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
