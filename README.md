 # Mining research models — concise index

 This workspace contains experiments and dataset configurations for YOLOv8, YOLOv9 and YOLOv10 used in mining / coal-miner safety research. The primary dataset used for these experiments is DSLMF+ (refer to the dataset documentation or dataset owners for an authoritative citation).

 Structure
 - `yolov8_models/`, `yolov9_models/`, `yolov10_models/`
	 - Dataset configs: `data.yaml`, `data2.yaml`, ... (paths & class lists)
	 - Notebooks: `yolov*_*.ipynb` — training and inference experiments
	 - Experiment outputs: `runs/detect/<train-folder>/` — contains `args.yaml` (exact CLI/args used) and, when present, `results.csv` (metrics and logs)
	 - `yolov10_models/` includes `start.txt` with notes about that series of experiments.

 Research context
 - Purpose: model development and evaluation for mining-safety detection tasks using DSLMF+.
 - This repository is intended to support figures, tables, and reproducibility materials for a research paper. Notebooks contain the orchestration used to run experiments; `args.yaml` captures the command-line arguments for exact replication.

 Quick reproduction (minimal)
 1. Confirm dataset paths in the appropriate `data*.yaml` file in the model folder you want to run.
 2. Open the corresponding notebook (e.g., `yolov9_models/yolov9_coal_miner.ipynb`) and follow the cells, or reproduce the run by invoking the same arguments found in `runs/detect/<train-folder>/args.yaml`.
 3. After training/inference, check `runs/detect/<train-folder>/results.csv` for logged metrics.

 Environment (recommended)
 - Python 3.8+ (use a virtual environment or conda)
 - CUDA-enabled GPU for training (if available)
 - PyTorch and the YOLO implementation used in the notebooks (see the top of each notebook for imports and package versions).
 - Keep package versions consistent with notebook metadata or `args.yaml` to improve reproducibility.

 Citation and usage
 - If you use these experiments in a publication, please cite the paper associated with this work and the DSLMF+ dataset. Add the dataset's official citation where appropriate.
 - Provide provenance: include which folder/notebook and which `runs/detect/<train-folder>/args.yaml` was used to produce reported results.

 Short troubleshooting
 - No `results.csv`: the run may have not finished or results were redirected; check notebook outputs and training logs.
 - Mismatched dataset paths: update `data*.yaml` to point to your local dataset copy.

 Contact
 - This README intentionally omits direct contact information. For questions about DSLMF+ or dataset licensing, contact the dataset owners or refer to the dataset documentation.


