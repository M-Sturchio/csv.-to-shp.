# csv.-to-shp.
Converts csv. files into shape-files

library(sf)
setwd("F:/Matt UNF/GTMNERR MarshMang/Cleaned up LicorWalz data")
DF1<-read.csv("complete_justXY.csv")

Useit <- st_as_sf(DF1, coords = c("POINT_X", "POINT_Y"))
str(Useit)
st_write(Useit,
         "useit.shp", driver = "ESRI Shapefile")                                   
