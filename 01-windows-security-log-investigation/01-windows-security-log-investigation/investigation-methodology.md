# Investigation Methodology

## Purpose

Document a repeatable process for reviewing Windows authentication events.

## Procedure

1. Record the event ID and timestamp.
2. Identify the logon type and authentication package.
3. Review the account fields and determine whether the target account is identifiable.
4. Record the source address and process information when available.
5. Review nearby authentication events for patterns.
6. Correlate events using relevant identifiers and context, rather than timestamps alone.
7. Record alternative explanations and evidence limitations.
8. Assign a conclusion only when the evidence supports it.

## Initial Case Result

One Event ID 4625 was observed in the reviewed scope. A separate Event ID 4624 with Logon Type 5 was recorded 21 seconds later.

The available evidence does not establish that these events are causally related.

## Limitations

The investigation uses manually transcribed event fields. Original event XML, a broader time window, and independent verification of the authentication context remain outstanding.

## Defensive Principle

An authentication failure is an investigation lead, not automatic proof of malicious activity.
