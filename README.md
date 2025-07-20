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

### Break down of key files
main.py: Coordinates the full ETL process (calls extract → transform → load).

etl/*.py: Each script does one job. Keeps code reusable and clean.

config/db_config.yaml: Stores connection strings, table names, etc.

.env: For secure credentials (used with python-dotenv if needed).

requirements.txt: Use pip freeze > requirements.txt to capture deps.

README.md: Explain your project, setup, and what you’ve learned.

tests/: Optional but adds polish — even a single test adds credibility.
