Executive summary

Between 14:49 PM and 15:20 PM GMT on 17th August, 2022, 31 customers experienced SQL server problems. the event was triggered by a new deployment.
The event was triggered by the monotoring tool. We migitated the event by by fixing the invalid parameters of SQL queries.
This incident affected 7% of customers

Leadup

At 14:40 on 17th August, 2022, a change was introduced to SQL server for new product features. The change caused errors server when querying newly
added customers with the invalid parameters.

Fault

420 queries were incorrectly sent to the server, 12% of the queries over the course of 40 minutes

Detection

The incident was discovered when the server alert was triggered and the DBM team was called. then they have to submit a page to the
platform team because they don't have access to read the service logs which slows down the response by 5 minutes

Resolution

SQL parameters in the code were fixed and deployed

lesson learned

SQL scripts should be re-checked in the test environment when code is merged before deployment
