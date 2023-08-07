Issue Postmortem: Web Stack Outage

Issue Summary:
Duration: 3 hours and 45 minutes (from 2023-08-06 10:15 AM to 2023-08-06 2:00 PM, UTC)
Impact: The online booking service was down during the outage, affecting approximately 25% of the users.
Root Cause: A database deadlock occurred due to a flaw in the booking system's data handling logic.

Timeline:

2023-08-06 10:15 AM (UTC): Issue detected by monitoring system - sudden drop in API response time.
2023-08-06 10:20 AM (UTC): Operations team alerted by the monitoring system.
2023-08-06 10:25 AM (UTC): Operations team started investigating the issue, suspecting database overload.
2023-08-06 11:00 AM (UTC): False lead - Increased memory usage in the application servers assumed to be the cause.
2023-08-06 11:30 AM (UTC): False lead - Network congestion suspected due to recent infrastructure changes.
2023-08-06 12:00 PM (UTC): Escalated incident to the development team due to the complexity of the issue.
2023-08-06 1:30 PM (UTC): Development team identified the deadlock in the booking system's database queries.
2023-08-06 2:00 PM (UTC): The issue was resolved by fixing the data handling logic and releasing a hotfix.
Root Cause and Resolution:
The root cause of the outage was a database deadlock that occurred when multiple booking requests accessed the same set of database records simultaneously. The booking system's data handling logic had a flaw that caused race conditions, leading to these deadlocks.

To resolve the issue, the development team identified the critical code paths that triggered the deadlocks and implemented a new mechanism for handling concurrent booking requests. They added transaction management to ensure proper locking and prevent simultaneous access to critical data. After thorough testing, a hotfix was released, resolving the deadlock issue.

Corrective and Preventative Measures:

Improve Database Monitoring: Implement enhanced database monitoring to detect and alert on potential deadlocks or long-running queries promptly. This will enable quicker responses to similar issues in the future.

Review Data Handling Logic: Conduct a comprehensive review of the data handling logic across the entire application. Identify and eliminate any other potential race conditions or critical code paths that may lead to similar outages.

Automated Load Testing: Set up automated load testing that simulates high traffic conditions on the booking service. This will help uncover performance bottlenecks and potential deadlocks before they impact real users.

Incident Handling Training: Provide incident handling training to the operations team to ensure they take the most effective steps when investigating and troubleshooting issues.

Implement Circuit Breakers: Introduce circuit breakers in the booking service to prevent cascading failures in case of future outages or service degradation.

Tasks to Address the Issue:

Patch Booking System: Apply the hotfix that resolves the deadlock issue to the production environment.

Deploy Monitoring Solution: Set up the enhanced database monitoring system to detect deadlocks and long-running queries.

Code Review: Conduct a code review of the booking system's data handling logic to identify potential race conditions and critical code paths.

Load Testing Automation: Automate load testing on the booking service to ensure it can handle high user traffic.

Incident Handling Workshop: Organize a workshop for the operations team to improve their incident handling and troubleshooting skills.

By implementing these corrective and preventative measures, we aim to bolster our system's reliability, ensuring a seamless experience for our users and minimizing the impact of any future incidents.
