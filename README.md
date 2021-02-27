# METAR Dart

A library for Dart developers.

Inspired from python-metar, a library writed in Python language for parse Meteorological Aviation Weather Reports (METAR and SPECI).

Current METAR reports

The current report for a station is available at the URL

  http://tgftp.nws.noaa.gov/data/observations/metar/stations/<station>.TXT

where `station` is the ICAO station code of the airport. This is a four-letter code. For all stations at any cycle (i.e., hour) in the last  hours the reports are available at the URL

  http://tgftp.nws.noaa.gov/data/observations/metar/cycles/<cycle>Z.TXT

where `cycle` is the 2-digit cycle number (`00` to `23`).

## Usage

A simple usage example:

```dart
import 'package:metar_dart/metar_dart.dart';

main() {
  String metarCode = 'METAR MROC 071200Z 10018KT 3000 R07/P2000N BR VV003 17/09 A2994 RESHRA NOSIG';
  final metar = Metar(metarCode);

  print('Type: ${metar.type}');
  print('Wind speed: ${metar.windSpeed}');
  print('Pressure: ${metar.pressure}');
  print('Temperature: ${metar.temperature}');
}
```

## Features and bugs

Please file feature requests and bugs at the [issue tracker][tracker].

[tracker]: https://github.com/diego-garro/metar-dart/issues

## Current Sources

The most recent version of this package is always available via git, only run the following
commando on your terminal:

  git clone https://github.com/diego-garro/metar-dart

## Authors

The `python-metar` library was originaly authored by [@TomPollard][Tom Pollard] in january 2005. This package `metar-dart` for Dart Language is inspired from his work in 2020 by [@DiegoGarro][Diego Garro].

[TomPollard]: https://github.com/tomp
[DiegoGarro]: https://github.com/diego-garro