# UVa Online Judge Automation

This Python project automates the process of logging into the UVa Online Judge platform, navigating through problem categories, fetching problem details, and submitting solutions. 

## Features

- Automatic login to UVa Online Judge
- Navigation through problem categories
- Fetching problem details (name, URL, ID)
- Submitting solutions automatically from specified directories

## Prerequisites

Before running the script, ensure you have the following:

- Python 3.x
- `requests` library
- `beautifulsoup4` library

You can install the required libraries using pip:

```bash
pip install requests beautifulsoup4
```

## Usage

1. **Clone the repository**:
    ```bash
    git clone https://github.com/AmirBuddy/Sync-UVa.git
    cd Sync-UVa
    ```

2. **Edit Login Credentials**:
    Open `main.ipynb` and replace the `username` and `passwd` values with your UVa Online Judge credentials.

3. **Organize Solution Files**:
    Ensure your solution files are organized like the following structure as an example:
    ```
    Getting Started: The Easy Problems/
    ├── Super Easy/
    │   ├── Problem 1/
    │   │   └── solution.cpp
    │   └── Problem 2/
    │       └── solution.cpp
    ├── Easy/
    │   ├── Problem 1/
    │   │   └── solution.cpp
    │   └── Problem 2/
    │       └── solution.cpp
    └── Medium/
        ├── Problem 1/
        │   └── solution.cpp
        └── Problem 2/
            └── solution.cpp
    ```

## Project Structure

```
uva-automation/
├── main.ipynb           # Main notebook for automation
├── README.md            # This readme file
└── requirements.txt     # Required libraries
```

## Script Overview

- **Login**: The script logs into the UVa Online Judge platform using the provided credentials.
- **Fetch Categories**: It navigates to predefined problem categories (Super Easy, Easy, Medium).
- **Retrieve Problems**: The script fetches the problems in each category.
- **Submit Solutions**: For each problem, it checks for a `.cpp` solution file in the corresponding directory and submits it.

## Error Handling

The script includes basic error handling:
- Asserts that the login was successful by checking for the presence of 'Logout' in the response.
- Ensures the problem directories and solution files exist before attempting to submit.

---

**Disclaimer**: This project is for educational purposes only. Use responsibly and adhere to UVa Online Judge's terms of service.
