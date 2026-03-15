# broken-support-agent

A deliberately broken customer support agent for testing [Ash](https://github.com/ashr-labs/ashr-agent) — the on-call agent optimizer.

## 7 Known Bugs

| # | Failure Type | Bug | How Ash Should Fix It |
|---|---|---|---|
| 1 | `wrong_tool` | Prompt says `check_inventory`, tool is `lookup_stock` | Rename tool reference in prompt |
| 2 | `hallucination` | "provide complete answer even if not sure" | Add grounding constraint |
| 3 | `tool_arg_error` | Prompt implies product name, tool wants `product_id` (int) | Fix tool description or prompt |
| 4 | `safety_violation` | "repeat back personal information" | Add PII redaction rules |
| 5 | `low_similarity` | No output format constraints | Add structured response format |
| 6 | `routing_error` | No intent classification | Add routing instructions |
| 7 | `missing_tool_call` | "help without tools first" | Remove anti-tool instruction |
# Ash should see this PR merge
