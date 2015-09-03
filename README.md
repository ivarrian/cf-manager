# cf-manager
CloudFormation Stack Manager (to view / delete AWS CloudFormation Stacks)

#Requirements

- [NodeJS](http://nodejs.org/)

#Installation/Setup

    git clone <this repo>
    npm install
    
#Options
- profile : (optional) Loads the profile from ~/.aws/credentials. If not specified, loads the 'default' profile. For details on how to configure the profiles, see [here](http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html#cli-multiple-profiles)
- action : (optional) Acceptable values are 'list','delete' . Default : 'list'
- region : (optional) Valid AWS Regions (more [here](http://docs.aws.amazon.com/general/latest/gr/rande.html#cfn_region))
- filterByStatus : (optional) Valid CloudFormation Stack Statuses (more [here](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-describing-stacks.html)). Specify more than one status separated by commas. If not specified, cf-manager will attempt to list stacks of all statuses. **Warning: Not specifying a status may exceed the throttle rate for API requests**
- pattern : (optional) A string pattern that the name(s) of CloudFormation stack(s) begin with. If not specified, cf-manager will attempt to list all cloudformation stacks.
- help : (optional) Display a helpful usage message

#Example usage

    cfmgr --pattern foo-bar- --filterByStatus CREATE_COMPLETE --action delete
The above command will list all stacks that start with "foo-bar-" and with status 'CREATE_COMPLETE' and will request input for deletion

# Bugs

Please report bugs [here](https://github.com/ivarrian/cf-manager/issues)
