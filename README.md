# Mini_ETL_Pipeline

My mini ETL pipeline to demonstrate Data Engineering skills.

## Author

Built by Darren Patterson — aspiring Data Engineer, with hands-on DBA experience and a passion for backend data workflows.

## REPO structure

Mini_ETL_Pipeline/
├── etl/                    # Main ETL logic (modular scripts)
│   ├── init.py
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

## Tech Stack

| Tool                   | Purpose                                                                 |
|------------------------|-------------------------------------------------------------------------|
| Python 3.x             | Main programming language used for the ETL logic.                       |
| PostgreSQL             | Target database to store the transformed data.                          |
| psycopg2               | Connects Python to PostgreSQL to execute queries.                       |
| YAML                   | Configuration format used in `db_config.yaml` for DB settings.          |
| python-dotenv          | Loads environment variables from `.env` file for secure credentials.    |
| pandas                 | For data cleaning and transformation during the ETL process.            |
| logging                | To track ETL progress, errors, and debug info in `logs/etl.log`.        |
| pytest                 | Testing ETL modules to ensure correct functionality.                    |
| Git                    | Version control and sharing the project via GitHub.                     |
| Docker                 | Optionally run PostgreSQL in a local container for isolated testing.    |

## Pipeline Flow

1. __Extract__:  
   - Read data from a CSV or static source using `extract.py`.

2. __Transform__:  
   - Clean and reshape data using `pandas`.

3. __Load__:  
   - Insert processed data into a PostgreSQL table using SQLAlchemy in `load.py`.

4. __Configuration__:  
   - Use `config/db_config.yaml` for database parameters.
   - Store sensitive info (like passwords) in `.env`.

5. __Execution__:  
   - `main.py` runs the ETL pipeline end-to-end and logs the process using Python's `logging`.
