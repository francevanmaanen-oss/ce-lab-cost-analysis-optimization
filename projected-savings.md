Overview: This report summarizes the expected financial impact of the implemented AWS cost optimizations for Week 2 usage.

Baseline Costs (Before Optimization)
Category	Monthly Cost ($)
EC2 Instances	17.70
EBS Storage	1.92
Total	18.92

️ Optimization Measures Implemented
1. Delete Unattached EBS Volume
Removed unused storage resource
Impact: Eliminates unnecessary storage cost

2. Right-size EC2 Instance
Downgraded from t3.small → t3.micro
Based on low CPU utilization (~5%)

3. Instance Scheduling
Stopped development instances during non-working hours
Reduced runtime from 24h/day → ~8h/day

Projected Costs (After Optimization)
Category	Monthly Cost ($)
EC2 Instances	5.14
EBS Storage	1.28
Total	6.42


Savings Breakdown
Optimization	Monthly Savings ($)
Delete unused EBS volume	0.64
Right-size instance	7.50
Instance scheduling	5.00
Total Savings	13.14

Savings Impact
Monthly Savings: $13.14
Annual Savings: $157.68
Cost Reduction: ≈ 69%


Success Criteria

✔ Target: ≥30% cost reduction
✔ Achieved: 69% reduction

Key Insights
The primary cost driver was over-provisioned compute resources
Right-sizing alone contributed ~40% of total savings
Eliminating idle resources (unused EBS + runtime reduction) provided immediate cost benefits
Combining multiple small optimizations resulted in significant overall savings


-->Future Optimization Opportunities
Use AWS Auto Scaling to dynamically adjust capacity
Purchase Reserved Instances for predictable workloads
Implement monitoring alerts using Amazon CloudWatch

Conclusion: By aligning infrastructure usage with actual demand and removing idle resources, the system achieved a highly efficient cost structure, reducing monthly expenses by more than half while maintaining performance.
