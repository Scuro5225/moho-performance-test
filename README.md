# Moho / Defold browser performance test

**Open the test:** https://scuro5225.github.io/moho-performance-test/

This is a browser performance workload with seven character/creature models
and thirteen animation exports: Izzie, Rae, Quest, Emby, swamp bird, swamp
butterfly and swamp toad. No standalone water, wave or splash effects are
included. It uses Defold 1.13.0 and the delivered Moho kit's default sampling,
not the experimental mask or animated-order renderer.

## Testing

1. Open the link in a current WebGL-capable browser on a phone, tablet or computer.
2. Keep the tab visible. Landscape is recommended on phones.
3. Select 10, 25, 50 or 100 instances, or run all levels for about one minute.
4. Enter the device model, download the results JSON and send it to the person
   coordinating the test. Include browser version, power mode and visible issues.

No Python installation or local server is needed. Results are not uploaded
automatically. An interrupted benchmark should be rerun.

## Interpretation

The internal canvas is fixed at 1280 x 720. Models become smaller at higher
counts, and all thirteen resource sets are preloaded. This is not a fixed-size
overdraw test, texture-streaming test or GPU-memory measurement.

The displayed timings are wall-clock engine-update intervals, including
browser scheduling and vsync, not CPU-only or GPU-only timings. The graphics
draw-call capacity is 8192; the WebAssembly heap setting is 512 MB, not measured
memory usage. Target-device results and visual approval remain necessary.

## Published files

This repository contains the compiled browser build, not the original Moho
projects, source kit, local qualification evidence or other projects.
`manifest.json` records the workload and published file hashes.
GitHub Pages serves the root of the `main` branch.
