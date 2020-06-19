README

Following things are required to be done.

1. Run this jenkins pipeline from the Linux node  which has access to internet, also label to be set as linux

2. Run aws configure to connect to appropriate AWS account with role having permission to create resources on AWS

3. Ensure jq utility is installed, if not installed, please run yum -y install jq


Post above pre requ



IT will 
 - take the EBS name as vairable
 - check the snapshot status
 - give the output if its valid or not


Entire automation is done using AWS CLI 



This script is working fine, test and giving expected results.