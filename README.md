# cf-manager
CloudFormation Stack Manager (to view / delete AWS CloudFormation Stacks)

#Installation/Setup

    git clone <this repo>
    
#Options
- action : Acceptable values are 'list','delete'
- region : Valid AWS Regions (more [here](http://docs.aws.amazon.com/general/latest/gr/rande.html))
- filterByStatus : Valid CloudFormation Stack Statuses (more [here](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-describing-stacks.html))
- pattern : A string pattern that the CloudFormation stack(s) begin with
- help : Display a helpful usage message

#Example usage

    cfmgr --pattern foo-bar- --filterByStatus CREATE_COMPLETE --action delete
The above command will list all stacks that start with "foo-bar-" and with status 'CREATE_COMPLETE' and will request input for deletion