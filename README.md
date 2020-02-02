# pyATS_genie

## Use Cases
- Network verification tool

## Installation
- Install genie as a whole
    - $ pip3 install genie

- To upgrade this package manually
    - $ pip3 install --upgrade genie

- To install alpha/beta versions, add --pre
    - $ pip3 install --pre genie


## Genie Commands/Examples
- Learn about device interfaces and output those files into a 'learn' folder
    - $ genie learn interface --testbed testbed.yaml --device ios-1 --output learn

- Run a diff against 2 directories/files
    - $ genie diff learn learn2 --output diff1

- Learn all from Genie and output those files into a 'learn' folder
    - $ genie learn all --testbed testbed.yaml --device ios-1 --output learn

- Run's a command against testbed file and stores the output
    - $ genie parse "show ip ospf database router" --testbed testbed.yaml --device ios-1 --output quickdemo


## Examples

### Example 1:
- Run genie learn and output to folder
- Make a network change via CLI
- Run genie learn again and output to different folder
- Run a diff

### Example 2:
- Create a troubleshooting lab
- Run genie learn and output to folder
- Make a routing change to break a network
- Run genie routing commands to show diffs in routing change


## Questions:
- Is 'testbed' file a default name?
- How do we store passwords from the testbed file?
    - Store using environment vars on local machine?
    - Read creds from a vault (netbox/hashicorp)
- Where to start?
    - Genie is part of pyATS. The best place to start is with genie CLI


## Advantages of Genie
- No need for API's - it's all done via the CLI
- Genie makes data structure output the SAME regardless if the commands run on an IOS-XE/XR or NXOS device which makes it easier for comparisons


## Extra Curricular
- Look into Genie Triggers
    - Example: tries to re-establish BGP peers if they go down


## Documentation:
- Genie Docs
    - https://developer.cisco.com/docs/genie-docs/
    - https://developer.cisco.com/docs/pyats/#!introduction/pyats-genie
- Genie Source Code:
    - https://github.com/CiscoTestAutomation/genielibs
- Genie API Library
    - https://pubhub.devnetcloud.com/media/genie-feature-browser/docs/#/
- Genie PyPi Page
    - https://pypi.org/project/genie/
- Genie Demonstration
    - https://github.com/hpreston/netdevops_demos/tree/master/genie-cli-1


## Videos
- David Bombal & Hank Preston
    - https://www.youtube.com/watch?v=unOmwDsMj8k