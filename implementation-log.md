Changes Made
1. Deleted Unused Volume
aws ec2 delete-volume --volume-id vol-333

2. Changed Instance Type
aws ec2 modify-instance-attribute \
  --instance-id i-67890 \
  --instance-type "{\"Value\": \"t3.micro\"}"

3. Stopped Instance Manually
aws ec2 stop-instances --instance-ids i-12345
4. Planned Automation
Scheduled Lambda to stop instances at 18:00
Restart at 08:00
