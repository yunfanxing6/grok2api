# Release Notes: v1.6.2-grok.1

Fork release based on the current `grok2api` 1.6.x codebase while preserving the existing `sub2api-grok` integration contract.

## Changed

- kept compatibility for `grok-imagine-1.0-fast` image generation requests
- preserved clearer `429` / rate-limit propagation instead of collapsing those failures into generic `502`
- kept media token-pool routing improvements for image and video workloads
- preserved the fixed `grok-imagine-1.0-edit` request path used by `sub2api-grok`
- preserved improved image/video result extraction used by the Grok upstream adapter
- propagated structured error codes in function imagine/video SSE responses
- refreshed fork release docs for the current compatibility baseline

## Compatibility Position

This release intentionally stays on the stable pre-v2 architecture so it can continue serving as the Grok upstream behind:

- `sub2api-grok`

It does **not** attempt a direct migration to upstream `grok2api v2.x`, because that would require a much larger integration rewrite.

## Verified

- service boots on the existing deployment layout
- direct health endpoint
- direct model-route compatibility assumptions preserved for `sub2api-grok`
- existing image / image-edit / video compatibility patches remain in place
