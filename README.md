<img src="https://capsule-render.vercel.app/api?type=waving&amp;height=190&amp;color=0:0B1D3A,100:2F81F7&amp;text=Zahed%20Tavangari&amp;fontSize=46&amp;fontColor=FFFFFF&amp;fontAlignY=34&amp;desc=Bioengineering%20%C2%B7%20Space%20Biomedicine%20%C2%B7%20Computational%20Modelling&amp;descAlignY=53&amp;descSize=15&amp;animation=fadeIn" alt="Zahed Tavangari" width="100%" />

<p align="center">
  <a href="https://github.com/tavangariz">
    <img src="https://readme-typing-svg.demolab.com/?font=Fira+Code&amp;weight=500&amp;size=21&amp;duration=3600&amp;pause=900&amp;color=2F81F7&amp;center=true&amp;vCenter=true&amp;width=760&amp;height=48&amp;lines=PhD+Researcher+in+Bioengineering;Space+Biomedicine+%26+Retinal+Physiology;Finite-Element+Modelling+%26+ML+Surrogates;Biomaterials%2C+Bioprinting+%26+Biomedical+Imaging;Reproducible+Scientific+Computing" alt="Research identity" />
  </a>
</p>

<p align="center">
  <a href="https://orcid.org/0000-0002-7361-9109"><img src="https://img.shields.io/badge/ORCID-0000--0002--7361--9109-A6CE39?style=for-the-badge&amp;logo=orcid&amp;logoColor=white" alt="ORCID"></a>
  <a href="https://scholar.google.com/citations?user=_u01Z-0AAAAJ"><img src="https://img.shields.io/badge/Google%20Scholar-4285F4?style=for-the-badge&amp;logo=googlescholar&amp;logoColor=white" alt="Google Scholar"></a>
  <a href="https://www.linkedin.com/in/zahed-tavangari/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&amp;logo=linkedin&amp;logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:z.tavangari@phd.uniba.it"><img src="https://img.shields.io/badge/Email-0B1D3A?style=for-the-badge&amp;logo=maildotru&amp;logoColor=white" alt="Email"></a>
</p>

<p align="center">
  <sub><b>Department of Biosciences, Biotechnology and Environment (DBBA)</b> &nbsp;·&nbsp; University of Bari Aldo Moro, Italy</sub>
</p>

---

Cells fail under stresses that are difficult to measure while they are happening: the shear a
myoblast meets inside a printing needle, the oxidative load a retinal epithelium carries under
altered gravity, the ultraviolet dose absorbed a few micrometres into a culture. I build physical
and statistical models of those stresses, and I test the models against experiments I run myself.
My doctoral work, funded by the Italian Space Agency, concerns the outer blood–retinal barrier
under gravitational unloading and the identification of countermeasure targets for
spaceflight-associated retinal alterations. I worked as a clinical medical physicist before the
doctorate, which is where the requirement that a model answer to a measurement comes from.

## Research Focus

| Area | What I work on |
|---|---|
| **Space biomedicine** | Retinal barrier models under gravitational unloading; ground-based surrogates for spaceflight stressors |
| **Computational biomechanics** | Finite-element modelling of non-Newtonian flow and cell-scale mechanical dose |
| **Biomaterials and bioprinting** | Process windows for extrusion bioprinting; micropatterned scaffolds for retinal cell culture |
| **Machine learning for physical models** | Gaussian-process surrogates over expensive solver grids; deep-learning segmentation of assay images |
| **Biomedical imaging and image analysis** | Quantitative, batch-scale readouts from fluorescence and brightfield assays; MR relaxometry |
| **Radiation and photon transport** | Monte Carlo optical and particle transport; nanoparticle-mediated thermal and radiation therapy |

## Selected Projects

### Predicting cell damage in extrusion bioprinting

<p>
  <img src="https://img.shields.io/badge/FEniCSx%20/%20DOLFINx-0B1D3A?style=flat-square" alt="FEniCSx / DOLFINx">
  <img src="https://img.shields.io/badge/Gaussian%20process%20surrogate-2F81F7?style=flat-square" alt="Gaussian process surrogate">
  <img src="https://img.shields.io/badge/ESB35%202026%20·%20Oral-475569?style=flat-square" alt="ESB35 2026 · Oral">
</p>

**Problem.** Extrusion bioprinting kills a fraction of the cells it deposits, and the settings that
decide that fraction, namely tip diameter, applied pressure and ink rheology, are still chosen by
trial and error. The quantity that matters, the mechanical dose an individual cell accumulates on
its way through the nozzle, is not measurable during a print.

