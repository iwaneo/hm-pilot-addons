# Agent changelog

What changed in each version of the Agent add-on. The newest version is on top. Each entry
starts with a heading `## X.Y.Z (YYYY-MM-DD)`: the version and its release day.

The first line of every entry says whether the Agent's Home Assistant permissions changed:
`Permissions: no change.`, or `Permissions: ...` with what changed and why. The release
pipeline compares the add-on manifest with the last released version and stops when this
line does not match (decision issue 30, second resolution, point 5). An MSP reads this line
before an Agent update: by updating, the MSP accepts the permissions of the new version.

## 1.0.1 (2026-11-26)

Permissions: no change.

- The pilot build shows a neutral name instead of the product name, so the Agent can be
  public before the product name is cleared (issue 40).

## 1.0.0 (2026-11-24)

Permissions: first version. Role `homeassistant` with the Core API, the Supervisor API of
that role, an admin-only page through ingress, and no port, host network, Docker socket or
host folder (decision issue 15).

- First pilot release. Not published: a private add-on repository and a private image only.
