Determine instance type support per availability zone:

aws ec2 describe-spot-price-history --region us-east-1 --instance-types m5.large --query "SpotPriceHistory[*].AvailabilityZone" --output text | tr '\t' '\n' | sort | uniq