**Approach.** An axisymmetric power-law Navier–Stokes model of the needle geometry, from the
cartridge through the contraction to the tip,
solved in FEniCSx/DOLFINx with a density continuation from Stokes to full inertia; Bagley-style
treatment of the entrance pressure; Lagrangian tracers for per-particle shear and extensional dose;
and a Gaussian-process surrogate, validated by leave-one-out cross-validation, fitted over a
32-case grid of four tip diameters by eight pressures. The surrogate turns a solver sweep into a
Pareto front of throughput against predicted damage.

**Why it matters.** It replaces an empirical settings search with a predicted operating window, and
it makes the trade-off explicit: how much throughput a given viability actually costs.

*Repository: `l8-myoblast-bioprinting-fem`, private pending publication. Presented as an oral
contribution at ESB35, Antwerp, September 2026.*

### Photoprotection of retinal pigment epithelium under ultraviolet stress

<p>
  <img src="https://img.shields.io/badge/Monte%20Carlo%20transport-0B1D3A?style=flat-square" alt="Monte Carlo transport">
  <img src="https://img.shields.io/badge/Reaction--diffusion-2F81F7?style=flat-square" alt="Reaction-diffusion">
  <img src="https://img.shields.io/badge/COSPAR%202026%20·%20Oral-475569?style=flat-square" alt="COSPAR 2026 · Oral">
</p>

**Problem.** Spaceflight-relevant retinal stress is hard to reproduce on the ground, so ultraviolet
exposure of ARPE-19 monolayers is used here as a controlled surrogate for the oxidative and DNA
damage involved. Polydopamine nanoparticles are a candidate countermeasure, but whether they
protect by absorbing the incident photons or by scavenging the radicals that follow is a question a
viability curve alone cannot separate.

**Approach.** An end-to-end forward model of the experiment: Monte Carlo optical transport through
the layered air / medium / cell / substrate stack, chromophore photochemistry with explicit quantum
yields, and one-dimensional reaction–diffusion of the resulting reactive species including the
oxidation kinetics of the fluorescent probe itself. The predictions are compared against paired
wet-lab assays on ARPE-19 monolayers: dsDNA quantification, DCFH-DA oxidation and the alkaline
comet assay, under control, nanoparticle, ultraviolet and combined conditions. A Geant4-DNA
component is maintained for the ionising-radiation extension.

**Why it matters.** Modelling the shielding and the chemistry separately makes the protective
mechanism identifiable rather than assumed, which is what a countermeasure has to be designed
against.

*Presented as an oral contribution at COSPAR 2026, Florence.*

### Batch-scale quantification of nuclear halo assays

<p>
  <img src="https://img.shields.io/badge/Cellpose-0B1D3A?style=flat-square" alt="Cellpose">
  <img src="https://img.shields.io/badge/OpenCV-2F81F7?style=flat-square" alt="OpenCV">
  <img src="https://img.shields.io/badge/HPC%20batch-475569?style=flat-square" alt="HPC batch">
</p>

**Problem.** The nuclear halo assay reports DNA damage through the size of the chromatin halo around
each nucleus. Scored by hand it is slow, and the threshold between a damaged and an undamaged
nucleus moves with the observer.

**Approach.** A hybrid pipeline that uses a Cellpose convolutional model for nucleus detection and
classical per-nucleus thresholding for the halo boundary, so that the learned step does what it is
good at and the measured step stays interpretable. It runs as a command-line tool over whole image
directories on the ReCaS HPC cluster and emits per-nucleus tables, summary statistics, and
classification figures for inspection.

**Why it matters.** The readout becomes reproducible and large enough to carry a statistical
comparison between conditions, instead of a small hand-scored subset.

*Repository: `Halo-assay`, private.*

> Repositories for work that is under review are kept private until the corresponding paper is
> published, at which point a clean, tagged snapshot is released. I am happy to share code and data
> with reviewers and collaborators on request.

## Technical Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,cpp,bash,linux,docker,git,github,anaconda,sklearn,opencv" alt="Python, C++, Bash, Linux, Docker, Git, GitHub, Anaconda, scikit-learn, OpenCV" />
</p>

| Layer | Tools |
|---|---|
| **Scientific computing** | Python, NumPy, SciPy, pandas, Matplotlib, Jupyter |
| **Numerical modelling** | FEniCSx / DOLFINx (finite elements), Gmsh (meshing), MPI via mpi4py, Monte Carlo photon transport (MCML), Geant4 / Geant4-DNA |
| **Machine learning** | scikit-learn (Gaussian-process regression, cross-validation), Cellpose |
| **Imaging and image analysis** | OpenCV, fluorescence and brightfield assay pipelines |
| **Reproducibility and infrastructure** | Docker, Git, conda/mamba, Make, HPC batch scheduling (HTCondor, ReCaS) |

## Research Workflow

These are the practices my project repositories are built around.

- **One canonical dataset per study.** Every reported number and every figure is read from a single
  versioned table, so a manuscript, a talk, and a notebook cannot quietly diverge onto different
  fits of the same data.
