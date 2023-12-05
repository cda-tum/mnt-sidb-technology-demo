# SiDB Gate Design and Analysis for Quantum Silicon Inc. (QSi)

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="docs/_static/mnt_light.svg" width="60%">
    <img src="docs/_static/mnt_dark.svg" width="60%">
  </picture>
</p>

This project introduces and analyzes SiDB gates designed using
the [Exhaustive Gate Designer](https://www.cda.cit.tum.de/files/eda/2023_nanoarch_minimal_gate_design.pdf). The SiDB
gates have been optimized with several metrics in mind, including Operational Domain, Population Stability, and Critical
Temperature.

The following gates are designed and analyzed:

1. [AND](sidb_gates/sqd/and_v0.sqd)
2. [Wire](sidb_gates/sqd/wire_v0.sqd)
3. [OR](sidb_gates/sqd/or_v0.sqd)
4. [Fan-Out](sidb_gates/sqd/fan_out_v0.sqd)

These gates adhere to
the [Bestagon scheme](https://www.cda.cit.tum.de/files/eda/2022_dac_hexagons_are_the_bestagons.pdf), and their file
format is `.sqd`, compatible with [_SiQAD_](https://github.com/siqad/siqad) for opening and further exploration.

## Software Packages

All SiDB software tools are seamlessly integrated within [_fiction_](https://github.com/cda-tum/fiction) and can be
accessed via [PyPI](https://pypi.org/project/mnt.pyfiction/).

```console
(venv) $ pip install mnt.pyfiction
```

The bindings can then be used in the Python project:

```python
from mnt.pyfiction import *
```

**Detailed documentation and examples are available at [ReadTheDocs](https://fiction.readthedocs.io/en/pyml/)
and [here](notebooks/sidb_gate_designs_and_analysis.ipynb).**

## Repository Structure

```plaintext
.
├── sidb_gates
│ └── sqd
│     └── ...
│        
└── notebooks
     └── sidb_gate_designs_and_analysis.ipynb
```

The SiDB gates are presented and analyzed in
the [sidb_gate_designs_and_analysis.ipynb](notebooks/sidb_gate_designs_and_analysis.ipynb)
notebook with respect to
the [Operational Domain](https://www.cda.cit.tum.de/files/eda/2023_nanoarch_reducing_the_complexity_of_operational_domain_computation_in_silicon_dangling_bond_logic.pdf),
the Population Stability, and
the [Critical Temperature](https://www.cda.cit.tum.de/files/eda/2023_ieeenano_temperature_behavior.pdf).

## Physical Simulation Parameters

The SiDB gates are designed for the following physical parameters:

* Charge-transition energy (μ<sub>-</sub>): -0.25 eV
* Relative Permittivity (ε<sub>r</sub>): 5.6
* Thomas-Fermi screening length (λ<sub>tf</sub>): 5 nm

However, due to a maximal Operational Domain, it is likely that they might work at deviations from these parameters.

