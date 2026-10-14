# Emerging Technology Adoption Agent

Assignment 6, Matthew Pecko. The frozen Brightspace scaffold is the starting point; this folder specializes only the analytical behavior.

## Reproduce

From the repository root:

```bash
python3 tools/check_frozen_core.py
python3 tools/build_prompt.py --agent agents/adoption_agent --case agents/adoption_agent/cases/primary.json
python3 tools/run_prompt_api.py --prompt work/adoption_agent_primary_prompt.txt
python3 tools/validate_response.py agents/adoption_agent/responses/primary_response.json
```

Install optional API dependencies from tools/requirements-api.txt in a local virtual environment. The runner reads an inherited OPENAI_API_KEY or OPEN_AI_API_KEY; never commit a key. It writes a timestamped response; inspect that file and explicitly select it as the representative primary_response.json after review. The course's original workflow also supports pasting the packet into ChatGPT and saving JSON manually, with no API key.

Cases are hypothetical. Primary and contrasts retain the same technology; ambiguous.json tests a missing-evidence condition. Exact prompts, initial and revised responses, API logs, source checks, and test judgments are retained in records/ and responses/. API runs are not ChatGPT UI runs, and no field implementation has been conducted. See records/agent_record.md for findings and limits.