- **Builders that refuse to write.** The script that produces that table re-derives its reference
  rows, checks mesh convergence and analytical closure, and exits without writing if any gate fails.
- **A fresh clone reproduces the figures.** Paths are repository-relative and the environment is
  pinned in a container, so the figures rebuild from committed results without re-running the solver.
- **Validation against published measurements, with disagreements left visible.** Where my results
  match an independent dataset I say by how much; where they do not, the discrepancy is recorded as
  open rather than narrated away.
- **One directory per run.** Solver output is written to dated, self-contained run directories, never
  to a shared "latest" folder that overwrites its own history.

## Publications

Author lists as published; my name in bold.

1. **Tavangari, Z.**, Asadi, M., Irajirad, R., Sarikhani, A., Alamzadeh, Z., Ghaznavi, H., Khoei, S.
   *3D modeling of in vivo MRI-guided nano-photothermal therapy mediated by magneto-plasmonic
   nanohybrids.* BioMedical Engineering OnLine, 2023.
   [10.1186/s12938-023-01131-w](https://doi.org/10.1186/s12938-023-01131-w)

2. Shirvalilou, S., **Tavangari, Z.**, Parsaei, M. H., Sargazi, S., Sheervalilou, R., Shirvaliloo, M.,
   Ghaznavi, H., Khoei, S. *The future opportunities and remaining challenges in the application of
   nanoparticle-mediated hyperthermia combined with chemo-radiotherapy in cancer.*
   WIREs Nanomedicine and Nanobiotechnology, 2023.
   [10.1002/wnan.1922](https://doi.org/10.1002/wnan.1922)

3. Adel, M., Keyhanvar, P., Zahmatkeshan, M., **Tavangari, Z.**, Keyhanvar, N. *A comparative
   simulation study of piezoelectric properties in zigzag and armchair boron nitride nanotubes: by
   discovering a pioneering protocol.*
   Journal of Mathematical Chemistry, 2024.
   [10.1007/s10910-024-01635-3](https://doi.org/10.1007/s10910-024-01635-3)

4. Alipanah-poor, K., Sheervalilou, R., Irajirad, R., Sarikhani, A., **Tavangari, Z.**, Alamzadeh, Z.,
   Ghaznavi, H., Khoei, S. *Physico-chemical and MR relaxometry study of bovine serum albumin-coated
   magneto-plasmonic nanoparticles designed for potential use in cancer nanotheranostics.*
   Magnetic Resonance Imaging, 2023.
   [10.1016/j.mri.2023.06.013](https://doi.org/10.1016/j.mri.2023.06.013)

5. Adel, M., Keyhanvar, P., Zare, I., **Tavangari, Z.**, Akbarzadeh, A., Zahmatkeshan, M.
   *Nanodiamonds for tissue engineering and regeneration.* Journal of Drug Delivery Science and
   Technology, 2023.
   [10.1016/j.jddst.2023.105130](https://doi.org/10.1016/j.jddst.2023.105130)

Complete list: [ORCID](https://orcid.org/0000-0002-7361-9109) · [Google Scholar](https://scholar.google.com/citations?user=_u01Z-0AAAAJ)

## Conference Contributions

| Contribution | Venue | Type |
|---|---|---|
| Preserving Myoblast Viability in Extrusion Bioprinting: FEM-Driven ML Surrogate | ESB35, Antwerp, September 2026 | Oral |
| Polydopamine NPs Attenuate Oxidative DNA Damage in a Biomimetic Retinal Model under Simulated Spaceflight Conditions | COSPAR 2026, Florence, August 2026 | Oral |
| Optimized 2PP Strategies for Large, High-Density Micropatterned Scaffolds for Retinal Cell Culture | EMMC20, Florence, May 2026 | Poster |

## Contact

I am interested in collaborations that put modelling and experiment on the same problem:
mechanical and radiation stress in tissue models, space-relevant biology, and surrogate models
that make an expensive simulation usable at the bench.

- **Email:** [z.tavangari@phd.uniba.it](mailto:z.tavangari@phd.uniba.it)
- **ORCID:** [0000-0002-7361-9109](https://orcid.org/0000-0002-7361-9109)
- **Google Scholar:** [profile](https://scholar.google.com/citations?user=_u01Z-0AAAAJ)
- **LinkedIn:** [zahed-tavangari](https://www.linkedin.com/in/zahed-tavangari/)

<p align="center">
  <sub>University of Bari Aldo Moro &nbsp;·&nbsp; Bioengineering &nbsp;·&nbsp; Space Biomedicine</sub>
</p>

<img src="https://capsule-render.vercel.app/api?type=waving&amp;section=footer&amp;height=110&amp;color=0:2F81F7,100:0B1D3A" alt="" width="100%" />
