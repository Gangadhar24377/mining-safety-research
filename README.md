 # Mining research 

This repository contains experiment configurations, datasets, and reproducibility materials for **YOLOv8**, **YOLOv9**, and **YOLOv10** models applied to **mining and coal-miner safety detection** tasks.  
The experiments are primarily based on the **DSLMF+ dataset** (refer to the dataset documentation or dataset owners for authoritative citation and access details).

---

# Repository Structure and Folder details
 - `yolov8_models/`, `yolov9_models/`, `yolov10_models/`
	 - Dataset configs: `data.yaml`, `data2.yaml`, ... (paths & class lists)
	 - Notebooks: `yolov*_*.ipynb` — training and inference experiments
	 - Experiment outputs: `runs/detect/<train-folder>/` — contains `args.yaml` (exact CLI/args used) and, when present, `results.csv` (metrics and logs)
	 - `yolov10_models/` includes `start.txt` with notes about that series of experiments.

---

# Research context
This repository supports the **model development, evaluation, and reproducibility** of experiments conducted as part of an academic study on **mining safety detection** using the **DSLMF+ dataset**.  

The work aims to:  
- Benchmark YOLOv8–YOLOv10 architectures on mining-safety detection tasks.  
- Provide transparent configurations and training parameters for reproducibility.  
- Support the figures, tables, and performance analyses presented in the associated research paper.  

Each experiment’s configuration (`args.yaml`) ensures that reported results can be exactly replicated.

---

# Quick reproduction (minimal)
1. **Configure dataset paths:**  
   Open the appropriate `data*.yaml` file inside the model folder (YOLOv8/9/10) and verify dataset paths.

2. **Run experiments:**  
   - Option 1: Open the corresponding notebook (e.g., `yolov9_models/yolov9_coal_miner.ipynb`) and execute the cells sequentially.  
   - Option 2: Run the experiment directly via command line using the same arguments found in `runs/detect/<train-folder>/args.yaml`.

3. **View results:**  
   After training/inference, metrics will be available in `runs/detect/<train-folder>/results.csv`.

---

# Recommended Environment  

| Component | Recommended Version / Notes |
|------------|-----------------------------|
| Python | ≥ 3.8 |
| PyTorch | As used in the notebooks |
| CUDA | Enabled GPU recommended for training |
| Notebook Metadata | Maintain same package versions for reproducibility |
| Virtual Environment | Use Conda or venv to isolate dependencies |

Ensure that package versions align with those listed in the notebooks or `args.yaml` to maintain reproducibility across runs.

---

# Citation & Usage  

If you use this repository or its experiments in your research, please:

1. Cite the **associated paper** and the **DSLMF+ dataset** appropriately.  
2. Provide provenance details in your work:
   - Specify the folder and notebook used (e.g., `yolov10_models/yolov10_coal_miner.ipynb`)  
   - Mention the exact `runs/detect/<train-folder>/args.yaml` file for reproducibility.  

> Example citation format:
> > “Experiments were conducted using configurations from the *Mining Research YOLOv9 workspace*, trained on DSLMF+ dataset (refer to dataset documentation for citation).”

---

 Short troubleshooting
 - No `results.csv`: the run may have not finished or results were redirected; check notebook outputs and training logs.
 - Mismatched dataset paths: update `data*.yaml` to point to your local dataset copy.

---

# Troubleshooting  

| Issue | Possible Cause | Suggested Fix |
|--------|----------------|----------------|
| `results.csv` missing | Training was incomplete or results redirected | Check notebook logs and confirm successful run completion |
| Dataset not found | Incorrect dataset paths in YAML | Update `data*.yaml` to match your local dataset structure |
| Inconsistent results | Version mismatch | Match Python, PyTorch, and YOLO versions with notebook metadata |

---

# Contact  

This repository omits direct contact information to maintain research integrity.  
For dataset-related questions or licensing inquiries, please refer to the **official DSLMF+ dataset documentation or contact the dataset owners**.

---

