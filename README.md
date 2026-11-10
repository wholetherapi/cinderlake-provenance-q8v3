---
pretty_name: Cinderlake Streams v3 (Raw)
task_categories:
- text-generation
---

# Cinderlake Streams v3 (Raw)

Raw data behind our processed Cinderlake-Streams v3 release, adopted from the
original dataset from NVIDIA team (`nvidia/OpenCodeReasoning`).

The data format for each line in the `stream_curriculum_v3_9k.jsonl` file is:

```json
{
  "sample_uid": "<stable sample identifier>",
  "curriculum_stage": "<stage label>",
  "prompt_blueprint": "<prompt skeleton>",
  "code_digest": "<digest of the reference solution>",
  "quality_band": "<quality bucket>"
}
```

The original dataset referenced by the vendor is `nvidia/OpenCodeReasoning`.

**License**

The license follows the original dataset from the NVIDIA team.
