# SOC Detection Lab using Splunk

## Overview
This project demonstrates basic SOC operations using Splunk by analyzing web server logs.

## Objectives
- Identify suspicious IP activity
- Detect reconnaissance behavior using HTTP status codes
- Monitor abnormal traffic patterns

## Key Use Cases
- Detection of high 404 responses (possible directory scanning)
- Identification of IPs generating repeated 403 errors
- Analysis of request frequency and access patterns

## Tools Used
- Splunk
- Sample web server logs

## Sample Queries
### Top Suspicious IPs
index=* sourcetype="access_combined_wcookie" status>=400
| stats count by ip
| sort - count

## Screenshots

## Conclusion
This project demonstrates how log analysis can be used to detect potential reconnaissance and suspicious behavior in web traffic.
