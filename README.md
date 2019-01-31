# scrumpal

Script to generate daily scrum updates using YAML and data from Redmine

Summary
-------

This script helps automate the generation of daily scrum updates. Data is pulled
from the previous day's Redmine time entries and a YAML configuration file
that's intended to be changed regularly.

The generated update can, optionally, be sent to a Slack chatroom if one
specifies a legacy API token and related confugration parameters.

Configuration
-------------

Here's an example configuration file:

    url: https://someredmineserver.com
    username: someeuser
    password: somepassword
    
    ignore issues:
    - 20
    - 100
    - 124
    
    current tasks:
    - "Code review for some feature (#12650)";
    - "Update the company website theme"
    
    current issues:
    - 10234
    - 10238
    
    blockers:
    - "Can't find the files for the website theme"
    
    slack api token: "xoxo-1716634552-3463981776-237394754607-a9345dce3239c3e07b9a514bc06ce072"
    slack username: "doug"
    slack channel: "daily-scrum"
