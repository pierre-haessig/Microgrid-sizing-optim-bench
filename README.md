# Benchmark of optimization algorithms for Microgrid sizing

*PH, October 2023*

Tools:

- [Microgrids.jl](https://github.com/Microgrids-X/Microgrids.jl)
- optimizers from [NLopt.jl](https://github.com/JuliaOpt/NLopt.jl/) (wrapper of https://nlopt.readthedocs.io)

All the code is in the notebook [Microgrid_sizing_optimization.ipynb](Microgrid_sizing_optimization.ipynb)

- raw results are saved in [sizing_optimizations_3360.csv](sizing_optimizations_3360.csv) table (and in a LibreOffice Calc annotated version `sizing_optimizations_3360.ods`)
- results figures saved in [figures](figures) folder

This experiment is used in the poster *Which optimization “ﬂavor” for sizing Microgrid energy systems?*, Julia Optimization Days 2023, https://hal.science/IETR-AUT/hal-04233749v1

## Results

Among NLopt.jl derivative free optimizers, the two which stands out are:

- DIRECT for a medium number of iterations
- CRS2 for more iterations.



![opti_budget_variability_shedmax_0.000](figures/opti_budget_variability_shedmax_0.000.png)![opti_budget_variability_shedmax_0.001](figures/opti_budget_variability_shedmax_0.010.png)
