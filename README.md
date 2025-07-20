# Mini_ETL_Pipeline

My mini ETL pipeline to demonstrate Data Engineering skills. This is to show case my knowledge when applying for Data Engineering roles.

## REPO structure

Mini_ETL_Pipeline/
├── etl/                    # Main ETL logic (modular scripts)
│   ├── __init__.py
│   ├── extract.py
│   ├── transform.py
│   └── load.py
│
├── config/                 # Configuration files (DB, paths, etc.)
│   └── db_config.yaml
│
├── data/                   # Raw or processed sample datasets (optional)
│   ├── raw/
│   └── processed/
│
├── logs/                   # Log output from ETL runs
│   └── etl.log
│
├── tests/                  # Unit tests for your ETL functions
│   └── test_etl.py
│
├── .env                    # Environment variables (not committed)
├── .gitignore              # Ignore sensitive and unnecessary files
├── requirements.txt        # Python dependencies
├── main.py                 # Entry point to run your ETL job
└── README.md               # Project overview, how to run, etc.
