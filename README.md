# AWS-Cost-Optimization
(Identifying stale resources and optimizing AWS cost.)
-We will create a Lambda function that identifies EBS snapshots that are no longer associated with any active EC2 instance and deletes them to save on storage costs.

>How it will work?
-The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks whether the volume (if it exists) is associated with any active instance or not. If it finds a stale snapshot(unassociated), it deletes it, effectively optimizing storage costs.
