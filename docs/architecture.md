# Platform Architecture

DevFabric runs as a static browser application. The Developer, Agent, Administration and Insights workspaces share a local command model. Accepted actions produce records that another persona can inspect. The browser stores and replays a versioned command log so progress survives refresh.

| Boundary | Information passed | Result |
| --- | --- | --- |
| Case rehearsal → workspace | A case reference carries the business context. | The workspace starts with its own records. Approvals, permissions and task outcomes stay in the rehearsal that produced them. |
| Developer → administrator | Service, accountable team, requested environment and proposed plan. | The request ledger retains the decision and simulated provisioning lifecycle. |
| API owner → reviewer → operator | Contract, required evidence and exact revision. | Publication exposes a tool descriptor. Calling it requires an active grant and the permitted environment. |
| Task runner → reviewer → insights | Task, invocation, invoice, tool, expected and actual responses, and evaluator version. | The reviewer decides on that receipt. Insights counts the task once as its state changes. |
| Workspace → context graph | Selected records and labeled joins or scenario assumptions. | A read-only projection supports impact and tool-fit questions across three entry points. |

Practice tours use isolated state. Infrastructure allocation, pipeline runs, tool responses and reminder delivery use local simulation. The role selector lets a visitor act through different workspaces. Enterprise identity, tenant isolation and trusted server-side policy enforcement are proposed pilot capabilities.

[Governance decisions](governance.md) · [Implementation boundaries](capability-map.md)
