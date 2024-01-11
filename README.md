# Digantara_Task
The code largely follows the approach provided in the question task. It is structured as multiple functions being called into __main__.

The different steps of alogorithm are timed for reference and comparison.

Based on testing, it takes around 60 secs to compute LLA for 30 satellites over 5 days in time step of 0.1 sec.

The filtered area is implemented naively assuming a rectangular-shaped region with four provided coordinates as corners.

Worker utilization and RAM/CPU usage are profiled using dask profilers, which are plotted in the end.

The computation intensive tasks of coordinate transformation are parallized using dask.delayed().

For parallization across multiple machines/CPUs, the Client (distributed Scheduler) module along with Futures (delayed functions) framework of Dask can be implemented.

