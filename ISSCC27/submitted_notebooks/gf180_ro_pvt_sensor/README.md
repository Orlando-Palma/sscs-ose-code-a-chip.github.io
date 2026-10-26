# Separating temperature from supply with two ring oscillators in GF180MCU

IEEE SSCS Code-a-Chip submission for ISSCC 2027.

Author: Orlando Arturo Palma León, Universidad de Sonora (México).

## Run it

Open `ro_pvt_gf180.ipynb` in Google Colab and choose *Runtime → Run all*. The first cell builds
ngspice 45.2 from source and fetches the GF180MCU device models at a pinned commit. The PVT grids
(105 simulations per ring), the mismatch Monte Carlo (288 simulations) and the mirror fix (170 simulations)
take most of the run and are cached as CSV files for the rest of the session. Keep the browser tab open
while it runs.

To use an existing installation instead, set `NGSPICE` (path to the ngspice binary) and `GF180_MODELS`
(folder holding `design.spice` and `sm141064.spice`) before running the first cell.

## Tools

- ngspice 45.2
- GF180MCU primitive device library `gf180mcu_fd_pr`, commit `5e4be8726e2ae8be099c4131f697a353d6457874`
- magic 8.3.464, netgen 1.5.272 and open_pdks `gf180mcuC` 1.0.471 (litex-hub conda packages, installed by the
  notebook with micromamba 2.3.0, for the layout, DRC, LVS and extraction)
- schemdraw 0.23 (installed by the notebook with pip, for the schematics)

## License

Apache License 2.0. See `LICENSE`.
