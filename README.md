
<!-- README.md is generated from README.Rmd. Please edit that file -->
bioRad <img src="man/figures/logo.png" align="right">
=====================================================

bioRad aims to standardize methods for extracting and reporting biological signals from weather radars. It provides functionality to access low‐level radar data, process these data into meaningful biological information on animal speeds and directions at different altitudes in the atmosphere, visualize these biological extractions, and calculate further summary statistics.

To get started, see:

-   [Dokter et al. (2018)](https://doi.org/10.1111/ecog.04028): a paper describing the package.
-   [bioRad vignette](https://adokter.github.io/bioRad/articles/bioRad.html): an introduction to bioRad's main functionalities.
-   [Function reference](https://adokter.github.io/bioRad/reference/index.html): an overview of all bioRad functions.

Installation
------------

You can install the released version of bioRad from [CRAN](https://CRAN.R-project.org) with:

``` r
install.packages("bioRad") # Coming soon!
```

Alternatively, you can install the latest development version from [GitHub](https://github.com/adokter/bioRad) with:

``` r
devtools::install_github("adokter/bioRad")
```

Then load the package with:

``` r
library(bioRad)
#> Welcome to bioRad version 0.3.0
#> Docker daemon running, Docker functionality enabled.
```

### Docker (optional)

You only need to install Docker to:

-   Read [NEXRAD radar data](https://www.ncdc.noaa.gov/data-access/radar-data) with `read_pvolfile()`. Docker is not required for reading ODIM radar data.
-   Convert NEXRAD radar data to ODIM format with `nexrad_to_odim()`.
-   Process radar data into vertical profiles of biological targets with `calculate_vp()`.

Why? bioRad makes use of a [C implementation of the vol2bird](https://github.com/adokter/vol2bird) algorithm through [Docker](https://www.docker.com/) to do the above. All other bioRad functions will work without a Docker installation.

<details> <summary><strong>Installing Docker</strong></summary>

1.  Go to [Docker Desktop](https://www.docker.com/products/docker-desktop).
2.  Download Docker for Windows or Mac (free login required) and follow the installation instructions.
3.  Open the Docker application. The Docker (whale) icon will appear in your menu bar and indicate if it is running correctly.
4.  In R do `check_docker()`.
5.  You can now use the bioRad functionality that requires Docker. </details>


``` r
```




