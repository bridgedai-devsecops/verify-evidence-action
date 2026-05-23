# BridgedAI verify-evidence-action

Calls the public supply-chain verification routes:

- **`POST /v1/artifacts/:artifactId/verify-supply-chain`** when **`mode`** is **`artifact-verify`** (default)
- **`GET /v1/builds/:buildId/supply-chain-verification`** when **`mode`** is **`build-summary`**

## Permissions

Use an API key with **`projects:read`** (or whatever the backend requires for these routes).

## Behavior

- **`offline`** defaults to **`true`** — do not assume live Rekor verification unless the backend capabilities say otherwise.
- This action does **not** claim full **Sigstore / Rekor** live cryptography; it forwards **`offline`** and surfaces **`findings-json`**.

## Inputs / outputs

See `action.yml`.
