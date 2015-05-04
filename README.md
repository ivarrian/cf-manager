# cf-manager
CloudFormation Stack Manager (to view / delete AWS CloudFormation Stacks)

#Installation/Setup

    git clone <this repo>
    npm install
    
#Options
- action : (optional) Acceptable values are 'list','delete' . Default : 'list'
- region : (optional) Valid AWS Regions (more [here](http://docs.aws.amazon.com/general/latest/gr/rande.html))
- filterByStatus : (optional) Valid CloudFormation Stack Statuses (more [here](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-describing-stacks.html))
- pattern : (optional) A string pattern that the name(s) of CloudFormation stack(s) begin with. If not specified, cf-manager will attempt to list all cloudformation stacks.  
- help : (optional) Display a helpful usage message

#Example usage

    cfmgr --pattern foo-bar- --filterByStatus CREATE_COMPLETE --action delete
The above command will list all stacks that start with "foo-bar-" and with status 'CREATE_COMPLETE' and will request input for deletion