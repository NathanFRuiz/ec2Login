#!/usr/bin/env python3

from contextlib import nullcontext
from dialog import Dialog
import os
import json

jsonstr=os.popen('aws ec2 describe-tags --filters "Name=key,Values=Name" "Name=resource-type,Values=instance" --query \'Tags[*].{name:Value,id:ResourceId}\' --output json').read()
data = json.loads(jsonstr)

choicedata=list()

d = Dialog(dialog="dialog")

for instance in data: 
        choicedata.append([instance["id"], instance["name"]])    
        
code, tag = d.menu("Instances",
                   choices=choicedata)

if code == d.OK:  
        os.system('clear')
        os.system(f"aws ssm start-session --target {tag}")
else:
        os.system('clear')
        print('ec2login closed')