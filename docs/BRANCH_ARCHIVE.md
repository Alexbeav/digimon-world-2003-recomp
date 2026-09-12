# Preserved development history

The default branch is the maintained source. The tags below preserve earlier source or separate candidates at exact commits.
No archived candidate gains new build, package, or gameplay acceptance through this cleanup.

A tag is a fixed source snapshot. Existing tree URLs and `git clone --branch <name>` can select these tags.
For local inspection, use `git fetch origin --tags` followed by `git switch --detach refs/tags/<name>`.
To resume development, create a temporary branch from the tag. Do not move an archive tag.

| Tag | Preserved commit | Disposition |
|---|---|---|
| `review/athena-title-fixes-20260912` | [`da075134f190923d82bd3e24f7f0243200101c92`](https://github.com/Alexbeav/digimon-world-2003-recomp/tree/da075134f190923d82bd3e24f7f0243200101c92) | Unqualified title candidate; source checks do not establish gameplay. |

Recorded 2026-09-13. Existing version tags and releases remain unchanged.
