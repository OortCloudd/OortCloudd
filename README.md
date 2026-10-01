# Nassim Louissi

Research Engineer · Machine learning for ophthalmology · Paris

I build ML experiments and the systems around them: getting data out of ophthalmic devices, turning it into usable datasets, and making training runs measurable and reproducible. I work at Quinze-Vingts Hospital in Paris, across corneal imaging, statistical modeling, and research infrastructure.

My background is in econometrics and statistics. These days, I spend a lot of time with OCT images, PyTorch, and the question of whether an experiment actually supports the conclusion we want to draw from it.

[Writing & projects](https://nassimlouissi.com) · [Publications](#selected-publications)

## What I’m working on

- **Representation learning for anterior-segment OCT.** Adapting and comparing masked reconstruction, predictive representation learning, and diffusion-based pretraining. My focus includes crop design, representation diagnostics, and evaluation that keeps patients separated across data splits.
- **The data underneath the models.** Building CorneaForge, an on-premise platform for ophthalmic device ingestion, corneal geometry and feature computation, annotation, and research datasets. I care about preserving the link between a derived measurement and its source.
- **Making limited compute useful.** Profiling training on two NVIDIA L40S GPUs, investigating input and memory bottlenecks, and checking numerical behavior before accepting an optimization.

## Open source

### [ML Training Monitor](https://github.com/OortCloudd/ml-training-monitor)

A skill for coding agents, built from the monitoring and profiling workflow I use in my own research.

It helps an agent connect existing training logs, inspect GPU activity, capture optional profiles, and investigate changes with measurements. The repository includes the dashboard, collectors, integration contracts, and profiling workflow. The supplied collectors support a single host, including multiple local GPUs; other environments need adapters.

### [OCT-CUDA](https://github.com/OortCloudd/OCT-CUDA)

A compact experiment in fusing an OCT reconstruction pipeline into a CUDA kernel with cuFFTDx. It explores how keeping intermediate values on the GPU chip changes the cost of a pipeline, with a reference implementation and benchmark.

## How I work

Follow a result back to its data. Make the comparison fair. Measure where time goes. Check what changed after an optimization.

My everyday tools include Python, PyTorch, NumPy/SciPy, CatBoost, PostgreSQL, and Linux. I also explore CUDA and lower-level systems when they help explain what the machine is doing.

## Selected publications

- **Co-first author** — [Machine Learning Model for Predicting Visual Acuity Improvement After Intrastromal Corneal Ring Surgery in Patients With Keratoconus](https://doi.org/10.1097/ICO.0000000000003933). *Cornea*, published online in 2025.
- **Co-author** — [CorvisST biomechanical indices in the diagnosis of corneal stromal and endothelial disorders: an artificial intelligence-based comparative study](https://doi.org/10.1136/bjo-2025-327855). *British Journal of Ophthalmology*, published online in 2025.

I write about the engineering behind this work at [nassimlouissi.com](https://nassimlouissi.com).
