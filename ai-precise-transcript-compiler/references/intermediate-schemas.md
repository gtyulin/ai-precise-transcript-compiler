# 中間產物欄位範本

## `meaning_units.jsonl`

每行一個 JSON 物件：

```json
{"unit_id":"MU-001","source_refs":["T01-P003-L012..L016"],"verbatim_excerpt":"…","paraphrase":"…","open_codes":["…"],"status":"included","evidence_level":"explicit","uncertainty":null}
```

`status` 建議使用：`included`、`merged`、`context_only`、`excluded_with_reason`、`unresolved`。`evidence_level` 使用：`explicit`、`reconstructed`、`inference`、`unresolved`。

## `concepts.jsonl`

```json
{"concept_id":"C-001","label":"…","member_unit_ids":["MU-001","MU-014"],"relation":"similar","merge_rationale":"…","counterexamples":[],"evidence_level":"reconstructed"}
```

## `provenance_audit.json`

```json
{"status":"PASS|FAIL|PARTIAL","source_units":0,"covered_units":0,"unmapped_units":0,"handout_claims":0,"unsupported_claims":[],"unresolved_items":[],"sample_checks":[]}
```

數字必須由實際產物計算；不能以模型估計值填寫。若無法計算，填 `null` 並說明原因。
