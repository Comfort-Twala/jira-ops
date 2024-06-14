# Jira-Ops

This project aims to integrate Jira Cloud with Azure DevOps by automating the process of updating Jira tickets based on commit messages and pull request activities in Azure DevOps. The integration script is written in Python and leverages the Jira and Azure DevOps APIs.

## Prerequisites

Before running the integration script, ensure you have the following prerequisites:

1. Python (version 3.6 or later) installed on your system.
2. A Jira Cloud account with necessary permissions to comment on tickets.
3. An Azure DevOps account with necessary permissions to access repositories and pull requests.

## Installation

1. Clone the repository to your local machine:
`git clone https://github.com/Comfort-Twala/jira-ops.git`
2. Navigate to the project directory:
`cd jira-ops`
3. Install the required Python packages:
`pip install -r requirements.txt`


## Configuration

1. Rename the `example.env` file to `.env`.

2. Open `.env` and update the following variables with your credentials:
- *JIRA_SERVER*: The URL of your Jira Cloud instance.
- *JIRA_USERNAME*: Your Jira Cloud username.
- *JIRA_API_TOKEN*: Your Jira Cloud API token.
- *AZURE_DEVOPS_ORG*: The URL of your Azure DevOps organization.
- *AZURE_DEVOPS_PROJECT*: The name of your Azure DevOps project.
- *AZURE_DEVOPS_REPO*: The name of your Azure DevOps repository.
- *AZURE_DEVOPS_PAT*: Your Azure DevOps Personal Access Token (PAT).

## Usage

Run the integration script:
`python main.py`

The script will automatically comment on Jira tickets based on commit messages and pull request activities in Azure DevOps.

For each commit message containing a Jira ticket ID (e.g., [ABC-123456] Added x implementation), the script will add a comment to the corresponding Jira ticket with the commit details.
When a pull request is created or updated, the script will add a comment to the Jira tickets mentioned in the commit messages, providing the pull request details.


## Note
This README.md file provides an overview of the project, installation instructions, configuration steps, usage guidelines, and information about customization and contributing. Make sure to replace the placeholders (e.g., `your-username`, `your-jira-instance.com`, `your-org`, etc.) with your actual values.

Feel free to modify and extend this README.md file based on your specific requirements and project structure.