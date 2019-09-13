# Console Weather Script

Nice and small utility script to get weather in console. It uses [`gomplate`](https://github.com/hairyhenderson/gomplate) and [`wttr.in`](https://github.com/chubin/wttr.in) to query and display the weather forecast.

## Installation

1. Install `gomplate` following those [instructions](https://docs.gomplate.ca/installing/).
2. Clone the repo and place `weather` and `in.tmpl` files in some directory that's on your `$PATH`.
3. By default `weather` produces weather for [Riga, Latvia](https://goo.gl/maps/sJmMP2zCWJaUpWyL8) and [Charlottenburg, Berlin, Germany](https://goo.gl/maps/jf6tpmsnHK6mjuLR6) for 2 days, but you can edit `weather` script and change it to cities that you're interested in.

## Running

Issue command `weather` in console and you should get a list of weather forecast similar to this:

```
1: Weather report: Riga

    \  /       Partly cloudy
  _ /"".-.     17 °C
    \_(   ).   ↗ 24 km/h
    /(___(__)  10 km
               0.1 mm
                                                       ┌─────────────┐
┌──────────────────────────────┬───────────────────────┤  Fri 13 Sep ├───────────────────────┬──────────────────────────────┐
│            Morning           │             Noon      └──────┬──────┘     Evening           │             Night            │
├──────────────────────────────┼──────────────────────────────┼──────────────────────────────┼──────────────────────────────┤
│  _`/"".-.     Patchy rain po…│  _`/"".-.     Light rain sho…│  _`/"".-.     Patchy rain po…│  _`/"".-.     Patchy rain po…│
│   ,\_(   ).   15 °C          │   ,\_(   ).   16 °C          │   ,\_(   ).   13..14 °C      │   ,\_(   ).   11..13 °C      │
│    /(___(__)  ↗ 19-27 km/h   │    /(___(__)  ↗ 19-29 km/h   │    /(___(__)  → 19-31 km/h   │    /(___(__)  → 19-33 km/h   │
│      ‘ ‘ ‘ ‘  10 km          │      ‘ ‘ ‘ ‘  10 km          │      ‘ ‘ ‘ ‘  9 km           │      ‘ ‘ ‘ ‘  9 km           │
│     ‘ ‘ ‘ ‘   0.1 mm | 83%   │     ‘ ‘ ‘ ‘   0.4 mm | 89%   │     ‘ ‘ ‘ ‘   2.1 mm | 74%   │     ‘ ‘ ‘ ‘   1.0 mm | 92%   │
└──────────────────────────────┴──────────────────────────────┴──────────────────────────────┴──────────────────────────────┘
                                                       ┌─────────────┐
┌──────────────────────────────┬───────────────────────┤  Sat 14 Sep ├───────────────────────┬──────────────────────────────┐
│            Morning           │             Noon      └──────┬──────┘     Evening           │             Night            │
├──────────────────────────────┼──────────────────────────────┼──────────────────────────────┼──────────────────────────────┤
│  _`/"".-.     Patchy rain po…│  _`/"".-.     Patchy rain po…│  _`/"".-.     Patchy rain po…│    \  /       Partly cloudy  │
│   ,\_(   ).   13..14 °C      │   ,\_(   ).   16 °C          │   ,\_(   ).   14 °C          │  _ /"".-.     9..11 °C       │
│    /(___(__)  → 21-29 km/h   │    /(___(__)  → 23-30 km/h   │    /(___(__)  → 18-26 km/h   │    \_(   ).   → 17-28 km/h   │
│      ‘ ‘ ‘ ‘  9 km           │      ‘ ‘ ‘ ‘  9 km           │      ‘ ‘ ‘ ‘  9 km           │    /(___(__)  9 km           │
│     ‘ ‘ ‘ ‘   1.1 mm | 65%   │     ‘ ‘ ‘ ‘   1.1 mm | 65%   │     ‘ ‘ ‘ ‘   0.4 mm | 76%   │               0.2 mm | 53%   │
└──────────────────────────────┴──────────────────────────────┴──────────────────────────────┴──────────────────────────────┘
Location: Rīga, Vidzeme, Latvija [56.9716562,24.1665986021]

Follow @igor_chubin for wttr.in updates

2: Weather report: Charlottenburg

    \  /       Partly cloudy
  _ /"".-.     20 °C
    \_(   ).   → 26 km/h
    /(___(__)  10 km
               0.1 mm
                                                       ┌─────────────┐
┌──────────────────────────────┬───────────────────────┤  Fri 13 Sep ├───────────────────────┬──────────────────────────────┐
│            Morning           │             Noon      └──────┬──────┘     Evening           │             Night            │
├──────────────────────────────┼──────────────────────────────┼──────────────────────────────┼──────────────────────────────┤
│               Overcast       │  _`/"".-.     Patchy rain po…│  _`/"".-.     Light rain sho…│  _`/"".-.     Moderate rain …│
│      .--.     18 °C          │   ,\_(   ).   20 °C          │   ,\_(   ).   17 °C          │   ,\_(   ).   14 °C          │
│   .-(    ).   ↗ 18-22 km/h   │    /(___(__)  → 19-24 km/h   │    /(___(__)  ↘ 15-23 km/h   │    /(___(__)  ↘ 13-20 km/h   │
│  (___.__)__)  10 km          │      ‘ ‘ ‘ ‘  10 km          │      ‘ ‘ ‘ ‘  10 km          │    ‚‘‚‘‚‘‚‘   10 km          │
│               0.1 mm | 47%   │     ‘ ‘ ‘ ‘   0.5 mm | 72%   │     ‘ ‘ ‘ ‘   0.6 mm | 80%   │    ‚’‚’‚’‚’   0.2 mm | 29%   │
└──────────────────────────────┴──────────────────────────────┴──────────────────────────────┴──────────────────────────────┘
                                                       ┌─────────────┐
┌──────────────────────────────┬───────────────────────┤  Sat 14 Sep ├───────────────────────┬──────────────────────────────┐
│            Morning           │             Noon      └──────┬──────┘     Evening           │             Night            │
├──────────────────────────────┼──────────────────────────────┼──────────────────────────────┼──────────────────────────────┤
│    \  /       Partly cloudy  │    \  /       Partly cloudy  │    \  /       Partly cloudy  │    \  /       Partly cloudy  │
│  _ /"".-.     15 °C          │  _ /"".-.     18 °C          │  _ /"".-.     18 °C          │  _ /"".-.     14 °C          │
│    \_(   ).   ↘ 5-6 km/h     │    \_(   ).   → 4-5 km/h     │    \_(   ).   ↘ 3-4 km/h     │    \_(   ).   ↗ 4 km/h       │
│    /(___(__)  10 km          │    /(___(__)  10 km          │    /(___(__)  10 km          │    /(___(__)  10 km          │
│               0.0 mm | 0%    │               0.0 mm | 0%    │               0.0 mm | 0%    │               0.0 mm | 0%    │
└──────────────────────────────┴──────────────────────────────┴──────────────────────────────┴──────────────────────────────┘
Location: Charlottenburg, Charlottenburg-Wilmersdorf, Berlin, Deutschland [52.515747,13.3096834]

Follow @igor_chubin for wttr.in updates

```

## License

[The MIT License](http://opensource.org/licenses/MIT)

Copyright &copy;2019 Reinholds Zviedris

