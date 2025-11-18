# AWS_Cloud_Cost_Optimization

## Identifying Stale EBS Snapshots
In this example, we'll create a Lambda function that identifies EBS snapshots that are no longer associated with any active EC2 instance and deletes them to save on storage costs.

## Description:
The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if exists) is not associated with any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.

<img width="1858" height="821" alt="Screenshot (56)" src="https://github.com/user-attachments/assets/0e6f391e-a717-4338-88cf-c290fd4528e1" />
