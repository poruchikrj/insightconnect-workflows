# Description

This workflow accepts a Microsoft Teams command containing an IP address. This IP address will be checked against a pre-defined address group in Check Point to determine whether or not the IP address is present. It is assumed that this address group will be used to store IP addresses for a block policy. A message with the results will be returned.

Sample Microsoft Teams Trigger Commands:

`!block-status 198.51.100.100`

# Key Features

* The ability to see if an IP address is currently blocked by the firewall

# Requirements

* [Microsoft Teams connection](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* Check Point firewall username and password

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **the first Microsoft Teams step will need the team name and channel name updated to suit your Microsoft Teams environment!** Edit the input with the preset text of `change_me` in the first Microsoft Teams step in the workflow.

In the _Check for IP_ step edit the Address Group Name input from `change_me` to an appropriate address group.

To run the workflow,  Use the command "!block-status <IP>". The workflow will post responses in the channel.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Check Point NGFW|2.0.1|1|
|HTML|1.2.1|1|
|Microsoft Teams|3.1.0|3|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.2.0 - Replace the preset text of "change_me" with automatic team and channel name extraction in all Microsoft Teams steps except the first one | Update Microsoft Teams to version 3.1.0 | Update documentation
* 1.1.1 - Update to make the Microsoft Teams plugin the latest version
* 1.1.0 - Update to make the Check Point NGFW plugin the latest version
* 1.0.0 - Initial workflow

# Links

## References

* [Check Point](https://www.checkpoint.com/)
* [Microsoft Teams](https://teams.microsoft.com)
