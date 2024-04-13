---
title: Adjusting Bands on R1CBU
subtitle: 
date: 2024-03-23
tags: ['r1cbu', 'x6100', 'bands']
draft: false
---

I updated the bands 
on my X6100 running R1CBU
to follow the US band plan/privileges:
- Clone source: https://github.com/strijar/x6100_gui
- Update `sql/bands_ham.csv` to break bands by plan and privileges for US
- Update  `sql/params.sql` to not import `band_params.csv`,
  but to instead build it
  from the `bands` table
- Rebuild the db: `sqlite3 params.db < params.sql`
- Copy the new `params.db` to the `DATA` partition of the SD card

<!--more-->

Rebuilding the database
loses all your settings 
on the radio,
so you have to put those back,
but I can now see where 
the general privileges start and end
on each band.
 
Here's the resulting patch file 
to make the changes I made:
```
diff --git a/sql/bands_ham.csv b/sql/bands_ham.csv
index 81e29af..8483924 100644
--- a/sql/bands_ham.csv
+++ b/sql/bands_ham.csv
@@ -1,12 +1,26 @@
 1	160m	1810000	2000000	1
-2	80m	3500000	3800000	1
-3	40m CW	7000000	7040000	1
-4	40m SSB	7040000	7200000	1
-5	30m	10100000	10150000	1
-6	20m CW	14000000	14070000	1
-7	20m SSB	14070000	14350000	1
-8	17m	18068000	18168000	1
-9	15m	21000000	21450000	1
-10	12m	24890000	24990000	1
-11	10m	28000000	29700000	1
-12	6m	50000000	53900000	1
+2	80m Data	3525000	3600000	1
+3	80m SSB E	3600000	3800000	1
+4	80m SSB G	3800000	4000000	1
+5	40m Data E	7000000	7025000	1
+6	40m Data G	7025000	7125000	1
+7	40m SSB E	7125000	7175000	1
+8	40m SSB G	7175000	7300000	1
+9	30m	10100000	10150000	1
+10	20m Data E	14000000	14025000	1
+11	20m Data G	14025000	14150000	1
+12	20m SSB E	14150000	14225000	1
+13	20m SSB G	14225000	14350000	1
+14	17m Data	18068000	18110000	1
+15	17m SSB	18110000	18168000	1
+16	15m Data E	21000000	21025000	1
+17	15m Data G	21025000	21200000	1
+18	15m SSB E	21200000	21275000	1
+19	15m SSB G	21275000	21450000	1
+20	12m Data	24890000	24930000	1
+21	12m SSB	24930000	24990000	1
+22	10m Data	28000000	28300000	1
+23	10m SSB N	28300000	28500000	1
+24	10m SSB G	28500000	29700000	1
+25	6m CW	50000000	50100000	1
+26	6m SSB	50100000	54000000	1
diff --git a/sql/params.sql b/sql/params.sql
index b2d92a3..265ff4f 100644
--- a/sql/params.sql
+++ b/sql/params.sql
@@ -20,7 +20,8 @@ CREATE TABLE band_params(
     UNIQUE      (bands_id, name) ON CONFLICT REPLACE
 );
 
-.import band_params.csv band_params
+-- .import band_params.csv band_params
+insert into band_params select id, 'vfoa_freq', start_freq from bands;
 
 CREATE TABLE params(
     name        TEXT PRIMARY KEY ON CONFLICT REPLACE,
```
