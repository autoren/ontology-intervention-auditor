# OIA-1 Track A 003b candidate-frontier acquisition report

**Audit:** `OIA-1-TRACK-A-003b`  
**Date:** 2026-08-21  
**Gate verdict:** **`candidate_frontier_feasible`**

## Scope

This was an opened Track A acquisition and admission audit only. It continued the
closed 003a resource gate without modifying or refreezing it. The accepted OIA-1
v0.2.1 archive remained byte-identical at
`2653020afcbf636def260da1517c9e3ba41c2ba1175fc210d4847b303febc33b`.

No OIA separator was synthesized, no real ARC environment action was executed, no
private or sealed environment was used, no credential was supplied, no paid or model
API call occurred, `cp437` was not rerun, and no Track B claim is made.

## Public acquisition

The public Zenodo object `article2_main_runs_additional.tar.gz` from record 21412274
was downloaded by a read-only GitHub Actions transfer job and verified before
inspection:

```text
size:    797,835,543 bytes
MD5:     4dd279f099609392c30cffa468801316
SHA-256: c3d85c4a75170de08837b9fc63cb7a7dde389b1205ca71b9f0fed16a9c09cf93
license: CC BY 4.0 record license
```

The first selection pass is preserved as a negative result. It selected zero files
because the paper-facing learner label `ewma_sv_v1.6` maps to archive directories
named `ewma_v1.6_sv`. The correction changed only archive path resolution. The
second pass selected the two frozen `ls20` run trees and their three sidecars each:

```text
selected files: 10,683
selected bytes: 28,897,676
manifest check: pass for every file
```

## Frozen candidate order

The parent 003a protocol remained unchanged. Before checkpoint behavior was
inspected, 003b additionally froze this order:

1. max final worktree;
2. xhigh final worktree;
3. then retained checkpoints round-robin by increasing iteration, max before xhigh;
4. retain the first candidate in that order for each finite behavior signature.

The exact frozen rule is retained as `protocol/checkpoint_enumeration_rule.frozen.json`
with Git blob SHA-1 `9ae3dba40fbc9df061af689a3cedda8b4b28b0ad` and SHA-256
`2802384b0dc5750ae5cfa47287174754c631f5b5b86d803e1ef7680cfd1efe5a`.

## Frozen prefix and action boundary

Both released runs contain a byte-identical reset observation before the first real
action:

```text
initial frame text SHA-256: 0fc0241eb2d3c992a2af68643f36e3878f5140fc85aed38410dd66ef5486afc7
initial metadata SHA-256:   0f1dfbd539066cba7373dcce2004196480db34dc2f8c01477e66e711b0c74347
canonical int16 frame SHA:  6305f5acb31a6c46bd260d54eb9c29dcddc91803a21189cd672ae4c0778b3f17
```

P0 has state `NOT_FINISHED`, zero completed levels, and actions `ACTION1` through
`ACTION4`. No parameterized `ACTION6` is available. The frozen finite screen is all
84 words at lengths one, two, and three.

## Candidate acquisition and admission

Thirteen executable attempts were screened in the frozen order: two released final
worktrees, then eleven retained checkpoints. Every attempt executed the complete
84-word seed-0 screen and reproduced P0 exactly. Behavioral deduplication found two
classes.

The first representative of each class was retained:

| Candidate | Fixed provenance | Native replay | Eight-process behavior hash |
|---|---|---|---|
| `max_final` | released final worktree, base HEAD `13618acd13f10eb351e2fa580b41cf62ba6a08b4` | levels 1–7 passed | `35aedc731ac854f713bffdb5463f88435b5a89e417841ee1b6c143e2599bb82a` |
| `max_iteration_2` | commit `93d546b7e1f2991f297949edf10c8fa8c5a225ea` | levels 1–3 passed | `ea5c7bb2147d2a1aa6cfe0ae18538f9641675ffd899e784627de27d95c564fee` |

For each admitted candidate, the screen was run twice in a fresh process at
`PYTHONHASHSEED=0,1,5,10`. All eight runs produced one candidate-specific behavior
hash, exact P0 rendering, zero execution errors, zero blocked audit events, and no
network or subprocess attempt. A once-reconstructed/deep-copied reset was checked
against full P0 reconstruction and produced byte-identical traces.

The candidates differ on 48 of the 84 frozen words. The shortest separator is:

```text
word: ACTION2
max_final settled frame:
3598cd92e4b667ab5962843fe8e2058e253b138b4aec18f28e3db8680f1a111c
max_iteration_2 settled frame:
6305f5acb31a6c46bd260d54eb9c29dcddc91803a21189cd672ae4c0778b3f17
both status: RUNNING
```

This establishes behavioral non-equivalence **within the frozen finite boundary**.
It is not a global-equivalence or impossibility result.

## Adapter and integrity boundary

Candidate execution contains only the transition engine, state reconstruction and
renderer, `game_status.py`, and the final candidate's two released level-7 static
artifacts needed for complete source closure. Static audit found no network,
service, subprocess, credential, or game-source dependency. Runtime reads during
all 16 promoted runs were limited to the three executable Python files because the
frozen prefix is level 1. The runner denied undeclared writes, runtime imports,
sockets, subprocesses, `os.system`, and dynamic library loading.

No game-source-like path was found in either released `agent_run` tree. The only
web/network term in the screened run-level files was the expected live
`client/client.py`, which is excluded from the candidate boundary. Pretrained-model
knowledge of the public game cannot be ruled out.

The release preserves animation evidence—389 intermediate frames in the max run and
474 in the xhigh run—but its executable verifier checks settled frames and status.
This audit preserves the multi-frame records while making only a settled-state
candidate claim.

A local check detected that `git status` refreshed two disposable analysis-copy
`.git/index` files. The untouched artifact was re-extracted, all 10,683 files were
reverified, and admitted source bytes were confirmed unchanged.

## Verdict and remaining boundary

**`candidate_frontier_feasible`** is warranted: two fixed, deterministic executable
candidates from a public released learner artifact initialize from one identical P0,
replay their available evidence, share a finite candidate-independent action set,
and differ inside the predeclared screen.

They are two states of one learner, not independently authored models. This audit
does not determine which candidate is externally correct, does not run an
OIA-selected intervention, and makes no ontology-identification, necessary-revision,
decision-superiority, sealed, or Track B claim.
