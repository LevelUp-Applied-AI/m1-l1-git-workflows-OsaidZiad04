# OmniGuard: AI-Powered Cyber Threat Intelligence Platform

## Team Members
- Osaid Alhawamdeh
- Roaa Al-Qadi
- Hala Moath

## Project Overview
OmniGuard is a smart Cyber Threat Intelligence (CTI) platform that combines AI and cybersecurity. It analyzes logs and threat feeds to detect anomalies and identify potential security breaches, providing actionable insights for security teams.

## Data Sources
The project utilizes network traffic logs and cyber threat intelligence feeds. 

Data is not tracked in this repository. See the setup instructions below for how to obtain and place the data files before running any analysis. Place the data files in `data/raw/threat_logs.csv`.

## Setup Instructions
To set up the project locally, run the following commands step by step:

    git clone https://github.com/LevelUp-Applied-AI/m1-l1-git-workflows-OsaidZiad04.git
    cd m1-l1-git-workflows-OsaidZiad04
    python -m venv .venv

Activate the virtual environment depending on your operating system:

    # Mac / Linux
    source .venv/bin/activate

    # Windows Git Bash
    source .venv/Scripts/activate

    # Windows CMD
    .venv\Scripts\activate.bat

    # Windows PowerShell
    .venv\Scripts\Activate.ps1

Once activated, install the dependencies and verify the environment:

    pip install -r requirements.txt
    python test_environment.py

`test_environment.py` should print `Environment OK` when the setup is correct.

## Project Structure

    project-name/
    ├── README.md             # Project overview and setup instructions
    ├── CHANGELOG.md          # Record of notable changes
    ├── AGENTS.md             # AI contribution policy
    ├── requirements.txt      # Python dependencies
    ├── setup.sh              # Automated environment setup script
    ├── test_environment.py   # Environment validation script
    ├── .gitignore            # Files excluded from version control
    ├── src/                  # Production source code (importable modules)
    ├── notebooks/            # Exploratory analysis notebooks
    ├── data/                 # Data directory (contents not committed to Git)
    │   └── raw/              # Original unmodified data files
    └── tests/                # Automated tests


## Contributing
- **Branch Naming:** Use descriptive prefixes such as `feature/`, `setup/`, or `fix/`.
- **PR Process:** All pull requests must be reviewed by at least one team member.
- **Commit Messages:** Follow standard conventional commits format summarizing the change.