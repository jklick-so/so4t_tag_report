# Stack Overflow for Teams Tag Report (so4t_tag_report)
An API script for Stack Overflow for Teams that creates a report (CSV file) of how well each tag is performing. You can see an example of what the output looks like in the Examples directory ([here](https://github.com/jklick-so/so4t_tag_report/blob/main/Examples/tag_metrics.csv)).

All data obtained via the API is handled locally on the device from which the script is run. The script does not transmit data to other parties, such as Stack Overflow.

This script is offered with no formal support. If you run into issues using the script, please [open an issue](https://github.com/jklick-so/so4t_tag_report/issues) and/or reach out to the person who provided it to you. 

## Requirements
* A Stack Overflow for Teams instance (Basic, Business, or Enterprise)
* Python 3.x ([download](https://www.python.org/downloads/))
* Operating system: Linux, MacOS, or Windows

## Setup

[Download](https://github.com/jklick-so/so4t_tag_report/archive/refs/heads/main.zip) and unpack the contents of this repository

**Installing Dependencies**

There's only a single dependency: the [Requests](https://pypi.org/project/requests/) library for Python. If you already have it installed, you can skip to API authentication.
* Open a terminal window (or, for Windows, a command prompt)
* Navigate to the directory where you unpacked the files
* Install the dependencies: `pip3 install -r requirements.txt`

**API Authentication**

For the Basic and Business tiers, you'll need an API token. For Enterprise, you'll need to obtain both an API key and an API token.

* For Basic or Business, instructions for creating a personal access token (PAT) can be found in [this KB article](https://stackoverflow.help/en/articles/4385859-stack-overflow-for-teams-api).
* For Enteprise, documentation for creating the key and token can be found within your instance, at this url: `https://[your_site]/api/docs/authentication`

## Usage
In a terminal window, navigate to the directory where you unpacked the script. 
Run the script using the following format, replacing the URL, token, and/or key with your own:
* For Basic and Business: `python3 so4t_tag_report.py --url "https://stackoverflowteams.com/c/TEAM-NAME" --token "uDtDkCATuydvpj2RzXFOaA))"`
* For Enterprise: `python3 so4t_tag_report.py --url "https://SUBDOMAIN.stackenterprise.co" --key "1oklfRnLqQX49QehDBWzP3Q((" --token "uDtDkCATuydvpj2RzXFOaA))"`

The script can take several minutes to run, particularly as it gathers data from via the API. As it runs, it will continue to update the terminal window with the tasks it's performing.

When the script completes, it will indicate the the CSV has been exported, along with the name of file. You can see an example of what the output looks like [here](https://github.com/jklick-so/so4t_tag_report/blob/main/Examples/tag_metrics.csv).
