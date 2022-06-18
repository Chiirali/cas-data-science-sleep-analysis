# CAS Data Science Projekt Sleep Analysis - Data Wrangling


## Datenquellen

**Mond Phasen**

Abruf: 03.04.2022
Quelle: `https://www.timeanddate.de/mond/phasen/` (Location: Basel). Händischer Download in ein CSV ohne Spalte Lunation und Duration
Dateien: 
- `raw/moon/*`

**Schlafdaten**

Abruf: 18.06.2022
Quelle: Daten Export von Fitbit Schlafdaten von privatem Account, CSV Export
Dateien: 
- `raw/sleep/*` 
- `raw/heart/*` 
- `raw/temp/*`


## Processing
- Grobes Preprocessing aller 4 DataFrames
- Zusammenführen der DataFrames auf dem Attribut 'date'


## Resultat nach Wrangling

| date     | temperature | overall_score | composition_score | revitalization_score | duration_score | deep_sleep_in_minutes | resting_heart_rate | restlessness | bpm       | Moon Phase    |
|----------|-------------|---------------|-------------------|----------------------|----------------|-----------------------|--------------------|--------------|-----------|---------------|
| 04.03.22 | -2.494845   | 67            | 17                | 15                   | 35             | 66                    | 60                 | 0.073479     | 68.873969 | First Quarter |
| 19.04.22 | -2.374779   | 75            | 16                | 17                   | 42             | 62                    | 52                 | 0.071966     | 62.836604 | First Quarter |
| 10.03.22 | -3.100641   | 88            | 21                | 22                   | 45             | 126                   | 60                 | 0.054695     | 67.206731 | First Quarter |
| 25.04.22 | -3.082295   | 56            | 15                | 15                   | 26             | 23                    | 56                 | 0.100186     | 67.187992 | First Quarter |
| 08.06.22 | -2.983674   | 75            | 20                | 19                   | 36             | 69                    | 55                 | 0.087816     | 69.163313 | First Quarter |
| 01.01.22 | -2.14144    | 68            | 19                | 18                   | 31             | 69                    | 60                 | 0.081197     | 61.607115 | First Quarter |
| 15.01.22 | -0.019856   | 61            | 17                | 10                   | 34             | 70                    | 57                 | 0.14459      | 68.972063 | First Quarter |
| 14.01.22 | -1.975761   | 77            | 21                | 20                   | 36             | 82                    | 59                 | 0.089701     | 68.562845 | First Quarter |
| 09.06.22 | -2.748225   | 76            | 22                | 16                   | 38             | 88                    | 54                 | 0.07064      | 59.214786 | First Quarter |
| 24.04.22 | -2.648158   | 68            | 16                | 15                   | 37             | 49                    | 54                 | 0.079038     | 76.126033 | New Moon      |
| 30.04.22 | -2.834139   | 78            | 21                | 18                   | 39             | 81                    | 58                 | 0.073281     | 65.089426 | New Moon      |
| 18.04.22 | -2.157149   | 84            | 21                | 22                   | 41             | 71                    | 53                 | 0.071207     | 59.130468 | New Moon      |
| 11.03.22 | -1.241001   | 84            | 21                | 18                   | 45             | 68                    | 58                 | 0.092812     | 66.110513 | New Moon      |
| 05.03.22 | -0.626451   | 82            | 21                | 19                   | 42             | 82                    | 62                 | 0.079188     | 63.769249 | New Moon      |
| 13.03.22 | -0.574393   | 70            | 15                | 15                   | 40             | 49                    | 57                 | 0.088235     | 61.645463 | New Moon      |
| 26.04.22 | -1.373009   | 79            | 20                | 14                   | 45             | 80                    | 57                 | 0.071137     | 63.024223 | New Moon      |
| 02.01.22 | -2.369522   | 84            | 19                | 20                   | 45             | 81                    | 61                 | 0.060579     | 76.712534 | New Moon      |
| 03.01.22 | -2.392509   | 68            | 19                | 15                   | 34             | 58                    | 60                 | 0.0801       | 61.696459 | New Moon      |
| 17.01.22 | -2.612512   | 80            | 21                | 21                   | 38             | 69                    | 58                 | 0.062356     | 63.264437 | New Moon      |
| 27.04.22 | -1.317362   | 87            | 22                | 20                   | 45             | 96                    | 59                 | 0.073703     | 60.999445 | New Moon      |