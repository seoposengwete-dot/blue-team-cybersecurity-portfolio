# Detection Rule: Repeated Failed Logons

## Objective

Identify potential password-guessing activity by detecting repeated failed authentication attempts from the same source within a defined time window.

## Detection Logic

Generate an alert when five or more failed logon events occur from the same source IP address within ten minutes.

## Relevant Windows Event IDs

- 4625 — Failed logon
- 4624 — Successful logon

## Test Result

The synthetic dataset contains five failed logons from `192.0.2.25` between 09:00 and 09:04:40 on 15 October 2026.

The source meets the configured threshold and should trigger an alert.

A subsequent successful logon is present in the dataset and should be considered during follow-up investigation.

## Analyst Response

1. Review the affected account and authentication timeline.
2. Examine whether the source is expected or authorised.
3. Check for additional failed or successful logons.
4. Review relevant endpoint and identity telemetry.
5. Escalate if corroborating evidence indicates unauthorised access.

## Limitations

This rule may generate false positives from mistyped passwords, stale credentials, or legitimate automated processes. It may also miss distributed attempts that remain below the per-source threshold.

The threshold is a training example, not a universally appropriate production setting.

## Conclusion

The rule identifies suspicious authentication patterns for investigation. It does not independently establish malicious intent or account compromise.

**Dataset:** Synthetic training data; no real attack is claimed.
