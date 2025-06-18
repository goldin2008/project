# Risk Explanation Narrative Generator

A pipeline for generating and evaluating risk explanation narratives using SHAP values and LLMs.

## Project Structure

```text
risk_explainer/
├── config/                        # Configuration files
│   ├── __init__.py
│   └── config.py                  # Global constants and settings
│
├── clients/                       # API clients
│   ├── __init__.py
│   └── azure_openai_client.py     # Azure OpenAI client implementation
│
├── prompts/                       # Prompt engineering
│   ├── __init__.py
│   └── prompt_generator.py        # Dynamic prompt construction
│
├── model/                         # Core modeling logic
│   ├── __init__.py
│   ├── shap_analysis.py           # SHAP value computation
│   ├── shap_utils.py              # SHAP visualization helpers
│   └── trainer.py                 # Model training routines
│
├── evaluation/                    # Quality assessment
│   ├── __init__.py
│   └── judge.py                   # Narrative evaluation framework
│
├── workflows/                     # Data pipelines
│   ├── __init__.py
│   └── generate_data.py           # End-to-end narrative generation
│
├── notebooks/                     # Experimental work
│   ├── 01_feature_analysis.ipynb        # Feature exploration
│   ├── 02_llm_narrative_testing.ipynb   # Prompt engineering
│   ├── 03_judge_eval_debug.ipynb        # Evaluation tuning
│   ├── 04_end_to_end_pipeline.ipynb     # Full workflow demo
│   └── 05_run.ipynb                     # Production pipeline
│
├── data/                          # Datasets (gitignored)
│   ├── input/                     # Raw feature data
│   └── output/                    # Generated narratives
│
├── tests/                         # Test suite
│   ├── __init__.py
│   ├── test_azure_client.py       # Client tests
│   ├── test_builders.py           # Prompt builder tests
│   ├── test_judge.py              # Evaluation tests
│   └── test_generate_data.py      # Pipeline tests
│
├── scripts/                       # Utility scripts
│   └── main.py                    # CLI entry point
│
├── .env                           # Environment variables
├── .gitignore                    # Version control exclusions
├── requirements.txt              # Python dependencies
├── README.md                     # This documentation
└── setup.py                      # Package configuration