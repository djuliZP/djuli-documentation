# Refresh Tree *(legacy)*

This entry exists for backwards compatibility only. The refresh button is now per-view:

- [`refreshCluster`](../refreshCluster) — while viewing clusters
- [`refreshProject`](../refreshProject) — while viewing projects under a cluster
- [`refreshReport`](../refreshReport) — while viewing reports under a project

No element in the current webapp dispatches `Navigation/refreshTree` any more; this folder can be safely deleted once external references (if any) are updated.
