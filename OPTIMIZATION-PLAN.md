Current State
Total monthly cost: $18.92
Instances: 2 running
Unattached volumes: 1
Average CPU usage:
t3.micro → ~15%
t3.small → ~5⚠️ (over-provisioned)

Identified Optimizations
1. Delete Unattached EBS Volume
Problem: Paying for unused storage
Action:
aws ec2 delete-volume --volume-id vol-333
Savings:
8 GB × $0.08 = $0.64/month

2. Right-size t3.small → t3.micro
Problem: Only 5% CPU usage
Action: downgrade instance

Savings calculation:

t3.small: $0.0208/hr
t3.micro: $0.0104/hr

50% cheaper

Monthly savings:
≈ $7.50/month

3. Stop Instances Overnight (BIG WIN)
Assume dev instance runs only 8h/day instead of 24h

Savings:

16 hours/day saved × 30 days = 480 hours
480 × $0.0104 ≈ $5/month

4. Reserved Instance (Optional Bonus)
If running continuously:
Save ~30–50%

Estimated:
≈ $6/month

Implementation Priority
Quick Wins (Do immediately)
Delete unattached volume
Stop instances when not used
Medium Term
Right-size instances
Long Term
Reserved Instances



Projected Savings
Optimization	Monthly Savings
Delete volume	$0.64
Right-size instance	$7.50
Stop schedule	$5.00

Total Savings: ~$13.14/month

Final Result
Original cost: $18.92/month
Optimized cost: $5.78/month

Savings: ~69% reduction  (well above 30%)
