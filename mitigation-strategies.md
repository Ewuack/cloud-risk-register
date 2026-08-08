# Mitigation Strategies

## IAM Risks
**Overly permissive IAM roles**  
Use predefined roles; enforce least privilege; review monthly.

**Service accounts with admin privileges**  
Remove admin roles; use workload identity federation.

**No MFA on admin accounts**  
Enforce MFA for all privileged users.

**IAM roles not reviewed regularly**  
Implement quarterly IAM review.

## VPC Risks
**Publicly exposed VPC subnet**  
Use private subnets; restrict external IPs.

**Firewall rules allow 0.0.0.0/0**  
Restrict to specific IP ranges; use Cloud Armor.

**Unrestricted API access**  
Use VPC-SC; restrict API endpoints.

**No private service access**  
Enable Private Service Connect.

## Storage Risks
**Publicly accessible storage buckets**  
Disable public access; use uniform bucket-level access.

**No encryption at rest**  
Enable CMEK or Google-managed encryption.

**No versioning or backup strategy**  
Enable object versioning; set lifecycle rules.

## Logging Risks
**Cloud Audit Logs disabled**  
Enable Admin, Data Access, and System logs.

**No alerting on critical events**  
Create alert policies in Cloud Monitoring.

**Logs not routed to SIEM**  
Export logs to BigQuery or SIEM pipeline.

## Compute Risks
**Compute Engine default service accounts**  
Use custom service accounts with least privilege.
