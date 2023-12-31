# Clone_Script

## Overview
Clone_Script is a Python script that synchronizes two folders by copying the contents of one folder to another. It also provides an option to set up a cron job for automatic synchronization at specified intervals.

## Features
- Clone files and folders from one directory to another.
- Option to set up a cron job for automatic synchronization.

## Prerequisites
- Python 3 +
- Required Python packages: `argparse`, `shutil`, `logging`, `logging.handlers`, `crontab`.

## Installation
1. Clone the repository.
2. Start the virtual env with the following command.
> venv\Scripts\activate
3. Install the required packages using the following command.
> pip install -r requirements.txt

### Note
Before you start using the tool, make sure to open the main.py and add the correct paths, lines 9 and 73

## Usage
Run the script from the command line with the following arguments:
- `-PO` or `--path_origin`: Path of the origin folder.
- `-PT` or `--path_target`: Path of the target folder.
- `-t` or `--time`: Set up synchronization time in minutes (optional).

Example:
> python main.py -PO /path/to/origin -PT /path/to/target

## Automatic Synchronization (Cron Job)
To set up a cron job for automatic synchronization, provide the `-t` flag with the desired synchronization interval in minutes. For example, the following command will run the script every 30 minutes:

> python main.py -PO /path/to/origin -PT /path/to/target -t 30

## Logging
The script logs its actions and errors to the `main.log` file located in the `var/log` directory.

## Note
- Be cautious when using automatic synchronization with a cron job. Make sure to test it thoroughly in a safe environment before deploying it to production.
- Always double-check paths and configurations before setting up cron jobs.
- This Script is designed to make exact copies of two folders, so have in mind that whatever was previously in the target folder will be automatically deleted
