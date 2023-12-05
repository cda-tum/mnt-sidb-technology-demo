<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="docs/_static/mnt_light.svg" width="60%">
    <img src="docs/_static/mnt_dark.svg" width="60%">
  </picture>
</p>

# SiDB Gate Design and Analysis for Quantum Silicon Inc. (QSi)

This project introduces Silicon Dangling Bond (SiDB) gates that were designed using
the [Exhaustive Gate Designer](https://www.cda.cit.tum.de/files/eda/2023_nanoarch_minimal_gate_design.pdf). These gates
showcase exceptional performance with a
maximal [Operational Domain](https://www.cda.cit.tum.de/files/eda/2023_nanoarch_reducing_the_complexity_of_operational_domain_computation_in_silicon_dangling_bond_logic.pdf),
a maximal Population Stability, and a
maximal [Critical Temperature](https://www.cda.cit.tum.de/files/eda/2023_ieeenano_temperature_behavior.pdf).
Due to their inherent stability, these SiDB gates prove to be ideal candidates for experimental evaluation.

The following gates are designed and analyzed:

1. AND
2. Wire
3. OR
4. Fan-Out

## Software Packages

All SiDB software tools are seamlessly integrated within [_fiction_](https://github.com/cda-tum/fiction) and can be
accessed via [PyPI](https://pypi.org/project/mnt.pyfiction/).

```console
(venv) $ pip install mnt.pyfiction
```

**Detailed documentation and examples are available at [ReadTheDocs](https://fiction.readthedocs.io/en/pyml/).**

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

The SiDB gate designs and their corresponding analyses are showcased in the ``sidb_gate_designs_and_analysis.ipynb``
notebook.

## Physical Simulation Parameters

The SiDB gates are designed for the following physical parameters:

* Charge-transition energy (μ<sub>-</sub>): -0.25 eV
* Relative Permittivity (ε<sub>r</sub>): 5.6
* Thomas-Fermi screening length (λ<sub>tf</sub>): 5 nm

However, due to a maximal Operational Domain, the gate may still work for different values in the
experiment.

