# A scale-dependent vacuum

**Vacuum energy along the renormalisation scale, one acceleration scale from galaxies to clusters, and a fading dark energy**
Mike One · Independent researcher, Italy

- `A_scale_dependent_vacuum_Mike_One.pdf`: the paper (11 pages)
- `A_scale_dependent_vacuum_source.zip`: LaTeX source and figures
- `GM_physical_plane_paper.zip`: the full test suite behind every number in the paper

The test suite produces 73 labelled results on public data: derivations, tests with pass/fail rules fixed before running, measurements, constraints and diagnostics. The data are SPARC galaxies, Pantheon+ supernovae, DESI DR2, BOSS, X-COP and kinematic clusters, and four high-redshift galaxy samples.

## Rerunning everything

    unzip GM_physical_plane_paper.zip
    cd GM_physical_plane_paper
    pip install -r requirements.txt
    python run_all.py

Data download automatically on the first run. Results are written to `results/paper_results.json`.

## Where each result appears in the paper

| Cell | Section |
| --- | --- |
| `p01_setup.py` | Data download (with checksums) and the result registry |
| `p02_geometry.py` | §2 Geometry |
| `p05_vacuum_along_S.py` | §3 Vacuum energy at four scales; cosmology likelihoods used in §6–§7 |
| `p04_galactic_gradient.py` | §4 Galaxies: the vacuum-gradient field on SPARC |
| `p08_redshift.py` | §4 Redshift test of the galactic scale |
| `p04b_clusters.py` | §5 Groups and clusters |
| `p06_top_of_map.py` | §6 The late-time vacuum |
| `p07_null_tests.py` | §7 Null tests |
| `p03_map.py` | §8 Structures along S |
| `p09_summary.py` | Writes every result to `results/` |

The code folder keeps the name and internal README of an earlier draft of this work. In the code, "GM" is the name of the model (for example, "GM prediction"). The code and data are unchanged from that draft.

## Acknowledgments

I thank R. Monjo for being the first to run the test suite, for comments on the redshift test and the plasma term, and for catching a bug when porting to Windows.
