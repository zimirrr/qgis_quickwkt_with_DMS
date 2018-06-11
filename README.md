# qgis_quickwkt_with_DMS
> altered original qgis quickwkt plugin, now with DMS conversion (only for POINTs)

I've added simple block of code to detect DMS and convert it to DD. Works only with POINTs

## Installation

Windows:
For QUICKWKT Version 2.8 copy file `QuickWKT.py` to
```
c:\Users\[your user]\.qgis2\python\plugins\QuickWKT\
```
and restart qgis.

For other version modify `QuickWKT.py` as in source code, find blockcode `# DMS2DD`
and commentate this line
```
qDebug("wkt: " + wkt.decode('utf-8'))
```

## Usage example

Now plugin can parse strings like this:
```
SRID=4326;POINT (40°26′46.0″ 79°58′56.1″)
SRID=4326;POINT (40°26'46.0 79°58'56.12345)
```