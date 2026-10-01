# Nassim Louissi

Research Engineer · Machine learning for ophthalmology · Paris

I built and operate **CorneaForge / OphtaFlow AI**, an on-premise ophthalmic data and research platform at Quinze-Vingts Hospital in Paris. My work spans deployed device pipelines and model serving, scientific image processing, and machine learning experiments.

My background is in econometrics and statistics. I work from the original device measurements through to the model and the systems that run it.

[Writing & projects](https://nassimlouissi.com) · [Publications](#selected-publications)

## Systems, experiments, and results

- **A platform in operation.** CorneaForge ingests MS-39 and Corvis data, processes OCT images, computes corneal features, and renders examinations. OphtaFlow AI connects examination review, annotation, native videos, and existing model predictions. The stack uses FastAPI, PostgreSQL, MinIO, and dedicated systemd workers. [Architecture and deployment](https://nassimlouissi.com/blog/from-device-export-to-research-system/).
- **AS-OCT representation learning.** Five pretraining recipes share an index of **3,427,130 B-scans** and a common encoder initialization. Recorded feature spectra show concentration in the patch-limited reconstruction arms and more dispersed variation in JEPA. [Results, figures, and measurement definitions](https://nassimlouissi.com/blog/reading-pretraining-diagnostics/).
- **Two-GPU training performance.** I implemented and profiled JEPA on two NVIDIA L40S GPUs. Overlapping coordinator input preparation reduced update time from **10.246 to 8.787 seconds (14.2%)** in a matched unprofiled comparison. Input, gradient, optimizer-state, and resume checks passed without changing the training recipe.
- **Corvis video research.** Classical corneal region segmentation, motion analysis, and an experimental neural classifier, supported by synchronized inspection and human-review tools. The classifier produces uncalibrated exploratory scores; independent performance evaluation remains open.

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

You can also [watch ML Training Monitor in 48 seconds](https://nassimlouissi.com/#monitor-demo). That promotional video uses labeled synthetic telemetry; the research figures linked above contain real aggregate measurements.
