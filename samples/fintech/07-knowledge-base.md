# Knowledge Base

This section contains sample Knowledge Base (KB) articles for the fictional **FinCore Platform**. These articles demonstrate how customer-facing documentation can help users quickly resolve common issues without contacting support.

> **Note:** These articles are fictional portfolio samples created to demonstrate technical writing and customer support documentation skills.

---

# KB-001: Unable to Authenticate API Requests

## Symptoms

API requests return:

```
401 Unauthorized
```

## Possible Causes

- Missing Bearer token
- Expired access token
- Invalid OAuth credentials

## Resolution

1. Verify that a valid OAuth access token is included in the request.
2. Ensure the token has not expired.
3. Generate a new access token if required.
4. Retry the API request.

---

# KB-002: Customer Creation Fails

## Symptoms

Customer creation returns:

```
409 Conflict
```

## Cause

A customer with the same Customer ID already exists.

## Resolution

- Verify the Customer ID.
- Use a unique identifier.
- Retry the request.

---

# KB-003: Kafka Events Not Received

## Symptoms

Expected events are not consumed by downstream services.

## Possible Causes

- Consumer is offline
- Incorrect topic subscription
- Network connectivity issue

## Resolution

1. Verify the Kafka topic name.
2. Confirm the consumer service is running.
3. Check consumer group configuration.
4. Review Kafka broker logs.

---

# KB-004: Invoice Generation Delayed

## Symptoms

Invoices are not generated on schedule.

## Possible Causes

- Billing scheduler unavailable
- Pending background jobs
- Database connectivity issues

## Resolution

- Verify scheduler status.
- Review application logs.
- Restart the billing service if necessary.
- Contact system administrator if the issue persists.

---

# Best Practices

- Search the Knowledge Base before creating a support ticket.
- Include request IDs when reporting issues.
- Capture screenshots where applicable.
- Refer to Release Notes for known issues.

---

# Related Documentation

- Banking Platform Overview
- REST API Guide
- Kafka Streaming Guide
- Release Notes
