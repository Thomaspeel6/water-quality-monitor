# Water Quality Monitor

A desktop dashboard for exploring UK water-quality sampling data, built in C++ and Qt 6 as the group coursework for COMP2811 User Interfaces at the University of Leeds (team of four).

It loads a year of UK water-quality sampling data (CSV) and presents it across several linked pages:

- **Dashboard**: an overview of the dataset and key indicators
- **Pollutant overview**: search a pollutant and chart its levels over time against safe thresholds
- **Persistent organic pollutants (POPs)** and **fluorinated compounds (PFAS)**: focused views with charts and compliance colouring
- **Environmental litter indicators**: litter and physical pollution by location
- **Compliance dashboard**: which sites meet or breach regulatory standards

The interface follows the coursework's usability requirements, including basic internationalisation.

## Build

Requires a C++17 compiler, CMake and Qt 6 (Widgets and Charts).

```bash
mkdir build && cd build
cmake ..
make
./waterquality
```

## Structure

- `main.cpp`, `window.*`: application entry point and main window
- `dataset.*`, `model.*`, `waterquality.*`, `csv.hpp`: data loading and the table model
- `*Page.*`: one class per dashboard page
- `stats.*`: summary statistics
