# ec2Login

CLI Tool to facilitate the SSM connection to EC2s instances in AWS

![Screenshot from 2021-06-25 21-25-37](https://user-images.githubusercontent.com/79537306/123496726-e4fb8e00-d5ff-11eb-9851-a3dd0183366e.png)

# Dependencies

1. Python3 and pip3
2. AWS CLI (https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html)
3. SSM Session-Manager Plugin (https://docs.aws.amazon.com/systems-manager/latest/userguide/session-manager-working-with-install-plugin.html)
4. Python dependencies on requirements.txt (pip install -r requirements.txt)

# Install

1. Install all dependencies
2. Move ec2login file to any of the paths listed on (echo $PATH) if you want to use it in any directory

# Use

1. Run the ec2login script
2. select the instance you want to connect and press ok
3. Instances must have SSM role enabled, otherwise connection will fail
