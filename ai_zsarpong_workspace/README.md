# AI Workspace — ai_zsarpong_workspace

Purpose
- A uniquely-named AI workspace for this repository to hold datasets, model manifests, prompt templates, training/inference scripts, infra, and docs.
- Large binary artifacts (weights, raw datasets) must not be checked in. Use manifests or pointers (S3 / Hugging Face / other storage).

Unique naming
- This workspace uses the ai_zsarpong_* prefix so it doesn't collide with other AI workspaces across projects.

Structure overview
- ai_zsarpong_models/: pretrained & fine-tuned model manifests (no raw weights checked in).
- ai_zsarpong_data/: dataset manifests and preprocessing.
- ai_zsarpong_prompts/: canonical system prompts and few-shot templates.
- ai_zsarpong_services/: inference API and worker wrappers.
- ai_zsarpong_scripts/: train/eval/infer entrypoints.
- ai_zsarpong_notebooks/: experimentation notebooks (.ipynb).
- ai_zsarpong_infra/: Dockerfiles, k8s manifests and deployment helper scripts.
- ai_zsarpong_tests/: unit and integration tests for AI components.
- ai_zsarpong_docs/: architecture notes and model cards.

Quick start
1. Add dataset pointers to ai_zsarpong_workspace/ai_zsarpong_data/datasets.md (do NOT add raw data).
2. Create a virtualenv and install the project's AI dependencies (we will add a requirements file if you want).
3. Use ai_zsarpong_workspace/ai_zsarpong_scripts/train.py to run experiments (skeleton provided).
4. Keep model metadata and manifests in ai_zsarpong_models/ instead of binary files.

Notes
- I will add a .gitignore to keep weights and raw data out of the repo.
- If you want, I can also add example train.py, infer.py skeletons and a model_manifest.json to track remote locations for weights.