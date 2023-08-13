<!--
SPDX-FileCopyrightText:  PyPSA-Earth and PyPSA-Eur Authors

SPDX-License-Identifier: AGPL-3.0-or-later
-->

# PyPSA-Kazakhstan

<p align="left">
by <a href="https://github.com/yerbol-akhmetov"><b>Yerbol Akhmetov</b></a>
</p>

## Development Status: **Stable and Active**

[![Status Linux](https://github.com/pypsa-meets-earth/pypsa-earth/actions/workflows/ci-linux.yaml/badge.svg?branch=main&event=push)](https://github.com/pypsa-meets-earth/pypsa-earth/actions/workflows/ci-linux.yaml)
[![Status Mac](https://github.com/pypsa-meets-earth/pypsa-earth/actions/workflows/ci-mac.yaml/badge.svg?branch=main&event=push)](https://github.com/pypsa-meets-earth/pypsa-earth/actions/workflows/ci-mac.yaml)
[![Status Windows](https://github.com/pypsa-meets-earth/pypsa-earth/actions/workflows/ci-windows.yaml/badge.svg?branch=main&event=push)](https://github.com/pypsa-meets-earth/pypsa-earth/actions/workflows/ci-windows.yaml)
[![Documentation Status](https://readthedocs.org/projects/pypsa-earth/badge/?version=latest)](https://pypsa-earth.readthedocs.io/en/latest/?badge=latest)
![Size](https://img.shields.io/github/repo-size/pypsa-meets-earth/pypsa-earth)
[![License: AGPL v3](https://img.shields.io/badge/License-AGPLv3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)
[![REUSE status](https://api.reuse.software/badge/github.com/pypsa-meets-earth/pypsa-earth)](https://api.reuse.software/info/github.com/pypsa-meets-earth/pypsa-earth)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![pre-commit.ci status](https://results.pre-commit.ci/badge/github/pypsa-meets-earth/pypsa-earth/main.svg)](https://results.pre-commit.ci/latest/github/pypsa-meets-earth/pypsa-earth/main)
[![Discord](https://img.shields.io/discord/911692131440148490?logo=discord)](https://discord.gg/AnuJBk23FU)
[![Google Drive](https://img.shields.io/badge/Google%20Drive-4285F4?style=flat&logo=googledrive&logoColor=white)](https://drive.google.com/drive/folders/1U7fgktbxlaGzWxT2C0-Xv-_ffWCxAKZz)

**PyPSA-Kazakhstan is an energy system model of Kazakhstan with data in high spatial and temporal resolution developed based on [PyPSA-Earth](https://pypsa-earth.readthedocs.io/en/latest/).** 

## Installation

1. Open your terminal at a location where you want to install pypsa-earth. Type the following in your terminal to download the package from GitHub:

    ```bash
    git clone https://github.com/yerbol-akhmetov/PyPSA-Kazakhstan.git
    ```
    Then navigate to `pypsa-earth` directory:
    ```bash
    cd pypsa-earth
    ```
2. The python package requirements are curated in the `envs/environment.yaml` file.
   In order to install the environment fast and smooth, `mamba` package is installed. First,
   activate `base` conda environment:

   ```bash
   conda activate base
   ```
   Install `mamba` package:
   ```bash
   conda install -c conda-forge mamba
   ```
    Install dependencies using `mamba`:

    ```bash
    mamba env create -f envs/environment.yaml
    ```
    Detailed instructions for installation are provided in the pypsa-earth [documentation](https://pypsa-earth.readthedocs.io/en/latest/installation.html), see `Install dependencies` and `Python dependencies`.
    After installing the environment, activate it using
    ```bash
    conda activate pypsa-earth
    ```

3. For running the optimization one has to install the solver. We can recommend CPLEX solver which has a free academic license. The installation manual is given [here](https://mertbakir.gitlab.io/operations-research/how-to-install-cplex-ibm-academic-initiative/).

4. (Optional) To use jupyter lab (new jupyter notebooks) **continue** with the [ipython kernel installation](http://echrislynch.com/2019/02/01/adding-an-environment-to-jupyter-notebooks/) and test if your jupyter lab works:

   ```bash
    ipython kernel install --user --name=pypsa-earth
    jupyter lab
   ```
5. Verify or install a java redistribution from the [official website](https://www.oracle.com/java/technologies/downloads/) or equivalent.
   To verify the successful installation the following code can be tested from bash:

   ```bash
    java --version
   ```

   The expected output should resemble the following:

   ```bash
      java version "1.8.0_341"
      Java(TM) SE Runtime Environment (build 1.8.0_341-b10)
      Java HotSpot(TM) 64-Bit Server VM (build 25.341-b10, mixed mode)
   ```
6. Before the whole workflow can be executed, the databundle must be retrieved. This can be done via:
    ```bash
    snakemake -j 1 retrieve_databundle_light
    ```

## Test run of 2020 scenario 
To run the **default 2020 scenario** of Kazakhstan *(no line and renewable expansion is allowed*):
1. Terminal/command window is located at `pypsa-earth` directory.
2. The environment is activated by `conda activate pypsa-kaz`.
3. The scenario is executed with command:
    ```bash
    snakemake -j1 solve_everything
    ```

## Questions and Issues

- We are happy to answer questions and help with issues. Future discord server link.

## Documentation

The documentation of PyPSA-Earth is available here: [documentation](https://pypsa-earth.readthedocs.io/en/latest/index.html).

## Collaborators

<!-- https://github.com/marketplace/actions/contribute-list -->

<!-- readme: collaborators,contributors,restyled-commits/- -start -->
<table>
<tr>
    <td align="center">
        <a href="https://github.com/yerbol-akhmetov">
            <img src="https://avatars.githubusercontent.com/u/113768325?v=4" width="100;" alt="yerbol-akhmetov"/>
            <br />
            <sub><b>Yerbol Akhmetov</b></sub>
        </a>
    <!-- </td>
    <td align="center">
        <a href="https://github.com/Beknaizer">
            <img src="https://avatars.githubusercontent.com/u/70391405?v=4" width="100;" alt="Beknaizer"/>
            <br />
            <sub><b>Beknazar</b></sub>
        </a> -->
    </td></tr>
</table>
<!-- readme: collaborators,contributors,restyled-commits/- -end -->
