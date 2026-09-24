## Proj4常见投影

[Directory of Map Projection](https://www.mapthematics.com/ProjectionsList.php)

## +proj

 - **utm**     &nbsp;&nbsp;UTM
 - **merc**    &nbsp;&nbsp;Mercator
 - **stere**   &nbsp;&nbsp;Stereographic
 - **eqc**     &nbsp;&nbsp;Equidistant_Cylindrical
 - **tmerc**   &nbsp;&nbsp;Gauss-Kruger/Transverse_Mercator
 - **lcc**     &nbsp;&nbsp;Lambert Conformal Conic
 - **aea**     &nbsp;&nbsp;Albers Equal Area
 - **sterea**  &nbsp;&nbsp;Oblique Stereographic Alternative
 - **longlat**
 - **laea**    &nbsp;&nbsp;Lambert Azimuthal Equal Area
 - **omerc**   &nbsp;&nbsp;Oblique Mercator
 - **cass**    &nbsp;&nbsp;Cassini
 - **somerc** &nbsp;&nbsp; Swiss Oblique Mercator
 - **nzmg**    &nbsp;&nbsp;New Zealand Map Grid
 - **poly**  &nbsp;&nbsp;  Polyconic (American)
 - **krovak** &nbsp;&nbsp; Krovak

## +ellps

 - WGS84
 - WGS72
 - WGS66
 - krass &nbsp;&nbsp; Krassovsky 1942
 - bessel   &nbsp;&nbsp; Bessel 1841
 - GRS80 &nbsp;&nbsp; GRS 1980
 - GRS67 &nbsp;&nbsp;  GRS 1967
 - clrk66  &nbsp;&nbsp; Clarke 1866
 - clrk80  &nbsp;&nbsp; Clarke 1880
 - intl &nbsp;&nbsp;  International 1924 
 - aust_SA &nbsp;&nbsp; Australian
 - helmert  &nbsp;&nbsp; Helmert 1906
 - airy  &nbsp;&nbsp;  Airy 1830
 - bess_nam &nbsp;&nbsp; Bessel 1841 (Namibia)
 - evrstSS &nbsp;&nbsp;  Everest 1830 (1967 Definition)


## 编译proj-6.3

```bash
 cmake -G "Visual Studio 15 2017 Win64" -DEXE_SQLITE3=D:/WorkBench/sqlite-autoconf-3320300/sqlite3.exe  -DSQLITE3_INCLUDE_DIR=D:/WorkBench/sqlite-autoconf-3320300 -DSQLITE3_LIBRARY=D:/WorkBench/sqlite-autoconf-3320300/sqlite3.lib 
```
