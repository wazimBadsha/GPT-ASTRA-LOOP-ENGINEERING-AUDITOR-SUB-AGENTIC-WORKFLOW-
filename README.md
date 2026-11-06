# GPT Astra — Agent Workflow Loop Engineering Auditor

**Version:** 1.0  
**Status:** Initial specification published; runtime audit not yet executed.

An evidence-first sub-agent specification for auditing GPT Astra's multi-step agent workflow engineering capabilities: planning, dependency DAGs, tool orchestration, specialist delegation, state management, checkpoint/recovery, retries, idempotency, cancellation, security, observability, and terminal-state correctness.

## Quick start

Read the complete specification:

- [Auditor specification](docs/GPT_ASTRA_AGENT_WORKFLOW_LOOP_AUDITOR_v1.md)

Then send the sub-agent the [first-run invocation](docs/GPT_ASTRA_AGENT_WORKFLOW_LOOP_AUDITOR_v1.md#5-first-run-invocation).

## Important execution boundary

The default mode is `EMULATED`. Use `REAL_RUNTIME` only when a real Astra runtime has been discovered, is callable, and produces observable evidence. A static specification or simulated workflow is not proof of runtime execution.

## Audit coverage

The specification defines six specialist workstreams and 18 controlled test scenarios covering tool calls, sequential workflows, DAG execution, handoffs, retry behavior, idempotency, malformed outputs, timeouts, authorization, approval/resume, checkpoint restoration, cancellation, context pressure, prompt injection, budget exhaustion, and recursive delegation loops.

## Safety

The auditor uses read-only inspection by default. It must not change billing, auto-recharge, account permissions, production data, repositories, or deployments without separate explicit authorization. It must not fabricate tool invocations, child agents, test results, traces, metrics, or successful repairs.

## Verdicts

- `VERIFIED STRONG`
- `CONDITIONAL`
- `PROTOTYPE`
- `NOT DEMONSTRATED`
- `FAILED`

A real-runtime certification is not available from `EMULATED` or `STATIC_AUDIT` mode.

## Current status

- Specification: published
- Astra sub-agent deployment: not verified
- Real Astra runtime invocation: not verified
- First audit run: not executed
