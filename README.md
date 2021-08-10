# ASMC Data

Public data for use with ASMC.

Files in this repository can be used to run examples for ASMC and FastSMC, and is also used internally for regression testing.

## Contents

### :file_folder: `/decoding_quantities`

Two sets of decoding quantities with corresponding CSFS files and intervals information.

Both sets were generated with the `CEU.demo` demography in :file_folder: `/demographies`, the correspondingly-named discretizations in :file_folder: `/discretizations`, and frequencies information from UKBB in :file_folder: `/frequencies`.

The `10-20-2000` uses a finer time discretization with steps of size 10.0 and 20.0 up to 2000.0, while `30-100-2000` uses a coarser time discretization with steps of size 30.0 and 100.0 up to 2000.0.


### :file_folder: `/demographies`

Contains the CEU demographic model used to generate the discretizations and decoding quantities, along with all other demographic models that can be used to [prepare decoding quantities](https://github.com/PalamaraLab/PrepareDecoding) by using their corresponding three letter code.

These models were inferred using smc++ in the PyRho paper and corresponds to [these population sizes](https://github.com/popgenmethods/pyrho/blob/master/smcpp_popsizes_1kg.csv), but rescaled to assume mutation rate of 1.65e-8.



### :file_folder: `/discretizations`

Contains the discretizations used to generate the decoding quantities.
As explained above, the `10-20-2000` is a finer time discretization (159 points) than `30-100-2000` (69 points).

Both use manually-specified time values up to 2000.0, after which a number of quantiles are generated from the demography using an exponential model.


### :file_folder: `/frequencies`

Frequencies information from UKBB.
