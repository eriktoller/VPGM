![logo](https://github.com/eriktoller/VPAEM/blob/main/VPAEM_logo.png)
# VPAEM (Vertical Plane Analytic Element Model)
The Vertical Plane Analytic Element Model (VPAEM) is a computer program for modelling groundwater flow in the vertical plane. The program includes multiple groundwater features, e.g. fractures, cavities, inhomogeneities and more. It is written in `C++` and is run through a *MATLAB* script.

The program has been developed based on the limitless analytic element introduced in Strack (2018) and include:
- constant pressure elements
- inhomogeneities
- drainging fracutres
- blocking fractures
- wells

This program has been developed using *MATLAB* and *Microsoft Visual Stuido*; only the `.m`-, `.cpp`- and `.exe`-files are included in the repository. The solution also uses the Eigen library (Guennebaud & Jacob, 2010).

## Instructions
The plots are generated using the MATLAB program `run_VPGM.m`. The script automatically calls the ´C++´ program which solves the system and plots the results. To run the program simply run the MATLAB script.

## Input data
This list contains all the definitions of the input data defined in `run_VPGM.m`.

### Global properties
- `W_uni` uniform flow rate (complex)
- `k` hydraulic conductivity of continuum (double)
- `rho` density of groundwtaer (double)
- `g` acceleration due to gravity (double)
- `h` reference elevation (double)
- `zref` coordinates for reference point (complex)
- `fi0` hydraulic head at reference point (double)
### Blocking fractures
- `z1a` start coordinates for blocking fractures (complex vector)
- `z2a` end coordinates for blocking fractures (complex vector)
- `ka` hydraulic conductivity for blocking fractures (double vector)
- `ba` fracture width for blocking fractures (double vector)
### Drainging fracutres
- `z1b` start coordinates for draining fractures (complex vector)
- `z2b` end coordinates for draining fractures (complex vector)
- `kb` hydraulic conductivity for draining fractures (double vector)
- `bb` fracture width for draining fractures (double vector)
### Constant pressure elements
- `z1c` start coordinates for constant pressure elements (complex vector)
- `z2c` end coordinates for constant pressure elements (complex vector)
### Inhomogeneities
- `z1d` start coordinates for inhomogeneity elements (complex vector)
- `z2d` end coordinates for inhomogeneity elements (complex vector)
- `kd` hydraulic conductivity for inhomogeneity elements (double vector)
### Wells
- `zw` coordinates for wells (complex vector)
- `Qw` discharges for wells (double vector)
- `rw` radii of wells (double vector)
### Solver and ploting properties
- `ma` number of coefficients for blocking fractures (integer)
- `mfara` number of far-field correction coefficients for blocking fractures (integer)
- `mb` number of coefficients for draining fractures (integer)
- `mfarb` number of far-field correction  coefficients for draining fractures (integer)
- `mc` number of coefficients for constant pressure elements (integer)
- `mfarc` number of far-field correction  coefficients for constant pressure elements (integer)
- `md` number of coefficients for inhomogeneity elements (integer)
- `mfard` number of far-field correction  coefficients for inhomogeneity elements (integer)
- `Nc` number of integral points for constant pressure elements (integer)
- `N` multiplier for number of solution points for blocking fractures, draining fractures and inhomogeneity elements (double)
- `xfrom` starting value for x-axis (double)
- `xto` end value for the x-axis (double)
- `yfrom` starting value for the y-axis (double)
- `yto` end value for the y-axis (double)
- `Nx` number of grid points in the x-diraction (integer)
- `Ny` number of grid points in the y-direction (integer)
- `lvs` number of contour levels

## Plotting functions
The following functions are included for the plotting scheme in MATLAB
- `creat_figure.m` creat the figure window
- `Plot_line.m` plots a line from `z1` to `z2`
- `Contour_flow_net.m` contours a flow net

## Author
VPAEM is developed by:\
Erik Å.L. Toller\
*Department of Earth Sciences,*\
*Uppsala University, Uppsala, Sweden*\
*ORCID 0000-0002-7793-3998*

## License and contributing
VPAEM is licensed under the MIT license (see LICENSE.md).

## Citations
The program has been used in the following paper:
- Comming soon.

## References
Strack, O. D. L. (2018). Limitless analytic elements. *Water Resources Research*, 54(2), 1174-1190.

Guennebaud, G., Jacob, B., et al. (2010). *Eigen v3*. http://eigen.tuxfamily.org.

