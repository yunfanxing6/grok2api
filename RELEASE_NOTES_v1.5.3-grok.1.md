# Release Notes: v1.5.3-grok.1

Fork release based on upstream `grok2api v1.5.3`.

## Changed

- improved image generation compatibility for `grok-imagine-1.0-fast`
- clearer 429 / rate-limit propagation for image and video flows
- improved token-pool routing behavior for media models
- fixed `grok-imagine-1.0-edit` request handling used by `sub2api-grok`
- improved media result parsing for image and video endpoints

## Intended Use

This release is primarily intended to be used as the upstream Grok adapter behind:

- `sub2api-grok`

## Verified

- text generation
- image generation
- image edit (direct grok2api origin)
- video generation
