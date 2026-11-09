# Governance and Evidence

A reviewer needs to distinguish three questions. Is the contract ready? Did this invocation return the correct answer? Does the caller still have permission to act? DevFabric records a separate decision for each.

| Decision | Governing evidence | What happens when the check fails |
| --- | --- | --- |
| Approve sandbox access | Team, service, request and administrator decision. | A rejected request remains visible. A corrected request can be submitted. |
| Publish a tool | Readiness and security approval for the current contract revision. | A change invalidates the old revision's authority. Repair and reassess before publishing again. |
| Invoke a tool | Current publication, registered agent, tool access, permitted sandbox, scope and identity. | The operator receives a reason. A production probe is denied even after an approved sandbox run. |
| Evaluate the result | Business expectation for the target invoice compared with the returned payload. | A wrong response fails. Missing evidence can yield an inconclusive verdict. Passing the contract regression suite leaves this check open. |
| Review a consequential action | A specific pending receipt or reminder and the reviewer's decision. | Rejection prevents the held action. Approval of a held reminder rechecks current permissions and tool availability. |

For an overdue, unpaid invoice that permits reminders, the lookup should return eligible. A response that says otherwise fails its invocation evaluation. A correct response can still be awaiting human review. A past Pass grants no future authority.

These are executable rules in the local simulation. A production service would need to enforce identity and authorization outside the user's browser. [See the agent journey](agent-journey.md)
