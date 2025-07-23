# Cybersecurity Event and Log Analysis

## Project Overview
This repository contains a collection of scripts and data for analyzing cybersecurity events and logs from different sources, including a general events log and data specifically from Trend Micro and Wazuh systems. The goal is to process raw security event data, clean it, extract meaningful insights, and visualize key trends related to threats, vulnerabilities, and user/device activities within a network environment.

## Files Included

* `events.csv`: Raw, uncleaned security event data. This file typically contains various security incidents, threat details, user information, and device data.
* `cleaned_security_events.csv`: A cleaned and preprocessed version of the `events.csv` file, ready for detailed analysis.
* `Wazu.ipynb`: A Jupyter Notebook dedicated to analyzing logs or data specifically related to the Wazuh Security Platform. This notebook likely focuses on:
    * Ingesting Wazuh-related security event data.
    * Identifying common threat names, severities, and alerts.
    * Analyzing event patterns based on users, devices, or time.
    * Visualizing threat landscapes or incident response metrics.
* `Weekly Trend Micro.ipynb`: A Jupyter Notebook for analyzing security data derived from Trend Micro products. This notebook probably covers:
    * Processing Trend Micro specific logs (e.g., URL filtering, application control, web reputation).
    * Summarizing blocked threats, top malicious IPs, or file types.
    * Generating weekly reports or trend summaries from Trend Micro data.

## Technologies Used

* **Programming Language:** Python
* **Libraries:** `pandas` (for data manipulation), `numpy` (for numerical operations), `matplotlib.pyplot` (for plotting), `seaborn` (for enhanced visualizations), `datetime` (for date/time handling).
* **Environment:** Jupyter Notebook

## How to Set Up and Run the Analysis

To run these notebooks and replicate the analysis on your local machine, follow these steps:

1.  **Clone the Repository:**
    If you haven't already, clone this repository to your local machine using Git:
    ```bash
    git clone [https://github.com/prathammehta23/YOUR_NEW_REPO_NAME.git](https://github.com/prathammehta23/YOUR_NEW_REPO_NAME.git)
    ```
    (Replace `YOUR_NEW_REPO_NAME` with the actual name you give this repository on GitHub, e.g., `Security_Log_Analysis`).

2.  **Navigate to the Project Directory:**
    ```bash
    cd YOUR_NEW_REPO_NAME
    ```

3.  **Install Required Libraries:**
    Ensure you have all the necessary Python libraries installed. It's recommended to use a virtual environment.
    ```bash
    pip install pandas numpy matplotlib seaborn jupyter
    ```
    (You might already have some of these, but `jupyter` is essential to run `.ipynb` files).

4.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
    This command will open a new tab in your web browser with the Jupyter Notebook interface.

5.  **Open and Run Notebooks:**
    From the Jupyter interface, you can then click on `Wazu.ipynb` or `Weekly Trend Micro.ipynb` to open them. Run the cells sequentially to execute the analysis and see the outputs.

## Data Structure / Schema (Example for `events.csv`)
While the notebooks will explore the data in detail, here's a general idea of columns you might find in `events.csv` (and `cleaned_security_events.csv`):

| Column Name      | Description                                          | Example Values                                      |
| :--------------- | :--------------------------------------------------- | :-------------------------------------------------- |
| `When`           | Timestamp of the event                               | `2025-07-17 04:51:01+05:30`                         |
| `Threat Name`    | Name of the detected threat                          | `Lockdown`, `Microsoft Activation Scripts`          |
| `Threat Path`    | File path or location of the threat                  | `\\\\192.168.3.4\\...`, `-` (if not applicable)     |
| `Event`          | Description of the security event                    | `'Lockdown' exploit prevented...`                   |
| `Cleanup Status` | Status of threat cleanup                             | `Not Cleaned`, `-`                                  |
| `Severity`       | Severity level of the threat                       | `Low`, `Medium`, `High`                             |
| `Alert`          | Indicates if an alert was triggered                  | `Yes`, `No`                                         |
| `User`           | User account associated with the event               | `ALTERMEDRCM\prakash.chandra220`                    |
| `Device`         | Device name where the event occurred                 | `Altermed-172`                                      |
| `IPAddress`      | IP address of the device                             | `172.16.0.100`                                      |
| *(and others specific to your Trend Micro or Wazuh data)* | | |

## License
[Optional: Specify a license if you want others to use, modify, and distribute your code and data. For example, MIT License.]
